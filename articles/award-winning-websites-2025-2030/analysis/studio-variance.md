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
  - "https://www.awwwards.com/sites/obys-2"
  - "https://www.awwwards.com/studiofreight"
  - "https://www.awwwards.com/unseenstudio"
  - "https://www.awwwards.com/AristideBenoist"
  - "https://tympanus.net/codrops/2026/03/06/obys-the-small-studio-designing-big-digital-narratives/"
  - "https://www.hontran.dev/blog/best-award-winning-websites-2026"
---

# Studio Variance — Section Order Can Repeat; the Device Kit and Content Archetype Never Do

Serial winners do not converge on one shared skeleton as a class, but one studio (Studio Freight) repeats its slot order across different-brand winners, so "same section order" alone is not a template smell. What no studio in the corpus ever does is repeat the *device kit* and the *content archetype* together across two brands. The repetition that wins sits below the skeleton (engineering, annotation grammar, type system); the layer that always rotates is the signature device, the close mechanism, and what the catalog *is*.

**Corpus:** 5 studios/authors, 21 award-linked artifacts: live HTML via curl, Wayback snapshots for dead or rebuilt builds, Awwwards profiles for award facts, read 17 Jul 2026. Claims for the four studios other than Locomotive are confirmed against raw HTML, and their per-site skeletons are quoted from markup in [`../winners/studio-obys.md`](../winners/studio-obys.md), [`../winners/studio-freight-darkroom.md`](../winners/studio-freight-darkroom.md), and [`../winners/studio-unseen-benoist.md`](../winners/studio-unseen-benoist.md); Locomotive's skeletons live only here.

Parent reference: [`../award-winning-websites-2025-2030.md`](../award-winning-websites-2025-2030.md).

## Variance table

Evidence class: **P** = live HTML · **A** = Wayback snapshot of the awarded build · **S** = secondary (Awwwards pages, case studies). Awards: **SOTD** = Site of the Day · **SOTM** = Site of the Month · **SOTY** = Site of the Year · **HM** = Honorable Mention.

### Locomotive (awwwards.com/locomotive — 91 SOTD, 4 SOTM, 1 SOTY)

| Site | Award | Skeleton (observed order) | Ev. |
|---|---|---|---|
| locomotive.ca/en | SOTM Mar 2023 | shuffle-type h1 hero → featured work (5) → mission → about → articles (6) → culture (6 trips) → store (2) → footer | P |
| gkc.ca/en | SOTD Nov 2025 | `c-hero-alpha` dark hero → featured projects (4 tiles) + stats → project push → clients listing (15 logos) → `c-scrolling-words` marquee → news (3) → `c-push-page` CTA ("Let's talk") → footer | P |
| aupalevodka.com/en | SOTD Mar 2026 | 100dvh photo/video hero → philosophy → the-bottle (scroll-progress) → 3 product catalogs (vodka/seltzers/mocktails) → creators mosaic → `c-prefooter` motto ("Leave no trace") + newsletter → footer | P |
| lightshiprv.com | SOTD Jan 2026 | product hero → AE.1 story sections → features → newsletter push → footer | P |
| dulcedo.com | SOTD Feb 2026 | sr-only h1 + manifesto h2 → "Cast your profiles" 3-step task flow → "Get in touch" close | P |

**Repeats:** big-type h1-first hero; a pre-footer "push" slot on 3 of 5 (gkc.ca `c-push-page`, aupalevodka `c-prefooter`, lightshiprv newsletter push; locomotive.ca goes store-straight-to-footer and dulcedo closes on "Get in touch" with no footer); `data-scroll`/`data-scroll-css-progress` (Locomotive Scroll, their own library) on every site; identical `c-*`/`u-*` CSS architecture including the `\|\|` class-separator idiom (locomotive.ca and gkc.ca literally share it); sr-only heading discipline.
**Diverges:** everything between hero and footer: section roles, counts, and the close mechanism (talk-CTA / motto+newsletter / newsletter / get-in-touch) change per client archetype. pangrampangram.com (SOTY 2021) is now a generic Shopify theme, rebuilt since the award, excluded.

