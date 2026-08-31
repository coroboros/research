---
title: "Interaction Grammars per Page — One Mechanic per Class, One Easing Register"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "micro-interactions", "hover-states", "easing", "design-systems", "cta"]
sources:
  - "https://www.awwwards.com"
  - "https://www.awwwards.com/sites/cuberto"
  - "https://www.awwwards.com/sites/terminal-industries"
  - "https://www.awwwards.com/sites/lando-norris"
  - "https://www.awwwards.com/sites/siena-film-foundation"
  - "https://www.awwwards.com/sites/delvaux-digital-flagship-store"
  - "https://www.awwwards.com/sites/son-daven"
  - "https://www.awwwards.com/sites/exat-typeface"
  - "https://www.awwwards.com/sites/igloo-inc"
  - "https://www.awwwards.com/sites/cartier-watches-wonders-2025"
  - "https://www.awwwards.com/websites/sites_of_the_month/"
  - "https://www.awwwards.com/annual-awards/winners"
  - "https://tympanus.net/codrops/"
  - "https://www.nngroup.com/articles/button-states-communicate-interaction/"
  - "https://help.figma.com/hc/en-us/articles/20953528101783-Design-an-interactive-button-component"
  - "https://www.uxpin.com/studio/blog/button-states/"
  - "https://www.webgpu.com/showcase/cartier-watches-and-wonders-immersive-garden/"
---

# Interaction Grammars per Page — One Mechanic per Class, One Easing Register

Across six archetypes, twelve award-confirmed winners each carry one distinct mechanic per element class, and every mechanic resolves to one easing register. Scope: Awwwards Site of the Day (SOTD), Site of the Month (SOTM) and Site of the Year (SOTY) winners plus FWA and CSSDA, 2024–2026, drawn largely from live reads elsewhere in this corpus; four winners inferred from case studies.

**A "2–3 effect families max" ceiling is not evidenced and is slightly harmful:** it pushes toward cloning one mechanic across element classes, a recorded anti-pattern. The invariant winners satisfy is **one lineage, one distinct mechanic per element class**; family count is a consequence of class count (observed range 2–5, mode 4), not a target. Two adjacent intuitions are strongly evidenced: **one primary-CTA component**, and **a weak brighten+lift primary hover reads cheap**. No winner ships it, and it is precisely the mainstream product-UI default (NN/g, Figma, UXPin) that award juries score against.

Per-class *mechanics* are cited from the live stylesheet reads of the sibling reports ([`../winners/delvaux.md`](../winners/delvaux.md), [`../winners/son-daven.md`](../winners/son-daven.md), [`../winners/studio-unseen-benoist.md`](../winners/studio-unseen-benoist.md), [`../archetypes/bold-maximal.md`](../archetypes/bold-maximal.md), [`../archetypes/minimalist.md`](../archetypes/minimalist.md), [`../archetypes/editorial.md`](../archetypes/editorial.md), [`../archetypes/immersive-cinematic.md`](../archetypes/immersive-cinematic.md), [`../archetypes/corporate-luxury.md`](../archetypes/corporate-luxury.md), [`../archetypes/experimental.md`](../archetypes/experimental.md)) or from published Codrops and Awwwards case studies; award lines are taken from the Awwwards site pages and listings in `sources:`. Parent reference: [`../award-winning-websites-2025-2030.md`](../award-winning-websites-2025-2030.md).

## The twelve winners

Read from live CSS in the sibling reports: Cuberto (bold-maximal; SOTD 22 Jun 2018, 7.37), Terminal Industries (minimalist; SOTD 3 Sep 2025, 7.68, SOTM Sep 2025), Lando Norris (immersive; SOTD 17 Nov 2025, 8.18, Site of the Year 2025), Siena Film Foundation (editorial and immersive; SOTD 18 Mar 2025, 7.9, SOTM Mar 2025), Truekind Skincare (editorial; SOTD 29 Apr 2025, 7.47), Delvaux (corporate-luxury; Honorable Mention 15 Jun 2026), Son Daven (corporate-luxury; SOTD 5 Jun 2026, 7.62, SOTM Jun 2026), and Aristide Benoist (experimental; SOTD 24 Jun 2021, 8.01, the 2021 build). Read from case studies: Exat by Studio Size and RISE2 (editorial type; SOTD 3 Apr 2025, 7.73, CSSDA and FWA), Eloy Benoffi (bold-maximal and brutalist; Honorable Mention + GSAP SOTD + CSSDA), Igloo Inc (experimental; SOTD 23 Jul 2024, 7.92, Site of the Year 2024), and Cartier Watches & Wonders 2025 (immersive 3D; SOTD 18 Aug 2025, 7.64, SOTM Aug 2025). Sub-scores and the CSSDA and FWA legs are in the archetype reports.

