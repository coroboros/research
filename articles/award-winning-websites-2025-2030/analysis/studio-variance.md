---
title: "Studio Variance — Section Order Can Repeat; the Device Kit and Content Archetype Never Do"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "studio-signature", "anti-template", "page-structure", "design-systems"]
sources:
  - "https://www.awwwards.com/about-evaluation/"
  - "https://www.awwwards.com/faqs/"
  - "https://www.awwwards.com/locomotive"
  - "https://www.awwwards.com/obys"
  - "https://www.awwwards.com/studiofreight"
  - "https://www.awwwards.com/unseenstudio"
  - "https://www.awwwards.com/AristideBenoist"
  - "https://tympanus.net/codrops/2026/03/06/obys-the-small-studio-designing-big-digital-narratives/"
  - "https://www.hontran.dev/blog/best-award-winning-websites-2026"
---

# Studio Variance — Section Order Can Repeat; the Device Kit and Content Archetype Never Do

Serial winners do not converge on one shared skeleton as a class — but one studio (Studio Freight) repeats its slot order across different-brand winners, so "same section order" alone is not a template smell. What no studio in the corpus ever does is repeat the *device kit* and the *content archetype* together across two brands. The repetition that wins sits below the skeleton (engineering, annotation grammar, type system); the layer that always rotates is the signature device, the close mechanism, and what the catalog *is*.

**Corpus:** 5 studios/authors, 21 award-linked artifacts — live HTML via curl, Wayback snapshots for dead or rebuilt builds, Awwwards profiles for award facts, read 2026-07-17. Claims for the four studios other than Locomotive are confirmed against raw HTML (last section).

Parent reference: [`../award-winning-websites-2025-2030.md`](../award-winning-websites-2025-2030.md).

## Variance table

Evidence class: **P** = live HTML · **A** = Wayback snapshot of the awarded build · **S** = secondary (Awwwards pages, case studies). Awards: **SOTD** = Site of the Day · **SOTM** = Site of the Month · **SOTY** = Site of the Year · **HM** = Honorable Mention.

### Locomotive (awwwards.com/locomotive — 91 SOTD, 4 SOTM, 1 SOTY)

| Site | Award | Skeleton (observed order) | Ev. |
|---|---|---|---|
| locomotive.ca/en | SOTM 03/2023 | shuffle-type h1 hero → featured work (5) → mission → about → articles (6) → culture (6 trips) → store (2) → footer | P |
| gkc.ca/en | SOTD 11/2025 | `c-hero-alpha` dark hero → featured projects (4 tiles) + stats → project push → clients listing (15 logos) → `c-scrolling-words` marquee → news (3) → `c-push-page` CTA ("Let's talk") → footer | P |
| aupalevodka.com/en | SOTD 03/2026 | 100dvh photo/video hero → philosophy → the-bottle (scroll-progress) → 3 product catalogs (vodka/seltzers/mocktails) → creators mosaic → `c-prefooter` motto ("Leave no trace") + newsletter → footer | P |
| lightshiprv.com | SOTD 01/2026 | product hero → AE.1 story sections → features → newsletter push → footer | P |
| dulcedo.com | SOTD 02/2026 | sr-only h1 + manifesto h2 → "Cast your profiles" 3-step task flow → "Get in touch" close | P |

**Repeats:** big-type h1-first hero; a pre-footer "push" slot on 3 of 5 (gkc.ca `c-push-page`, aupalevodka `c-prefooter`, lightshiprv newsletter push — locomotive.ca goes store-straight-to-footer and dulcedo closes on "Get in touch" with no footer); `data-scroll`/`data-scroll-css-progress` (Locomotive Scroll, their own library) on every site; identical `c-*`/`u-*` CSS architecture including the `\|\|` class-separator idiom (locomotive.ca and gkc.ca literally share it); sr-only heading discipline.
**Diverges:** everything between hero and footer — section roles, counts, and the close mechanism (talk-CTA / motto+newsletter / newsletter / get-in-touch) change per client archetype. pangrampangram.com (SOTY 2021) is now a generic Shopify theme — rebuilt since the award, excluded.

### Obys (awwwards.com/obys — SOTDs 2024–2026, Studio of the Year 2023)