### The four studios read in their own reports

| Studio (Awwwards profile) | Sites (award; evidence) | Repeats | Diverges | Per-site skeletons |
|---|---|---|---|---|
| **Obys** (awwwards.com/obys: Studio of the Year 2023; SOTD 2024–2026) | obys.agency (SOTD 4 May 2026, 7.46, Developer Award 7.98; P) · glyphic.bio (SOTD 27 Nov 2025; P) · library.obys.agency (SOTD 17 Dec 2025; P) · aim.obys.agency (SOTM Jan 2024; P) | type-forward hero → manifesto → **enumerated index as primary body** → big-type footer, across custom, Next.js, and Webflow stacks; the index is the signature in four costumes (`01–19` rows / `01–03` steps / `(3)`+`(6)` / `E01–E05`+`[06]`); HUD header with a live CET clock and Vertical/Horizontal/Grid view toggles on obys.agency | hero medium (WebGL on studio and tech sites, pure editorial type on content sites); close (contact form + inverted dark footer "Designed by Obys" **only on the commercial client**; every Obys-owned property closes self-referentially, no form) | [`studio-obys.md`](../winners/studio-obys.md) |
| **Studio Freight / Darkroom** (awwwards.com/studiofreight: 16 SOTD, 29 HM), the counterexample | scrib3.co (SOTD 29 Apr 2024, 7.55; P) · dragonfly.xyz (SOTD 19 Sep 2022; A) · dragonfly.xyz "Dragonfly Redux" (HM 19 Jun 2026; P) · lenis, now lenis.dev (SOTD 2 Feb 2023; A+P) · hyperbolic.xyz (SOTD 14 May 2025; A) · darkroom.engineering (studio site; P) | a stable macro order across *different brands*: typographic claim hero → social-proof/marquee band high → services → proof → updates/log slot → form-in-footer close. SCRIB3 and Hyperbolic (both SOTD, different brands, ~1 year apart) share roughly 5–6 of 7 slots by role; Dragonfly 2022→2026 keeps its section sequence in order (**01 About → 02 Writing → 03 Team → 04 Portfolio → 05 Careers**, section ids verified in live source); Lenis smooth scroll fingerprinted on every build; Lenis copy carried near-verbatim across the rebrand | exactly one signature device per site, never reused: SCRIB3's **342 `frame_corner` HUD brackets** (counted in source), Hyperbolic's testimonial-name marquee loop + jokey pre-footer, Redux's numbered indices + WebGL-totem pre-footer, darkroom's inverted sticky reveal-under footer + dated Activity Log. Form type flips (contact vs newsletter); Dragonfly 2022 flips theme per section, bilingual EN/中文. The order-repeating Redux scored HM, not SOTD | [`studio-freight-darkroom.md`](../winners/studio-freight-darkroom.md) |
| **Unseen Studio** (awwwards.com/unseenstudio: 35 SOTD, 3 SOTM) | unseen.co (SOTM Feb 2023; P) · 2025.unseen.co (SOTD Mar 2026; P) · symphonyofvines.com (SOTD Aug 2025; P) · blueyard.com (SOTD May 2025; P) · 2025.oceanx.org (SOTD Feb 2026; P) | the instrument panel: serial numbering, HUD counter, or chapter selector on every site (numbered nav 01–04, `[US_01_25]`, `[SCROLL]`, `[00%]`, "0…5 / 05" counter, fixed chapter menu), mono/bracketed data strips, gated entries (audio-gated on unseen.co), contact-or-CTA-as-close ("Say hello"; "Stay Tuned" + `[Start a project with us]`; "The END" + credits + restart; "Share the Journey"), and a hard **zero-`<footer>` rule** (0 occurrences verified on unseen.co, blueyard.com, 2025.unseen.co) | the skeleton itself: hub (WebGL drag world + filterable Selected Projects index) vs 4 WebGL chapters with instruction lines vs manifesto-question landing with 4 thesis sections and a portfolio index table vs chapters 0–6 vs a **horizontal** 12-month story; no two of the five share a section order; scroll axis flips | [`studio-unseen-benoist.md`](../winners/studio-unseen-benoist.md) |
| **Aristide Benoist** (awwwards.com/AristideBenoist: 38 SOTD, 5 SOTM) | aristidebenoist.com (SOTD + SOTM Jun 2021; P) · arocksworld.com (SOTD May 2024; P) · in-cognita-corp.com (SOTD Mar 2025, 7.53; P) | the machine: CSR shell + persistent WebGL canvas + terse id grammar + split-per-letter type + data-strip HUDs (`01/30` pagination + COMPLETED/TYPE/ROLE/CLIENT rows; DJ-set index tables with timestamps and a 6AM→2AM timeline HUD) + overlay-based nav/contact (about is an overlay state, verified via his own XHR endpoint returning the full DOM) + never a footer | the entire visible skeleton per subject: home *is* a 30-row index with no hero, manifesto, or footer; a film-gate hero ("PLAY THE FILM") → multi-route IA with the footer content in a menu route; a single-route numbered product page with a horizontal gallery + pagination and a multi-step Stripe funnel. None of the three contains the standard hero → manifesto → catalog → contact skeleton at all | [`studio-unseen-benoist.md`](../winners/studio-unseen-benoist.md) |

