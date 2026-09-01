---
title: "The Winning Recipe of AI Design Skills"
date: "2026-08-31"
author: "Coroboros"
tags: ["web-design", "agent-skills", "ai-slop", "typography", "design-systems", "frontend", "claude-code", "prompt-engineering", "verification"]
sources:
  - "https://github.com/elayadesign/ai-design-skills"
  - "https://github.com/elayadesign/redesign-skill"
  - "https://github.com/NousResearch/hermes-agent"
  - "https://github.com/pbakaus/impeccable"
  - "https://github.com/Nutlope/hallmark"
  - "https://github.com/anthropics/claude-plugins-official"
  - "https://github.com/openai/plugins"
  - "https://github.com/Leonxlnx/taste-skill"
  - "https://github.com/alchaincyf/huashu-design"
  - "https://github.com/nextlevelbuilder/ui-ux-pro-max-skill"
  - "https://github.com/Melvynx/aiblueprint"
---

# The Winning Recipe of AI Design Skills

A 403-line Markdown file with no scripts, no templates, and no reference folder holds more decided design than systems twenty-four times its size. That file is `landing-page-design` in [elayadesign/ai-design-skills](https://github.com/elayadesign/ai-design-skills), and it is the sharpest data point in a corpus of eleven open-source systems that all attack the same problem: language models generate visually recognizable, interchangeable interfaces by default, and instructions alone do not fix it.

This article reads those eleven systems line by line and extracts what converges. The systems disagree on almost everything visible: single file versus 107-file tree, honor-system checklists versus screenshot diffing, imposed house style versus derived identity, English prose versus a Chinese three-subagent pipeline. Underneath, the ones that work share a small set of mechanisms. Three independent authors ship lists of faces to refuse by default, and all three name Inter. Eight force a written commitment before code. Three independently refuse the eyebrow label above a heading, one as an outright ban. The recipe exists, with file-and-line provenance against each repository's state at the end of August 2026.

Line counts throughout follow each system's own packaging: skill files as shipped, verified with `wc -l`, data and site chrome excluded unless stated. Quality verdicts are read from the instruction files — what each system decides, bans, and measures — not from rendered builds; no comparative output was generated for this piece.

## 1 / The case study — why 403 lines beat 9,752

`skills/landing-page-design/SKILL.md` is the entire elaya skill: one file, 403 lines. Six properties explain its output quality.

**1. Zero freedom on commodity axes.** The file imposes exact values wherever a model's prior is weak. Fonts: "Use: Geist, Manrope, Geist Mono, Poppins" and "Never use: Inter, Roboto, Arial, Open Sans, Helvetica" (`SKILL.md:154,156`). Type sizes "resolve … to Tailwind's default type scale", snapped "to the closest step below" (`:172,174`). Spacing is a closed table: "Only these values. Nothing between them, nothing outside them" (`:201`). Radii follow arithmetic: "inner radius = outer radius − gap" (`:228`). Motion allows one curve: "cubic-bezier(0.32,0.72,0,1)" (`:272`). Dark backgrounds come from a list of six hex values (`:244`). The model decides nothing where deciding badly is its habit.

**2. One committed house style.** The floating "glass pill" nav (`:277`), the heading gradient from `#FFFFFF` to `#9B9B9B` (`:250`), the flat backgrounds (`:238`): every output pattern-matches one contemporary look, declared as "the non negotiable visual system" (`:12`). The cost is that every elaya page resembles every other elaya page. The instructive detail: a mandatory glass nav (its expanded menu ships `backdrop-blur-3xl`, `:281`) is precisely what another corpus system flags as slop tell #5, "Unearned blur — glassmorphism with no real depth/elevation system behind it" ([hermes-agent](https://github.com/NousResearch/hermes-agent) `skills/creative/claude-design/SKILL.md:446`). The same pattern is a tell when it is a default and a signature when it is a commitment.

**3. Strategy before pixels.** Part A settles "one offer → one audience → one primary action" (`:10`), page structure, headline formulas ("{Outcome} without {pain}", `:104`), and the top three objections "as a section, not a footnote" (`:99`) before Part B allows any visual work: "Work through A before touching B" (`:12`).

**4. One mandatory signature moment.** Section B11 is titled "Tagline reveal section (mandatory)" (`:341`): one large type section where "each word transitions individually from that muted tone to the full text color, in reading order" (`:355`). Exactly one place spends the boldness budget.

**5. Fully resident.** All 403 lines are in context whenever the skill runs. Nothing is lazy-loaded, so no rule can fail to load. Larger systems route around their own size: [Nutlope/hallmark](https://github.com/Nutlope/hallmark) instructs "Do not load the whole catalogue — that's ~37 KB of dead weight for a single pick" (`skills/hallmark/SKILL.md:266`), spending lines policing the cost of its own lines.

**6. Terminal re-anchoring.** The procedural body closes with checklists for states ("Every interactive element ships with its full state set", `:315`), content realism ("Never ship filler. These are the tells that a page was generated rather than made", `:301`), and ship requirements (`:328`), and a terminal quick checklist (`:377`) re-grounds the model immediately before emission.

## 2 / The recipe — twelve mechanisms

The corpus converges on twelve mechanisms. Each entry cites the systems that carry it.

**1. Commit to a written direction before code.** Universal among the strong systems. elaya's Part A precedes Part B. [pbakaus/impeccable](https://github.com/pbakaus/impeccable) requires the direction "as a contract in the artifact's opening comment, five short blocks, 150 words at most" (`skill/reference/new-work.md:75`). hallmark demands: "State your pick. Before writing any code, say `Macrostructure: <name>. Theme: <name>. Differs from the last on: <axes>.` in plain text" (`skills/hallmark/SKILL.md:284`). [alchaincyf/huashu-design](https://github.com/alchaincyf/huashu-design) writes the pick into a `direction-approved.md` gate file, and a repository shell hook, wired into `settings.json` by hand and never installed by the skill (`scripts/design-gate-hook.sh:14`), blocks renders of 45 seconds or longer when the file is missing (`SKILL.md:326,413`; `design-gate-hook.sh:7`). [Anthropic](https://github.com/anthropics/claude-plugins-official)'s 55-line `frontend-design` works "in two passes. First, brainstorm a short design plan" (`plugins/frontend-design/skills/frontend-design/SKILL.md:33`). OpenAI's `get-context` is a mandatory brief gate: before any build skill runs, it plays the brief back "in one pithy user-visible note" (`plugins/product-design/skills/get-context/SKILL.md:38`). taste-skill's one-line Design Read and hermes's out-loud archetype commitment are the same rule in smaller form (`skills/taste-skill/SKILL.md:25`; `skills/creative/claude-design/SKILL.md:172`). A direction that lives only in the model's head is re-decided, worse, at every generation step.

**2. Name and ban the model's fingerprint.** Three authors independently ship lists of faces to refuse by default. hallmark: "These fonts are on-distribution for every LLM … Inter, Roboto, Open Sans, Lato, Poppins" (`skills/hallmark/references/typography.md:38,40`). elaya bans five of the same faces (`SKILL.md:156`). impeccable names sixteen: "these training-data defaults mean you stopped looking: Fraunces, Playfair Display … Inter-as-display, DM Sans, DM Serif, Outfit" (`skill/reference/new-work.md:65`); Inter is the one face on all three lists, impeccable's as a display face. Its craft floor extends the ban to composition: identical card grids, gradient text, "Glass and blur as decoration", and the eyebrow, "a ban, not a default: no brief earns it back" (`skill/reference/craft-floor.md:25,33,34,27`). hallmark's anti-patterns file calls the purple-gradient hero "the single most-recognised AI aesthetic" (`skills/hallmark/references/anti-patterns.md:13`), and its skill ships section eyebrows "default OFF" (`skills/hallmark/SKILL.md:450`). The lists even disagree — elaya's four-face allowlist includes Poppins (`SKILL.md:154`) while hallmark lists it as on-distribution — and the deeper form of the rule absorbs the conflict by naming the model's own reflex rather than any fixed list: "Treat that first palette as already spent … nothing about the subject requires your default" (impeccable, `new-work.md:70`). Anthropic states the same diagnosis: the current defaults "are defaults rather than choices, and they appear regardless of subject" (`SKILL.md:31`).

**3. Slop is compositional before it is cosmetic.** The hermes `claude-design` skill contributes the corpus's central analytical claim: "Most AI design slop is compositional, not cosmetic — the model reaches for a centered hero + three equal-weight feature cards for every surface, then decorates … the layout was wrong before a single color was chosen" (`SKILL.md:170`). Its seven surface archetypes (Monitor, Operate, Compare, Configure, Decide/Learn, Explore, Command/Inspect) each carry a composition, and "The hero-plus-three-cards composition is correct for Decide/Learn only. Reaching for it anywhere else is the #1 tell" (`:189`). Repair is sequenced: "Diagnose first, treat second — auditing and fixing in one breath fails, because the model's prior outweighs the instruction" (`:438`), and compositional tells are causes while the rest "are usually symptoms" (`:461`).

**4. Concrete values on commodity axes, freedom on identity axes.** elaya's closed tables (property 1 above) are the extreme case. The generalizable version derives identity from the subject's world instead of from a template, which is what impeccable's "already spent" rule forces (`new-work.md:70`): after rejecting the reflex, the second choice must come from somewhere, and the only somewhere left is the brief.

**5. One signature moment, exactly one.** elaya's mandatory B11 reveal (property 4 above). Anthropic's compressed version quotes Chanel: "before leaving the house, take a look in the mirror and remove one accessory" (`plugins/frontend-design/skills/frontend-design/SKILL.md:43`).

**6. Content realism.** elaya's realism checklist (property 6 above). OpenAI's rubric bans faked assets outright: "Never fake visible assets with ASCII, prose, text symbols, emoji, placeholder boxes, CSS art, div art …" ([openai/plugins](https://github.com/openai/plugins) `plugins/product-design/references/critical-overrides.md:58`).

**7. Full state coverage plus a ship checklist.** elaya's B9 states and B10 ship requirements. OpenAI's QA rubric enumerates "hover, focus, active, selected, disabled, loading, success, error, empty states" (`plugins/product-design/skills/design-qa/references/qa-rubric.md:30`). [elayadesign/redesign-skill](https://github.com/elayadesign/redesign-skill) places "Loading, empty, and error states" as its own fix-priority rung (`skills/redesign-existing-projects/SKILL.md:206`).

**8. Build section by section; never regenerate the page.** The redesign skill is built on it: "Scan … Diagnose … Fix — Apply targeted upgrades inside the existing stack, in the Fix Priority order" (`SKILL.md:20–22`).

**9. Verify with fresh pixels and an isolated reviewer.** The most unevenly distributed mechanism, detailed in the ladder below. Its strongest form is impeccable's: "Assessment A and B MUST run as two isolated sub-agents … They must not see each other's output" (`skill/reference/critique.md:8,33`) whenever a sub-agent tool is exposed, because "a review anchored on the contract inherits whatever the builder's abstraction dropped" (`skill/agents/impeccable-finish-reviewer.md:25`).

**10. Stay small and fully resident.** 403 always-loaded lines beat 9,752 lazy-loaded ones. The strong small systems (elaya 403, Anthropic 55, redesign 259, hermes 650) hold their whole contract in context; the large ones document their own loading discipline as a failure mode to manage (hallmark `SKILL.md:266,357`).

**11. Landing pages: conversion before visuals.** elaya's Part A is a conversion argument, headline formulas and objection sections included, before any aesthetic decision. No other corpus system treats persuasion structure as a first-class phase (impeccable comes closest, folding conversion into the Persuade form's own vocabulary, `new-work.md:59`); most treat a landing page as a styling problem.

**12. The separation ladder.** OpenAI's `ideate` skill orders section separation: "1. Use spacing, grouping, alignment, typography, and hierarchy … 2. Use simple dividers … 3. Use a subtle surface tint … 4. Use borders only when separation still is not clear. 5. Use shadows/elevation last, and sparingly" (`plugins/product-design/skills/ideate/SKILL.md:139–143`), paired with "Do not put cards inside cards. Do not make every major section a card" (`:147`). The compact antidote to the everything-is-a-card disease.

## 3 / The verification ladder

How a system checks its own output separates the corpus more than any aesthetic choice. Four rungs, in ascending order of trustworthiness.

**Rung 0: the honor system.** [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) (1,206 lines) closes its procedural body with a pre-flight matrix of 62 self-declared checkboxes: "THIS IS NOT OPTIONAL. Run every box." (`skills/taste-skill/SKILL.md:914`). No executable check ships; even the box labeled "mechanical" is the model counting its own output (`:933`). hallmark's 58-gate slop test is the same architecture at larger scale: 107 files, zero scripts, "Every answer must be no" (`skills/hallmark/references/slop-test.md:3`), "Eyeball each viewport" (`:170`). A self-assessment asked of the author is not a check; the model that produced the slop grades the slop.

**Rung 1: data lookup.** [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) queries ~4,300 lines of CSV (styles, palettes, 74 font pairings, UX rules) through a search script (`.claude/skills/ui-ux-pro-max/SKILL.md:42`). Retrieval is real, but what it retrieves is the industry's central tendency; see the anti-lessons below.

**Rung 2: gate artifacts.** OpenAI's `design-qa` writes a `design-qa.md` whose "final result must be exactly passed or blocked" (`plugins/product-design/skills/design-qa/SKILL.md:168`) and instructs "Do not let the build skill hand off as done" when comparison is impossible (`:19`). huashu's opt-in hook (mechanism 1 above) refuses long renders without `direction-approved.md`, with `SKIP_DESIGN_GATE=1` as an auditable bypass (`design-gate-hook.sh:12`). The artifact makes skipping the gate a visible act instead of a silent one.

**Rung 3: measured pixels.** impeccable ships 61 deterministic detector rules in an executable registry (`cli/engine/registry/antipatterns.mjs`) and a comp-diff pipeline that scores a build screenshot against its approved comp on structure, color, detail, and bands (whether the horizontal sections line up), with per-region verdicts of match, drift, missing, or contradicted (`skill/scripts/comp-diff.mjs`). Its review rule generalizes: "Never judge fidelity from one full-page thumbnail; it hides exactly the failures that matter" (`new-work.md:131`).

The ladder's lesson: instructions raise the floor, measurement holds it. Every system on rungs 0 and 1 depends on the model resisting its own prior at the exact moment the prior is strongest.

## 4 / The eleven systems

- **elayadesign/ai-design-skills** · 403 lines, 1 file — the case study above, whole. The most decided design per line in the corpus, at the price of a house style every output shares.
- **elayadesign/redesign-skill** · 259 lines — scan, diagnose, fix, in a priority ladder ordered by impact over risk: "1. Font swap — biggest instant improvement, lowest risk" (`skills/redesign-existing-projects/SKILL.md:200`). The pragmatic answer to every make-it-look-better request.
- **NousResearch hermes-agent, claude-design** · 650 lines plus two siblings — the compositional theory above, split into three composable siblings: process (`claude-design`), brand mimicry (`popular-web-designs`, 54 templates), and token specs (`design-md`).
- **pbakaus/impeccable** · 5,305 prose lines plus a large executable layer — contract, "already spent", a craft floor of category defaults the brief must earn back (the eyebrow alone an outright ban), 61 detector rules, comp-diffing, isolated reviewers. The reference implementation for measured verification.
- **Nutlope/hallmark** · 9,752 lines, 107 files, zero scripts — maximal instruction: 21 claimed themes, a slop test of 57 or 58 gates depending on which file counts, "State your pick". Its scale produces the corpus's clearest internal contradictions (below).
- **alchaincyf/huashu-design** · 10,607 skill-scoped Markdown lines (Chinese) — three direction drafts from three parallel, mutually isolated subagents ("independent contexts … to avoid convergence", translated from `SKILL.md:290`), a user pick recorded in `direction-approved.md`, and the opt-in gate hook above.
- **Leonxlnx/taste-skill, taste-skill** · 1,206 lines — aggressive taste rules (a declared design read before code, three intensity dials, an image-generation-first mandate for real assets) ending in 62 honor-system checkboxes. Strong opinions, unverified execution.
- **nextlevelbuilder/ui-ux-pro-max-skill, ui-ux-pro-max** · 6,943 prose-and-script lines plus ~4,300 of CSV — a searchable recommendation database (192 product reasoning profiles, 74 font pairings, queried by script). The corpus's control group: it recommends the exact center of the distribution the other systems exist to escape.
- **[Melvynx/aiblueprint](https://github.com/Melvynx/aiblueprint), use-style** · 4,092 lines — thirteen named preset styles loaded on demand and treated "as hard constraints" (`agents-config/skills/use-style/SKILL.md:24`); the Stripe preset pins `#635BFF` and substitutes Inter for Söhne (`agents-config/skills/use-style/styles/stripe.md:15,90`). Identity by imitation, instantly.
- **OpenAI plugins, product-design and frontend-app-builder** · 1,473 SKILL.md lines across the ten-skill plugin and the builder — separation ladder, cards-in-cards ban, default eyebrow prohibition (`plugins/build-web-apps/skills/frontend-app-builder/SKILL.md:27`), faked-asset bans, the passed/blocked gate. The corpus's reference for product surfaces, where most others think in landing pages.
- **Anthropic frontend-design** · 55 lines — a design-lead persona, the three-cluster diagnosis, plan-then-build, the removed accessory. Proof that the recipe's core fits in a page when the model is trusted to execute judgment.

## 5 / Anti-lessons

**The mono-skill disease.** hallmark demonstrates what scale does to an instruction-only system. Its 9,752 lines contradict themselves: italic display is banned globally ("All display is roman — italic headers are banned globally", `SKILL.md:277`; gate 38a fails any italic heading, `slop-test.md:100`) while the custom-theme protocol prescribes "italic-serif — Fraunces italic, Newsreader italic" as a display style and its worked example picks "display Fraunces italic" (`skills/hallmark/references/custom-theme.md:189,281`). The skill claims 21 catalog themes (`SKILL.md:251`) while its own gate 57 lists 20 (`slop-test.md:186`); the README says "fifty-seven slop-test gates" (`README.md:13`) while the gate file is titled "58 gates" (`slop-test.md:1`). The failures are structural: a contract grown past what any single load, or any single author pass, can hold consistent.

**The control group.** ui-ux-pro-max is built from real industry data, and that is exactly its limitation: pairing No. 1 in its typography table is Classic Elegant, Playfair Display with Inter (`.claude/skills/ui-ux-pro-max/data/typography.csv:2`), and pairing No. 5 is Inter paired with itself. Both faces sit on the corpus's ban lists — Inter on all three, Playfair Display on impeccable's sixteen and, as body copy, hallmark's (`skills/hallmark/references/typography.md:38,40,41`). Aggregated best practice reproduces the average; the average is the fingerprint. A recommendation engine cannot escape a distribution it is built from.

**Presets are speed, not identity.** use-style delivers consistency instantly, and every consumer of the same preset ships the same look, borrowed from a brand that is not theirs. The contrast with impeccable's "already spent" rule is the corpus's central fork: identity by imitation versus identity derived from the subject. Presets win on speed for internal tools; derivation is the only route to an output that could not have come from anyone else's prompt.

## 6 / What generalizes

Reduced to what survives across the corpus, the recipe is short. Decide in writing before generating, because an undecided direction collapses to the prior. Ban the prior by name: the model cannot see its own habits. Fix composition before color, because decoration on a wrong layout is polish on a wrong answer. Impose exact values wherever the axis is commodity, and derive from the subject wherever the axis is identity. Spend boldness once. Keep the whole contract resident: a rule that is not loaded does not exist. And measure the output with something that is not the author, because the honor system fails precisely on the failures that matter.

The elaya file is the proof that most of this fits in 403 lines. The impeccable detector is the proof that the last mechanism cannot be written in prose at all.