| Site | Award | Skeleton | Ev. |
|---|---|---|---|
| obys.agency | SOTD 05/2026 | HUD header (Work · About · **live CET clock** · Contact) → WebGL canvas stage → numbered project index (two-digit counters running to 25 in source) → footer with Vertical/Horizontal/Grid view toggles | P |
| glyphic.bio | SOTD 11/2025 | kinetic type hero (ProSE™ ×3) → 3 numbered process steps → manifesto → caps process strip → about → careers index → big-type interstitial → contact form → **inverted dark footer** ("Designed by Obys") | P |
| library.obys.agency | SOTD 12/2025 | type manifesto → quotes (3) index → featured books → authors (6) monogram index → about-project → logo-transform footer | P |
| aim.obys.agency | SOTM 01/2024 | type hero ("AIM—" + Scroll to Explore) → about with `[*]` footnotes → featured gallery `[06]` → credit footer (Webflow build) | P |

**Repeats:** type-forward hero → manifesto → **enumerated index as primary body** → big-type footer, across custom, Next.js, and Webflow stacks. The enumerated index is the signature in four costumes (`01–19` rows / `01–03` steps / `(3)`+`(6)` / `E01–E05`+`[06]`).
**Diverges:** hero medium (WebGL on studio/tech sites, pure editorial type on content sites); close (contact-form + inverted footer **only on the commercial client**; all Obys-owned properties close self-referentially, no form).

### Studio Freight / Darkroom (awwwards.com/studiofreight — 16 SOTD, 29 HM) — the counterexample

| Site | Award | Skeleton | Ev. |
|---|---|---|---|
| scrib3.co | SOTD 04/2024 (7.55) | type mega-claim hero → logo marquee "(01)…(08)" → services → press-as-giant-type → cases index → team → footer with **contact form**, plus **342 `frame_corner` HUD brackets** (counted in source) | P |
| dragonfly.xyz (2022) | SOTD 09/2022 | hero → about (bilingual EN/中文) → research → team → portfolio → careers → footer, per-section theme flips | A |
| dragonfly.xyz (2026, "Dragonfly Redux") | HM 06/2026 | hero → **01 About → 02 Writing → 03 Team → 04 Portfolio → 05 Careers** → WebGL-totem pre-footer → glyph footer — **same slot order, 4 years later** (section ids/classes verified in live source) | P |
| lenis (2023 → lenis.dev) | SOTD 02/2023 | hero-manifesto → why-features → narrative pivot → solution → showcase → CTA footer; copy carried near-verbatim across the rebrand | A+P |
| hyperbolic.xyz | SOTD 05/2025 | type hero → testimonial-name marquee loop → services → why-grid → updates → jokey prefooter → footer with **newsletter form** | A |
| darkroom.engineering | studio site | wordmark hero → 300vh pinned showcase → testimonials → index tables (services/clients/tech/awards) → dated **Activity Log** → **inverted sticky reveal-under footer** | P |

**Repeats — this is the counterexample:** a stable macro order across *different brands* — typographic claim hero → social-proof/marquee band high → services → proof → updates/log slot → form-in-footer close. SCRIB3 and Hyperbolic (both SOTD, different brands, ~1 year apart) share roughly 5–6 of 7 slots by role. Dragonfly 2022→2026 preserves its section sequence in order. Lenis smooth scroll fingerprinted on every build.
**Diverges:** exactly one signature device per site, never reused — SCRIB3's frame corners, Hyperbolic's testimonial loop + sign-off, Redux's numbered indices + WebGL totem, darkroom's inverted sticky footer + Activity Log stay on their home sites. Form type flips (contact vs newsletter). The order-repeating Redux scored HM, not SOTD.

### Unseen Studio (awwwards.com/unseenstudio — 35 SOTD, 3 SOTM)