Raw-HTML spot-checks, all confirmed:

| Site | Confirmed in source |
|---|---|
| obys.agency | CET clock, Vertical/Horizontal toggles, numbered index |
| glyphic.bio | `HomeIntroSection`, "Get in Touch", `bg-gray-900` dark footer, the Obys credit |
| scrib3.co | section order hero → logo-marquee → services → press → cases → team; 342 `frame_corner` occurrences |
| dragonfly.xyz | live section order hero → about → large-text → writing → team → portfolio → careers |
| unseen.co, blueyard.com, 2025.unseen.co | zero `<footer>` |
| aristidebenoist.com | `?xhr=true` full-DOM endpoint with `01/30` gold pagination |
| awwwards.com/faqs | the template sentence, verbatim |

## Repetition that stays award-compatible

Three layers must repeat together before repetition reads as template: slot order, the device kit, and the content archetype. The limit case is two **different-brand** sites at the observed ceiling of order-repetition (~6 of 7 slots by role, the top of the 5–6 Studio Freight ships) *and* sharing the device kit *and* sharing the content archetype down to the close mechanism. The corpus separates those three layers, and only the first has precedent.

- **Same slot order alone: precedented and award-compatible.** Studio Freight shipped near-identical slot orders across different brands (SCRIB3 2024 / Hyperbolic 2025, both SOTD) and across a 4-year rebuild (Dragonfly). An order-repeat by itself is not what juries can see; they judge one site at a time.
- **Same device kit: unprecedented in 21 artifacts.** Every serial winner rotates that layer. SCRIB3's 342 frame-corners appear on no other Studio Freight site; Obys re-costumes its enumerated index every time (`01–19` → `01/03` steps → `(3)/(6)` → `E01–E05`); Unseen rebuilds the chapter machine per brief; Locomotive rotates the close across its five sites (four distinct mechanisms, two newsletter-based). Each signature device in the corpus belongs to exactly one site (SCRIB3's frame corners, obys.agency's CET clock), not to a pair.
- **Same content archetype: the strongest signal.** Nowhere in the corpus does the same item-count-plus-content-pattern-plus-close-mechanism recur across two different brands. Even Obys, the most grammar-consistent studio, reserves the contact-form close for the client site only.

Repeating all three layers therefore reads as template, not studio signature, and the discriminating layer is the device kit and the content archetype, not the section order.

