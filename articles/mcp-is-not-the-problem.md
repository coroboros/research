---
title: "MCP Is Not the Problem"
date: "2026-05-18"
author: "Coroboros"
tags: ["mcp", "model-context-protocol", "claude-code", "agent-skills", "cli", "code-mode", "context-window", "tokens", "cloudflare-workers", "anthropic", "notion", "tooling", "agent-architecture"]
sources:
  - "https://www.anthropic.com/engineering/code-execution-with-mcp"
  - "https://blog.cloudflare.com/code-mode-mcp/"
  - "coroboros/agent-skills"
  - "https://developers.notion.com/guides/mcp/overview"
---

# MCP Is Not the Problem

> The cost is context, not the protocol.

Preferring curated skills and CLIs over standard MCP for external services is an argument about context economics. It is not a verdict on the protocol. MCP is sound. Loading every tool definition into the context window at all times is not. Read the rule that way and the apparent contradiction resolves — a Notion skill that routes 95% of its work *to* MCP.

---

## 1 / The two ways tool-calling burns context

Standard MCP tool-calling spends context twice.

First, on definitions. Anthropic's engineering writeup states that agents wired to thousands of tools process hundreds of thousands of tokens before reading the request. Cloudflare quantifies the same failure on its own API: 2,500+ endpoints, one MCP tool each, over 2 million tokens. An equivalent server without Code Mode would consume 1.17 million tokens. Cloudflare notes that exceeds the entire context window of the most advanced foundation models.

Second, on intermediate results. Every tool result passes back through the model. Anthropic's example: a 50,000-token meeting transcript fetched by one tool and handed to another flows through context twice. Large documents exceed the window and break the run.

That is the whole basis of the rule. Not protocol quality. Token accounting.

## 2 / The Notion skill — routing, not rejection

Coroboros' Notion skill is the counter-example to "CLI beats MCP."

It defaults to the official Notion MCP for ~95% of intents. It drops to the `ntn` CLI for the five cases the MCP cannot serve. The MCP is the richer surface; the CLI fills the holes.

| Capability | Notion MCP | `ntn` CLI |
|---|---|---|
| SQL DDL schema create/alter | Yes — DSL, no CLI equivalent | No |
| View create/update via View DSL | Yes — DSL, no CLI equivalent | No |
| Block-level comments on rendered Markdown | Yes | No |
| Batch up to 100 rows in one call | Yes | No |
| Semantic search across connected sources | Yes — Slack, GDrive, GitHub, Jira | No |
| File upload to Notion | No upload tool | Yes — `ntn files create` |
| Notion Workers / serverless | No Workers tools | Yes — `ntn workers` |
| Headless / CI / non-interactive | Requires an interactive session | Yes — token + `--json --yes` |
| Raw API endpoint discovery | No | Yes — `ntn api ls` |
| Shell piping into `jq` | No | Yes |

The skill is the routing layer. It decides which transport answers which intent, so the model never carries the full MCP catalogue or the full CLI surface. A skill that wraps MCP curates that surface. The failure mode is an agent statically loaded with every server's definitions.

## 3 / Code Mode MCP — the exception that flips the rule

The exception to the rule is Code Mode MCP, and it is decisive at scale.

Code Mode keeps MCP and stops exposing tools as tool-calls. Anthropic presents MCP tools as code modules on a filesystem. The agent reads only the definitions it needs and calls them in code, `await gdrive.getDocument({...})`. Cloudflare collapses 2,500+ endpoints to two tools, `search()` and `execute()`, both taking code, ~1,000 tokens of context total.

The numbers carry the argument. Anthropic: 150,000 tokens of definitions down to 2,000, a 98.7% cut. Cloudflare: 1.17 million down to ~1,000, ~99.9%. Intermediate data stays in the sandbox — a 10,000-row sheet is filtered in code so the model sees five rows, not 10,000.

This is why the exception exists. Code Mode MCP is MCP behind a code-execution boundary. That boundary removes the exact context tax that motivated preferring skills and CLIs.

It is not free. Anthropic is explicit: running model-written code requires a sandbox with resource limits and monitoring that direct tool calls avoid. Cloudflare runs it in a Dynamic Worker isolate — a V8 sandbox with no filesystem. Outbound fetch is disabled by default; tokens are downscoped under OAuth 2.1. Cloudflare's own claim cuts against unconditional CLI preference too: a CLI is a far broader attack surface than a sandboxed isolate.

## 4 / The decision

Three transports. One axis decides between them: context cost against capability and blast radius.

| | Standard MCP tool-calls | Skills + CLI | Code Mode MCP |
|---|---|---|---|
| Context cost | High — every definition resident | Low — the skill curates | Lowest at scale — ~1,000 tokens |
| Best for | Small, stable tool sets | External services, scripting, CI | Large API surfaces, hundreds to thousands of endpoints |
| Intermediate data | Through the model | Through the model or shell | Stays in the sandbox |
| Control flow | Model-driven turns | Shell or script | Real code — loops, filtering, chaining |
| Failure cost | Context exhaustion | Low | Sandbox plus monitoring overhead |
| Security note | Many tools, many tokens | Broad CLI attack surface | Isolated; downscoped tokens |

Pick standard MCP when the tool set is small and fixed — the definition cost is bounded and a skill adds nothing. Pick skills plus CLI for external services with modest surfaces, scripting, and headless paths — the Notion skill's default. Pick Code Mode MCP when the surface is large, because no curation beats not loading the catalogue at all.

## 5 / Restated

MCP is not the problem. Unbounded tool-definition loading is. The skills-and-CLI preference is a context-economics heuristic with a hard exception. When the API surface is large, MCP behind a code-execution sandbox wins on the metric the heuristic optimizes — tokens. The Notion skill proves the nuance in production: a skill that chooses MCP for nearly everything, and the CLI only where MCP has no answer.

The protocol was never the cost. The accounting was.
