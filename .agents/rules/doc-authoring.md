# Documentation authoring

Articles and notes share the frontmatter and citation contract below.

## Format taxonomy

- `articles/` — standalone technical references.
- `notes/` — focused observations, hypotheses, or synthesis.

Choose by purpose; length follows the material the reader needs.

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

## Indexes

Add every new article or note to `INDEX.md` under the matching topic section. Create a new section when the entry opens up a new topic area that will plausibly collect more than one piece over time. Mark the format (`**Article**` or `**Note**`) as a prefix in the index entry — topic drives navigation, format prefix sets reading expectations.

`README.md` surfaces major references in its Articles and Notes tables; update the matching table when shipping a major piece. `INDEX.md` remains the complete listing.

## Content boundaries

- Anthropic-authored documentation — belongs in `coroboros/archivist/docs/insights/`
- Internal SOPs, proprietary prompts, unsanitized strategy notes — belong in a private location, not in this public repo
- Runnable code and skills — `coroboros/agent-skills`

## Promoting content from a private source

Public promotion requires sanitized content: remove private system references, client names, and unattributed quotes; set `author: "Coroboros"`, the publication date, and complete `sources`. With authorization at the private origin, archive or remove the working version so it cannot compete with the published source. Preserve required provenance.