Distinct hover/press families per winner, counted at per-class pointer granularity: Cuberto 4; Terminal 4–5; Lando ~4; Siena 4–5; Truekind 4–5; Delvaux 3–4; Son Daven 4–5; Benoist 2–3 (one slide idiom across loader, index, explore, and project); Exat ~2 hover mechanics (proximity glyph-weight field, style-name weight/width morph) plus scroll signatures, with a "Visit" link and no CTA hover documented; Eloy ~3 (location text-swap, card scale-storm, clone-storm CTA), the clone-storm CTA being one compound mechanic on a single instance. Igloo and Cartier expose no CSS families at all: one in-engine substrate carries every class (Igloo's SDF-offset scramble on UI text; Cartier's six (stated, webgpu.com) 3D scenes with hidden-gesture interactions). **Range and mode:** DOM-countable winners run **2–5 families, mode 4**. The range brackets the per-archetype channel bands counted across the nine archetype reports (3–4 for minimalist, editorial, and bento-card; 3–5 for brutalist; 4–5 for immersive, corporate-luxury, spatial-organic, bold-maximal, and experimental; [`../surfaces/interaction-channels.md`](../surfaces/interaction-channels.md)), with families here counted at the finer per-class granularity.

**Under every count, one lineage.** Cuberto: one expo-out family, `cubic-bezier(0.16,1,0.3,1)` with the sibling `cubic-bezier(0.19,1,0.22,1)` (11 and 8 uses in the live build). Delvaux: one easeOutQuart `cubic-bezier(0.25,1,0.5,1)`, byte-identical in the CSS var and the GSAP `CustomEase`. Terminal: one expo `cubic-bezier(.19,1,.22,1)` plus a named fade register. Lando: one bezier plus one accent meaning "active" everywhere.

## The invariants the corpus satisfies

Scope: minimalist, editorial, corporate-luxury, immersive, bold-maximal, experimental. Pure anti-design/brutalist relocates cohesion to the concept level (planned chaos as the unifying grammar) and is out of scope.

**1. Families per page: no numeric cap is evidenced; cohesion is the only invariant.** What is capped is the number of **lineages: exactly one.**

- Each element class present carries its **own** distinct mechanic, never one hover cloned across button *and* link *and* card *and* nav (flagged as an anti-pattern in every archetype report in scope).
- Every mechanic resolves to **one easing family and one gesture metaphor** from the site's declared motion system; a different easing per element class is likewise an anti-pattern.
- Testable on any site: enumerate the `:hover`/`:focus`/press mechanics; each element class present carries at least one distinct mechanic, and all `transition-timing-function` values and GSAP eases reduce to one bezier family plus at most one named second speed register for fades.

**2. Primary-CTA consistency: single treatment, full strength, product-default brightness absent.**

- The primary CTA carries **one** hover/press treatment, applied verbatim on every primary instance (Terminal, Lando, Siena, Truekind, Delvaux, Son Daven).
- That treatment is a full-strength committed mechanic (full-token flood + label/icon inversion, a masked label roll-swap, a directional token-wipe inversion, or a line/stroke draw) resolving state colors to full-strength design tokens.
- **Absent from every winner as the primary hover:** a bare brightness or lift (`filter:brightness()`, or a lone `translateY(-2px)`), and a pale low-opacity tint fill (`rgba(accent, <0.15)`). Both are the documented mainstream product-UI default. A pale wash is defensible only where the button starts transparent, a ghost or tertiary variant where the tint raises emphasis from nothing, never on a primary.
- Testable: the primary CTA hover paints a full-strength token (fill/invert/roll/draw), does not rely on `filter:brightness`, a lone `translateY`, or an `rgba(...,<0.15)` fill; every element in the primary role shares that identical rule.

**3. Peer buttons: one lineage, role-differentiated, never two unrelated grammars.** Equal-rank buttons share the mechanic. Different-rank buttons (primary vs secondary/ghost) differ **only** along an emphasis hierarchy, and both share the one easing lineage (Terminal token-wipe primary + 5% ghost wash; Truekind fill-invert + marquee variant; one bezier each). Not found on any winner: two unrelated grammars (different easing lineages or unrelated property signatures) on peer buttons. Testable: the secondary button's easing reduces to the same family as the primary's; the two differ in property or geometry mapped to a stated emphasis step, not in lineage.

**4. Nav responds (invariant); wordmark-on-hover is a floor (lower evidence tier).** Every interactive nav element responds to pointer and focus; coverage is total, and a nav link inert on hover is a fail, not restraint (Lando masked swap, Son Daven spotlight-dim, Terminal underline/dot). **Winner-verified.** The wordmark, as a home link, **should** carry the same quiet mark/word hover and focus response; an inert wordmark is a dead element in the first spot the eye checks. That rests on general interaction-design practice, *not* on clean winner verification, since several winners animate the logo on load (Flip into header) rather than on hover. It stays a lower-tier finding until computed-style reads on 3–4 live winners settle it.

## Refuted

