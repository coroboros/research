---
title: "Obys — Type-Forward Hero and an Enumerated Index on Every Site"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "studio-skeleton", "page-structure", "obys", "webgl", "typography", "editorial-design", "webflow"]
sources:
  - "https://www.awwwards.com/obys/"
  - "https://www.awwwards.com/sites/obys-2"
  - "https://web.archive.org/web/20260413204638id_/https://www.awwwards.com/annual-awards-2023/studio-of-the-year"
  - "https://obys.agency"
  - "https://glyphic.bio"
  - "https://library.obys.agency"
  - "https://aim.obys.agency"
---

# Obys — Type-Forward Hero and an Enumerated Index on Every Site

Two things hold across all four Obys-built winners: every site opens type-forward, and every site carries an enumerated index, the studio's true signature. The hero medium and the close change per brief, and the rest of the grammar holds unevenly. Section-order read of four live award winners, taken from server-rendered markup, as structural evidence behind the archetypes. Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

## Sites inspected

All four fetched **live** via `curl -sL` on 17 Jul 2026 (server-rendered HTML), cross-checked against the [Awwwards profile](https://www.awwwards.com/obys/) for award facts: 42 Sites of the Day, 2 Sites of the Month, 33 Honorable Mentions, plus Studio of the Year 2023 on the [archived Annual Awards 2023 page](https://web.archive.org/web/20260413204638id_/https://www.awwwards.com/annual-awards-2023/studio-of-the-year). Skeleton and content claims are grounded in the `<section>`/`<header>`/`<footer>` markup and text order extracted; motion, cursor, and grain claims are lower-confidence because these are JS-heavy SPAs and much runs at runtime (flagged where relevant).

| Site | URL | Award | Evidence | Tech (from markup) |
|---|---|---|---|---|
| **Obys Agency** (studio site) | obys.agency | Site of the Day (SOTD) 4 May 2026, 7.46 (Design 7.56 / Usability 7.04 / Creativity 7.71 / Content 7.75) + Developer Award 7.98 ([award page](https://www.awwwards.com/sites/obys-2)) | Live HTML, 90 KB | Custom; `<canvas id="gl">` WebGL |
| **Glyphic Biotechnologies** | glyphic.bio | SOTD 27 Nov 2025 + Developer Award (per the profile) | Live HTML, 225 KB | Next.js (`_next/*` chunks) |
| **Obys' Design Books** | library.obys.agency | SOTD 17 Dec 2025 + Developer Award (per the profile) | Live HTML, 75 KB | Custom; GSAP/ScrollTrigger refs, `<canvas>` |
| **AIM — AI Modernism of Kharkiv** | aim.obys.agency | **Site of the Month (SOTM) Jan 2024** + No-code Honors (per the profile) | Live HTML, 71 KB | **Webflow** (`data-w-id`, `w-mod`) |

Ferrumpipe.com resolved to a Plesk Obsidian hosting-parking page (`<div id="plesk-root">`, `<title>Plesk Obsidian 18.0.77`): **dead, excluded.**

The first three are near-consecutive 2025–2026 winners on the same custom/React stack; AIM is an older 2024 Webflow no-code piece, a deliberate contrast case.

## Per-site skeletons

### Obys Agency — obys.agency (studio portfolio)
**Ordered slots** (from `<main>` text order):
1. **HUD header**: `Work · About · CET 00:00 AM · Contact` (live-time readout is a persistent device)
2. **WebGL stage**: `<canvas id="gl">` full-viewport, driving hero + hover media
3. **Project index / catalog**: one long numbered list; the logical rows run **01→19**, while the raw HTML carries two-digit counters running to **25**. The device is confirmed, the exact project count is not: the name list repeats 3× in source (marquee/duplicated rows for the scroll device), so counters and logical rows do not correspond one-to-one. Each row = project name + client category (Architecture, Fashion, Technology…) + discipline tags (`Creative Direction, Web Design/Dev, 3D`).
4. **Footer**: layout-mode toggles `Vertical, / Horizontal, / Grid` + `All rights reserved. ©2026 Obys`

- **Hero pattern:** WebGL/`canvas`-driven, type + hover-media index; not a photo or scrub-video hero. Load-in + scroll-scrub inferred (bundled JS).
- **Close pattern:** big-type/utility footer with view-mode switches, **not** a contact form.
- **Devices:** live CET clock (HUD readout), numbered index catalog, view-mode toggles, WebGL canvas, custom cursor (weak signal in static HTML).

### Glyphic Biotechnologies — glyphic.bio
**Ordered slots** (from `data-component` + `<section>` order):
1. **Hero**: `<section data-component="HomeIntroSection">` h=110vh: `Protein Sequencing by Expansion (ProSE™)` repeated 3× (kinetic type) + subline
2. **Product / "Introducing ProSE™"**: 3 numbered process steps: `Sample Preparation → Molecular Expansion → Amino Acid Sequencing`
3. **Manifesto statement**: "…spatial expansion… discrimination of all 20 amino acids"
4. **Process strip**: 3-col caps grid: `SAMPLE PREPARATION / MOLECULAR EXPANSION / AMINO ACID SEQUENCING`
5. **About / company**: "Glyphic Biotechnologies… Since 2021… Founded in Berkeley"
6. **Careers**: open-positions index (job title · location · dept · salary rows)
7. **Big-type interstitial**: "The next great chapter of scientific discovery will be written in ProSE™"
8. **Contact**: address + email + **application/newsletter form** ("Get in Touch! … I accept the Terms of Use")
9. **Inverted footer**: dark (`bg-gray-900`) mail-list signup + sitemap + `Designed by Obys` + `©2026`

- **Hero:** type-first kinetic (repeated headline), WebGL canvas present; scroll-scrub through the process steps.
- **Close:** contact form → **inverted (dark) big footer**. This is the clearest "contact-close + inverted footer" of the set.
- **Devices:** numbered process index, all-caps data strip, sticky/pinned process animation (`data-progress-text` on headings), inverted footer, canvas.

### Obys' Design Books — library.obys.agency
**Ordered slots:**
1. **Header**: `About · Books · Credits · Contacts` + Menu/Close overlay
2. **Manifesto/about**: "Obys' Design Books — a personal selection… design in ways the screen never could" + contacts inline
3. **Quotes (3)**: index-table of typographer quotes (Ruder, Müller-Brockmann, Airey) + **Featured Books** list (title · author · year)
4. **Featured Authors (6)**: initials-monogram index: `ER · JMB · DA · MV · JA · MB` + "Top 6 Best Printhouses"
5. **About Project (3)**: closing manifesto: "not a library about design — it's a library for designers"
6. **Footer**: `data-animation="logo-transform"` scroll-pinned logo transform, `info@obys.agency ©2025`

- **Hero:** type-only editorial manifesto (no photo/WebGL hero, though `<canvas>` refs exist for book renders).
- **Close:** manifesto + logo-transform footer, **not** a form.
- **Devices:** parenthetical counters `(3) (6)` as index device, monogram author index, quote tables, scroll-driven logo-transform footer.

### AIM — aim.obys.agency
**Ordered slots** (Webflow `id="Home-*"`):
1. **Nav**: `AI Modernism of Kharkiv [Ukraine] · Index · Experiment · About · [Gallery] · Obys Agency ©2025 · Menu`, with a **modernists index** in the drawer: `E01: Anatol Petrytskiy … E05: Vadym Meller`
2. **Hero**: `id="Home-hero"`: `AIM— / AI Modernism / Of Kharkiv` + `Scroll to Explore`
3. **About**: `id="Home-about"`: "This AI experiment … Kharkiv Modernism [*]… 1910 to 1930" with `[*] [**] [***]` footnote markers
4. **Big-image / featured gallery**: `Kharkiv Modernism × Obys × AI · [06] Featured:` with named AI works (`Suprematista, Buntesglas, Vierensee…`)
5. **Footer**: "An AI Experiment Based on the Kharkiv Modernism · Obys Agency ©2023"

- **Hero:** big type-only ("AIM—"), `Scroll to Explore` prompt; Webflow-driven, no WebGL canvas in markup.
- **Close:** big-type credit footer, **not** a form.
- **Devices:** `E01–E05` enumerated index, `[*] [**] [***]` footnote/coordinate markers, `[06] Featured` bracket-numbering, section-triggered nav.

## Pairwise comparison

### Obys ↔ Glyphic (both 2026/2025 custom+WebGL SOTD)
| Slot / device | Obys | Glyphic | Verdict |
|---|---|---|---|
| Persistent nav header | Work/About/Contact + **live clock** | logo + theme header | **Changed** (HUD clock is studio-only) |
| Hero medium | WebGL type/hover index | kinetic repeated type + canvas | **Same family** (type-first + canvas) |
| Core body | project **index 01–19** | **process index** + careers index | **Same device, different content** (numbered index catalog) |
| Data strip | discipline tags per row | all-caps 3-col process strip | **Same** (caps data strip) |
| Close | view-toggle utility footer | **contact form + inverted footer** | **Changed** |

### Glyphic ↔ Library (consecutive Nov/Dec 2025 SOTD)
| Slot / device | Glyphic | Library | Verdict |
|---|---|---|---|
| Hero | kinetic type + canvas | editorial type manifesto | **Changed** (product vs editorial) |
| Manifesto slot | yes (statement section) | yes (about + about-project) | **Same** (manifesto bookends) |
| Index device | process + careers rows | quotes(3) + authors(6) + books | **Same** (list/index-table as primary body) |
| Counter device | numbered steps `01/02/03` | parenthetical `(3) (6)` | **Same family** |
| Close | inverted dark footer + form | logo-transform light footer | **Changed** |

### Library ↔ AIM (custom 2025 vs Webflow 2024)
| Slot / device | Library | AIM | Verdict |
|---|---|---|---|
| Enumerated index | authors `ER/JMB/…`, `(6)` | modernists `E01–E05`, `[06]` | **Same device** (labeled enumerated index) |
| Bracket/footnote marks | `(3)` counters | `[*] [**] [***]`, `[Gallery]` | **Same family** (bracket annotation) |
| Hero | type manifesto | type "AIM—" + Scroll to Explore | **Same** (type-only hero) |
| About slot | About Project | Home-about | **Same** |
| Close | logo-transform footer | big-type credit footer | **Same** (type footer, no form) |
| Tech | custom/GSAP | Webflow no-code | **Changed** |

## What holds

Obys repeats a skeletal grammar (type-forward hero → manifesto or about statement → an enumerated index or catalog as the primary body device → a big-type footer close) and varies the medium and the close per brief, regardless of stack (custom, Next.js, Webflow) and year (2024–2026): a reusable system, not a copied template. Two parts are universal, every site opening type-forward and every site carrying an enumerated index (`01–19` project rows on obys.agency, `01/02/03` process steps on glyphic.bio, `(3)`/`(6)` quote-and-author tables on library, `E01–E05` + `[06]` on AIM), while the other two hold 3 of 4 with the misses on different sites: obys.agency ships no manifesto or about-statement slot at all (HUD header → WebGL stage → project index → footer), and glyphic.bio closes on a contact form plus an inverted dark utility footer rather than a big-type one. What varies is the hero medium, WebGL canvas on the two studio/tech sites and pure editorial type on the two content sites, and the close, since only Glyphic (a commercial client) ends on a **contact form + inverted dark footer** while the three Obys-owned properties close on a self-referential big-type/utility footer with **no form**.

## Could not verify

- **Motion, scroll-scrub, custom cursor, grain/noise:** these run in bundled/runtime JS. Static HTML showed a `<canvas>`/cursor hint but no GSAP on obys.agency (bundled) and no grain layer anywhere. No browser execution was used, so live scroll behavior, cursor, and grain went unobserved; hero *interaction* (load-in vs scrub) is inferred, not observed.
- **Award dates and types for Glyphic, Library, and AIM** rely on the Awwwards profile; only obys.agency's own award page was opened.
- **Ferrumpipe, Shalom, Sad Book, WG24, drama-tickets, Way of the Web**: not inspected. Ferrumpipe is dead (Plesk parking); the others are not among the live URLs resolvable from the profile.
- **Full section count on obys.agency:** the WebGL index duplicates its row list 3× in source (marquee), so both readings of the catalog are reported, the 01–19 logical count and the counters running to 25 in raw HTML, rather than a single reconciled figure. A rendered read of the index would settle it.