| Site | Award | Skeleton | Ev. |
|---|---|---|---|
| unseen.co | SOTM 02/2023 | audio-gated entry → numbered nav (01–04) → WebGL "world" drag hero → filterable Selected Projects index → "Say hello" contact close — **no `<footer>` element** | P |
| 2025.unseen.co | SOTD 03/2026 | **horizontal** 12-month story, bracketed data strips (`[US_01_25]`, `[SCROLL]`) → "Stay Tuned" end-card + `[Start a project with us]` + `[00%]` HUD | P |
| symphonyofvines.com | SOTD 08/2025 | fixed title card → 4 WebGL chapters with instruction lines → chapter-selector HUD → "The END" + credits + restart | P |
| blueyard.com | SOTD 05/2025 | manifesto-question hero → 4 thesis sections (mono kickers) → portfolio index table → team roster → back-to-top + "0…5 / 05" counter | P |
| 2025.oceanx.org | SOTD 02/2026 | fixed chapter menu → chapters 0–6 → "Share the Journey" close | P |

**Repeats:** the instrument panel — serial numbering/HUD counter or chapter selector on every site, mono/bracketed data strips, gated entries, contact-or-CTA-as-close, and a hard **zero-`<footer>` rule** (0 occurrences verified on unseen.co, blueyard.com, 2025.unseen.co).
**Diverges:** the skeleton itself — hub vs linear story vs thesis-landing vs horizontal timeline; no two of the five share a section order; scroll axis flips.

### Aristide Benoist (awwwards.com/AristideBenoist — 38 SOTD, 5 SOTM)

| Site | Award | Skeleton | Ev. |
|---|---|---|---|
| aristidebenoist.com | SOTD+SOTM 06/2021 | **no hero, no manifesto, no footer** — home IS a 30-row index, each row a data strip (`01/30` pagination + COMPLETED/TYPE/ROLE/CLIENT); about is an overlay state (verified via his own XHR endpoint returning the full DOM) | P |
| arocksworld.com | SOTD 05/2024 | film-gate hero ("PLAY THE FILM") → multi-route IA; the "footer" content lives in a menu route; DJ-set index tables with timestamps; 6AM→2AM timeline HUD | P |
| in-cognita-corp.com | SOTD 03/2025 (7.53) | single-route sectioned product page: numbered sections, horizontal gallery + pagination, multi-step Stripe funnel — structure grounded on code tokens | P |

**Repeats:** the machine — CSR shell + persistent WebGL canvas + terse id grammar + split-per-letter type + data-strip HUDs + overlay-based nav/contact + never a footer.
**Diverges:** the entire visible skeleton per subject; none of his three winners contains the standard hero → manifesto → catalog → contact marketing skeleton at all.

## Repetition that stays award-compatible

Three layers must repeat together before repetition reads as template: slot order, the device kit, and the content archetype. The limit case is two **different-brand** sites at the observed ceiling of order-repetition — ~6 of 7 slots by role, the top of the 5–6 Studio Freight ships — *and* sharing the device kit *and* sharing the content archetype down to the close mechanism. The corpus separates those three layers, and only the first has precedent.

- **Same slot order alone: precedented and award-compatible.** Studio Freight shipped near-identical slot orders across different brands (SCRIB3 2024 / Hyperbolic 2025, both SOTD) and across a 4-year rebuild (Dragonfly). An order-repeat by itself is not what juries can see — they judge one site at a time.
- **Same device kit: unprecedented in 21 artifacts.** Every serial winner rotates that layer. SCRIB3's 342 frame-corners appear on no other Studio Freight site; Obys re-costumes its enumerated index every time (`01–19` → `01/03` steps → `(3)/(6)` → `E01–E05`); Unseen rebuilds the chapter machine per brief; Locomotive rotates the close across its five sites (four distinct mechanisms, two newsletter-based). Each signature device in the corpus belongs to exactly one site — SCRIB3's frame corners, obys.agency's CET clock — not to a pair.
- **Same content archetype: the strongest signal.** Nowhere in the corpus does the same item-count-plus-content-pattern-plus-close-mechanism recur across two different brands. Even Obys, the most grammar-consistent studio, reserves the contact-form close for the client site only.

Repeating all three layers therefore reads as template, not studio signature — and the discriminating layer is the device kit and the content archetype, not the section order.

Jury-side evidence — published criteria, the pre-made-template eligibility rule, the absent juror quote — is consolidated in [`jury-evidence.md`](./jury-evidence.md). The corpus adds one fact that file cannot: serial winners never present that combination in the first place. Scoring is per-site by ≥18 jurors with no cross-submission mechanism (scores are private except to winners), so cross-site repetition would be caught only probabilistically.