- **"2–3 effect families max" as a ceiling.** Not evidenced on any winner; observed families run 2–5 (mode 4), and a numeric cap pushes toward cloning one mechanic across classes, the recorded anti-pattern.
- **Terminal Industries, SOTM Oct 2025.** The Awwwards listing carries Sep 2025, paired with SOTD 3 Sep 2025 at 7.68 ([`../archetypes/minimalist.md`](../archetypes/minimalist.md), [`../winners/site-of-the-year-contenders.md`](../winners/site-of-the-year-contenders.md)); the October label came from case-study prose.
- **Siena Film Foundation, SOTM Apr 2025.** The listing carries Mar 2025, paired with SOTD 18 Mar 2025 ([`../archetypes/editorial.md`](../archetypes/editorial.md#refuted)).
- **Truekind Skincare, a CSSDA leg.** No award record in this corpus carries one; SOTD 29 Apr 2025 (7.47) plus the Developer Award (7.85) are the confirmed legs ([`../archetypes/editorial.md`](../archetypes/editorial.md)).
- **Cartier Watches & Wonders 2025, SOTM Sep 2025.** The case study's label is a month off: SOTM Aug 2025 (listing), beside SOTD 18 Aug 2025 at 7.64 ([`../archetypes/corporate-luxury.md`](../archetypes/corporate-luxury.md#corpus)). The family counts are independent of the award lines.
- **Igloo's footer particle-coalesce on link hover.** Unsupported: the cited Awwwards case study describes no footer particle journey, only a previs animation and the links particle simulation ([`../archetypes/experimental.md`](../archetypes/experimental.md)), and Igloo ships no DOM footer at all, only a copyright line baked into the HUD ([`../archetypes/spatial-organic.md`](../archetypes/spatial-organic.md)). The in-engine substrate reading is unaffected.

**Counter-examples.**

- *Eloy Benoffi's primary CTA looks like multiple unrelated treatments.* It is not: it is one compound mechanic (spawn duplicates on mouse-move, blend-difference, staggered `back.in` exit), and a single-instance one-off, one maximalist hero button per page, never repeated UI ([`../archetypes/bold-maximal.md`](../archetypes/bold-maximal.md)). It refutes any naive "primary hover = one simple property transition": the invariant is one treatment per primary role, not one property.
- *Truekind runs two button mechanics*, fill-invert and kinetic marquee. The closest real stress on rule 3. It survives because both sit on one bezier and map to different button roles, but it proves winners are not limited to a single button mechanic. What is absent is two unrelated *lineages*, not two mechanics.
- *Brutalist/anti-design winners run "an excessive abundance of hover effects," every page its own style.* A genuine partial counter-example to "one lineage", but the sources insist the chaos is "planned," "intentional and purposeful." Cohesion moves up a level, which is why the finding is scoped out of anti-design.
- *Igloo, Cartier W&W, Lusion render interaction in-engine.* The "effect family" abstraction breaks: one shader/physics substrate, not N CSS families. A page can win with, in CSS terms, *zero* families. The finding is about coherence of whatever interaction layer exists, not a count of CSS hover rules.
- *Inert wordmark.* No documented winner with a provably inert wordmark was found, but the negative cannot be proven from search and no hover was driven. Several winners Flip the logo on load, which is not a hover response; such a site is plausibly a winner and would refute the wordmark floor. Hence its lower evidence tier.

**The inference gap: "winners do X" does not imply "X is required."** Survivorship bias is real: only winners were examined, never losers who also used one lineage, nor any winner who used several. Two things make the finding defensible as stated. First, it is a **universal negative across the examined corpus paired with a documented mass-baseline divergence**: the brighten+lift and pale-tint primary hover is absent across the examined winners yet is the *prescribed* product-UI default ([NN/g](https://www.nngroup.com/articles/button-states-communicate-interaction/) describes the hover state as "a slight darkening of the background color compared to the enabled state"; [Figma's component tutorial](https://help.figma.com/hc/en-us/articles/20953528101783-Design-an-interactive-button-component) swaps the fill to a lighter tint on hover; [UXPin's button-states guide](https://www.uxpin.com/studio/blog/button-states/) defines hover as the cue that a button is clickable). A corpus uniformly diverging from a documented default is stronger than winner-correlation alone; it explains why a reviewer reads such a build as cheap: it matched the default the award tier scores against (Creativity 20% + Design 40%). Second, the finding is stated as a coherence invariant the corpus satisfies, not a causal guarantee of winning.

The one brightness use anywhere in the corpus is Terminal's `brightness(1.05)` on a single number.

## Could not verify

**The method is the biggest hole.** No live CSS was read and no hover driven for this file. Every per-class mechanic is second-hand: the live-CSS reads cited above, or case-study prose relayed in compressed summary form. Case-study prose describes *intent*, not shipped `transition-timing-function` values, so the "one lineage" reads for Exat, Eloy, Igloo, and Cartier are inference, not measurement. Only the awards are first-hand-verified. Confirming these findings as invariants requires computed-style reads per element class on 3–4 live winners.