Jury-side evidence (published criteria, the pre-made-template eligibility rule, the absent juror quote) is consolidated in [`jury-evidence.md`](./jury-evidence.md). The corpus adds one fact that file cannot: serial winners never present that combination in the first place. Scoring is per-site by ≥18 jurors with no cross-submission mechanism (scores are private except to winners), so cross-site repetition would be caught only probabilistically.

## What varies, what holds

**Varies across every studio in the corpus.** Holding any two constant across brands exceeds observed winner behavior.

1. **Content archetype of the body**: what the catalog/index *is* (products / projects / process steps / chapters / theses) and its item counts. Observed count-plus-archetype pairings never repeat: 5 featured works, 4 project tiles, 3 product catalogs, a 01–19+ index, (3)+(6) indexes, 4 WebGL chapters, 7 chapters, 30 rows, "(5)". Bare counts do recur (4, 3); the pairing does not.
2. **The signature device, exactly one per site, never reused.** The clearest law in the data: frame-corners, testimonial loop, WebGL totem, Activity Log, CET clock, view toggles, day-timeline each occur on exactly one site.
3. **Close mechanism**: contact form / newsletter / motto / "The END + restart" / share / sponsor CTA / view-toggle footer / no-footer overlay. Every studio rotates it inside its own winner set; Locomotive varies it per client archetype, Obys reserves the contact form for the client site.
4. **Hero medium + interaction**: WebGL world / kinetic type / editorial manifesto / photo-video / film gate / index-as-home; every studio varies this within its own winner set.
5. **Costume of the index/HUD**: the annotation *form* persists across a studio's sites; its rendering is re-dressed each time (brackets vs parentheses vs two-digit pagination vs monograms).
6. Weaker: **topology** (scroll axis, one-pager vs multi-route). Unseen and Benoist rebuild it per brief; Studio Freight does not and still wins.

**Holds constant.** What serial winners demonstrably keep across 2–4+ years and different stacks.

- **Type system and typographic grammar** (split-letter titles, mono kickers, big-type h1-first).
- **Interaction vocabulary**: scroll library + easing (Lenis on every Studio Freight build; Locomotive Scroll on every Locomotive build), cursor system, entry-gate convention, load choreography.
- **Annotation grammar as a form**: that data strips, counters, and bracket footnotes exist at all (Unseen's `[…]`, Obys's `(n)`, Benoist's A/B/C/D rows); content and costume rotate.
- **Engineering architecture**: CSS conventions (`c-*`/`u-*`, terse ids), CSR shell, sr-only heading discipline.
- **Macro slot presence** (hero-first, an index somewhere, a close-last) and a **footer philosophy**, studio-level constants juries read as signature. The two philosophies differ in strength: the Unseen and Benoist zero-`<footer>` rule holds on every site in their sets, three of them confirmed against raw HTML; Locomotive's prefooter-push-into-footer is a tendency, 3 of 5 rows.

## Could not verify

obys.agency's project count: the index counters run to 25 in source against the `01–19` rows carried in the table above; the device is confirmed, the count is ambiguous.

Not verified: runtime motion (no browser execution; hero scrub/hover behavior inferred from markup attributes like `data-scroll-css-progress`, `h-[300vh] sticky`); bit-identity of live sites with awarded builds (hyperbolic.ai and pangrampangram.com are confirmed rebuilds, excluded or archive-sourced); studiofreight.com's own-site SOTD (absent from their verified profile list, so the premise there is unconfirmed); "The Fabricant" attribution to Benoist (no evidence found); Hon Tran's jury membership (self-claimed); actual jury score effects and whether any juror ever sees both sites of a pair (scores private); the claim that Awwwards sells templates in a marketplace (no policy text found). Dead sites excluded rather than inferred: ferrumpipe.com (Plesk parking), deathchef.com (parked), epicurrence.com (unreachable).