## What varies, what holds

**Varies across every studio in the corpus** — holding any two constant across brands exceeds observed winner behavior.

1. **Content archetype of the body** — what the catalog/index *is* (products / projects / process steps / chapters / theses) and its item counts. Observed count-plus-archetype pairings never repeat: 5 featured works, 4 project tiles, 3 product catalogs, a 01–19+ index, (3)+(6) indexes, 4 WebGL chapters, 7 chapters, 30 rows, "(5)" — bare counts do recur (4, 3), the pairing does not.
2. **The signature device — exactly one per site, never reused.** The clearest law in the data: frame-corners, testimonial loop, WebGL totem, Activity Log, CET clock, view toggles, day-timeline each occur on exactly one site.
3. **Close mechanism** — contact form / newsletter / motto / "The END + restart" / share / sponsor CTA / view-toggle footer / no-footer overlay. Every studio rotates it inside its own winner set — Locomotive varies it per client archetype, Obys reserves the contact form for the client site.
4. **Hero medium + interaction** — WebGL world / kinetic type / editorial manifesto / photo-video / film gate / index-as-home; every studio varies this within its own winner set.
5. **Costume of the index/HUD** — the annotation *form* persists across a studio's sites; its rendering is re-dressed each time (brackets vs parentheses vs two-digit pagination vs monograms).
6. Weaker: **topology** (scroll axis, one-pager vs multi-route) — Unseen and Benoist rebuild it per brief; Studio Freight does not and still wins.

**Holds constant** — what serial winners demonstrably keep across 2–4+ years and different stacks.

- **Type system and typographic grammar** (split-letter titles, mono kickers, big-type h1-first).
- **Interaction vocabulary**: scroll library + easing (Lenis on every Studio Freight build; Locomotive Scroll on every Locomotive build), cursor system, entry-gate convention, load choreography.
- **Annotation grammar as a form**: that data strips, counters, and bracket footnotes exist at all (Unseen's `[…]`, Obys's `(n)`, Benoist's A/B/C/D rows) — content and costume rotate.
- **Engineering architecture**: CSS conventions (`c-*`/`u-*`, terse ids), CSR shell, sr-only heading discipline.
- **Macro slot presence** (hero-first, an index somewhere, a close-last) and a **footer philosophy** — studio-level constants juries read as signature. The two philosophies differ in strength: the Unseen and Benoist zero-`<footer>` rule holds on every site in their sets, three of them confirmed against raw HTML; Locomotive's prefooter-push-into-footer is a tendency, 3 of 5 rows.

## Could not verify

**Spot-checks against raw HTML:** obys.agency CET clock + Vertical/Horizontal toggles + numbered index — confirmed, one discrepancy (counters run to 25 in source, the initial read reported 01–19; device confirmed, exact project count ambiguous). glyphic.bio `HomeIntroSection` + "Get in Touch" + `bg-gray-900` dark footer + Obys credit — confirmed. scrib3.co section order (hero → logo-marquee → services → press → cases → team) and 342 `frame_corner` occurrences — confirmed. dragonfly.xyz live section order (hero → about → large-text → writing → team → portfolio → careers) — confirmed. Zero `<footer>` on unseen.co, blueyard.com, 2025.unseen.co — confirmed. aristidebenoist.com `?xhr=true` full-DOM endpoint with `01/30` gold pagination — confirmed. Awwwards FAQ template sentence — confirmed verbatim.

**Could not verify:** runtime motion (no browser execution — hero scrub/hover behavior inferred from markup attributes like `data-scroll-css-progress`, `h-[300vh] sticky`); bit-identity of live sites with awarded builds (hyperbolic.ai and pangrampangram.com are confirmed rebuilds, excluded or archive-sourced); studiofreight.com's own-site SOTD (absent from their verified profile list — the premise there is unconfirmed); "The Fabricant" attribution to Benoist (no evidence found); Hon Tran's jury membership (self-claimed); actual jury score effects and whether any juror ever sees both sites of a pair (scores private); the claim that Awwwards sells templates in a marketplace (no policy text found). Dead sites excluded rather than inferred: ferrumpipe.com (Plesk parking), deathchef.com (parked), epicurrence.com (unreachable).
