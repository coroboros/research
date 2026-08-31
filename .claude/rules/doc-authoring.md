# Documentation Authoring

Rules for authoring content in this repo. Same frontmatter and citation discipline across both formats.

## Format taxonomy

- `articles/` — long-form technical references, standalone reading (typically 500+ lines)
- `notes/` — short-form observations, hypotheses, synthesis (typically under 200 lines)

When in doubt between article and note, default to article — promoting a note later is easier than splitting an article.

## Filename

Follow the canonical [Claude Project KB naming conventions](https://github.com/coroboros/archivist/blob/main/docs/insights/claude-project-knowledge-bases-best-practices.md) (kebab-case, ASCII-only, descriptive). Curated in `coroboros/archivist`.

## Frontmatter

Required, exact keys, double-quoted strings:

```yaml
---
title: "Human-Readable Title"
date: "YYYY-MM-DD"              # publication date
author: "Coroboros"             # or a specific human name
tags: ["tag-one", "tag-two"]    # lowercase kebab-case, surfaces in INDEX.md
sources:
  - "https://primary-source.example.com"
  - "org/repo"                  # GitHub shorthand OK
---
```

Optional:

- `revision: "YYYY-MM-DD"` — last major revision after publication
- `status: "draft" | "published"` — defaults to `published` when merged to `main`

An index `README.md` inside an article folder carries the same frontmatter.

## Body

Clean Markdown. One `# H1` matching `title`. No custom HTML beyond this rule file. Cite sources inline where claims are made — primary sources first, aggregators second. Keep `sources:` frontmatter as the consolidated deduplicated list.

## INDEX

Add every new article or note to `INDEX.md` under the matching topic section. Create a new section when the entry opens up a new topic area that will plausibly collect more than one piece over time. Mark the format (`**Article**` or `**Note**`) as a prefix in the index entry — topic drives navigation, format prefix sets reading expectations.

## README tables

`README.md` has two tables — Articles and Notes. Update the matching one when shipping a major piece. The README surfaces major references; `INDEX.md` is the complete listing.

## What NOT to author here

- Anthropic-authored documentation — belongs in `coroboros/archivist/docs/insights/`
- Internal SOPs, proprietary prompts, unsanitized strategy notes — belong in a private location, not in this public repo
- Runnable code and skills — `coroboros/agent-skills`

## Promoting content from a private source

When content is ready to move from a private location to this public repo:

1. Sanitize — remove any references to internal systems, client names, un-attributed quotes.
2. Rewrite frontmatter (`author: "Coroboros"`, fresh `date`, complete `sources`).
3. Remove or archive the internal version at its private origin to avoid two-version drift.
