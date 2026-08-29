---
title: "Composition Chains — 21 Section Sequences by Archetype"
date: "2026-07-30"
author: "Coroboros"
tags: ["design-archetypes", "page-structure", "macrostructure", "composition", "motion-design", "webgl", "awwwards"]
sources:
  - "https://www.awwwards.com/sites/siena-film-foundation"
  - "https://www.anthropic.com"
  - "https://www.awwwards.com/sites/truekind-skincare"
  - "https://www.awwwards.com/sites/terminal-industries"
  - "https://www.cssdesignawards.com/sites/terminal-industries/47847/"
  - "https://www.awwwards.com/sites/gabriel-contassot"
  - "https://www.awwwards.com/sites/stefan-vitasovic-portfolio25"
  - "https://www.awwwards.com/sites/delvaux-digital-flagship-store"
  - "https://www.awwwards.com/sites/son-daven"
  - "https://www.awwwards.com/sites/depo-luxe"
  - "https://www.awwwards.com/sites/lando-norris"
  - "https://www.awwwards.com/annual-awards/winners"
  - "https://www.awwwards.com/sites/lusion-v3"
  - "https://www.awwwards.com/sites/anime-js"
  - "https://www.awwwards.com/sites/endex"
  - "https://www.awwwards.com/sites/exat-typeface"
  - "https://www.awwwards.com/sites/cuberto"
  - "https://www.awwwards.com/sites/ponpon-mania"
  - "https://www.awwwards.com/sites/flowfest-2025"
  - "https://www.awwwards.com/sites/eloyb-design"
  - "https://www.awwwards.com/sites/treize-grammes"
  - "https://www.awwwards.com/sites/brunos-portfolio"
  - "https://www.awwwards.com/sites/igloo-inc"
  - "https://www.awwwards.com/sites/aristide-portfolio-2021"
  - "https://www.awwwards.com/sites/obys-2"
  - "https://www.awwwards.com/sites/cyd-stumpel-portfolio-2025"
  - "https://www.awwwards.com/websites/sites_of_the_month/"
  - "https://siena.film/"
---

# Composition Chains — 21 Section Sequences by Archetype

Eight hero-fold forms across the winners carry no filled CTA at all, and beyond the numeric counter curtain six loader patterns appear once each. The 21 entries cover 23 award-winning sites plus Anthropic as a brand control, not a winner: one ordered section list per entry, with its pacing curve and its loader decision, grouped by archetype. A site that two archetype reports carry (Siena, Lusion, Igloo, the Aristide Benoist / Obys pair) appears once. Archetype labels extend the parent reference's eight archetypes with a ninth, spatial-organic: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

Notation: `role (section form) [intensity]`, intensity being this file's comparative estimate of attention load on a 1–10 scale (the sibling reports describe pacing qualitatively), with `climax` marking a chain's attention peak. Each entry opens with its award line, cited to the award page, and an evidence tag: `(winner-verified)` = the section order was read from the live page in a sibling report of this corpus; `(shipped)` = the live shell was read and the in-engine sequence comes from the case study; `(design-canonical)` = a reference build with no award. Site of the Month (SOTM) membership is read from the [monthly listing](https://www.awwwards.com/websites/sites_of_the_month/).

## Editorial

**Siena Film Foundation (gated-reel).** Awwwards Site of the Day (SOTD) 18 Mar 2025, 7.9, SOTM Mar 2025 ([award page](https://www.awwwards.com/sites/siena-film-foundation)); carried by the editorial and immersive-cinematic reports `(winner-verified)`. threshold (entry gate) [8] → masthead (hero-masthead, media back) [9, climax] → reel (pinned-filmstrip) [8] → detail (editorial-split, media left) [6] → close (close-panel) [6]. Footer bare-cue / costumed-credits: "©2024. SIENA FILM FOUNDATION." is a `.copyright-menu-text` line at the foot of the menu overlay, after the COOKIE / TERMS / PRIVACY list, and the served [homepage](https://siena.film/) carries no `<footer>` element and no oversized wordmark. No separate loader: the held, clickable gate is the arrival, an opaque black fixed panel of its own (`.preloader-w`), not a scrim over the reel, doubling as loader and sound gate. Gate and masthead stack the attention climax up front; the filmstrip sustains proof; rest at the per-work detail before a thin credits close, a designed refusal since the body already spent the spectacle. Fits a film foundation, festival, or cinema archive in a dark poster grade with a ritual-of-entry gate, a treated-still archive, and operable film stills.

**Anthropic (standfirst-stack), brand control, not a winner.** No jury award in this window; live HTML and CSS read as the light-register control `(design-canonical)` ([anthropic.com](https://www.anthropic.com)). masthead (hero-masthead, no media) [6] → belief-index (index-reel-header + index-list) [5] → release-cards (card-list) [6] → mission-close (close-panel) [6]. Footer tabular-index; no loader (instant paint, verified absence). Even intensity, no spectacle peak: the chrome carries the voice, and rest is inherent to the reading cadence. Fits an institution or research org, reading-first, voice-in-the-chrome, no spectacle.

**Truekind Skincare (maison-scroll).** Awwwards SOTD 29 Apr 2025, 7.47, Developer Award 7.85 ([award page](https://www.awwwards.com/sites/truekind-skincare)) `(winner-verified)`. hero (hero-masthead, media back, align start) [7] → value-chapters (editorial-split ×n, media alternating) [6] → product-index (index-reel-header + index-list) [6] → journal-teaser (card-list) [4] → connect (close-panel) [6]. Footer contact-first (social grid, house tagline); loader is a progress-tracked full-screen `.preloader` (`100dvh`, `inset:0`, `z-index:9999`, driven by `$sstatePreloadProgress` / `$sstatePreloadDone` in the bundle, see [`../surfaces/preloaders.md`](../surfaces/preloaders.md)). Even intensity through the value chapters, since the maison refuses a spike; rest at the journal teaser before the connect close. Fits warm editorial commerce, skincare, or a maison where commerce hides behind Discover and restraint is the register.

## Minimalist

**Terminal Industries (argument-scroll).** Awwwards SOTD 3 Sep 2025, 7.68, SOTM Sep 2025; CSSDA Website of the Day 4 Aug 2025, 8.42 ([award page](https://www.awwwards.com/sites/terminal-industries), [CSSDA page](https://www.cssdesignawards.com/sites/terminal-industries/47847/)) `(winner-verified)`. hero (hero-masthead, media back, align start) [8] → logo-strip (logo-wall) [4] → stat-band [5] → mechanism-reveal (type-as-image) [9, climax] → benefits (editorial-split ×3) [5] → quote (editorial-split, media left) [6] → close (close-panel) [6]. Footer oversized-wordmark, where the `<h1>` lives, a sticky reveal over a 50vh holder; loader is a numeric counter curtain recoloring into the footer's dark green. One mid-page climax at the mechanism reveal; the void gap is the rest; the footer is a second quiet peak, the `<h1>` landing last. Fits a product or SaaS site with one held promise argued beat by beat.

**Gabriel Contassot, Stefan Vitasović (gallery-stack).** Contassot: Awwwards SOTD 14 Apr 2024, 7.34 ([award page](https://www.awwwards.com/sites/gabriel-contassot)); Vitasović: Awwwards SOTD 20 Sep 2025, 7.25, Developer Award 8.04 ([award page](https://www.awwwards.com/sites/stefan-vitasovic-portfolio25)) `(winner-verified)`. name-card [6] → project-stack (full-bleed-figure ×n, one per viewport) [8, climax]. Footer bare-cue ("SCROLL UP" / "2025."); loader is a bare 1→100 counter, no curtain. The hero holds no image; the first full-bleed still below the fold is the reward and the climax; intensity holds flat-high through the stack; the close is a bare cue. Fits a minimalist portfolio where the work is the whole argument and the hero is a text-only name card.

## Corporate Luxury

**Delvaux (maison-scroll).** Awwwards Honorable Mention 15 Jun 2026, no jury score displayed ([award page](https://www.awwwards.com/sites/delvaux-digital-flagship-store)) `(winner-verified)`. hero (hero-masthead, media back) [7] → swiper (swiper-strip) [5] → emblematic-product (editorial-split, media left) [6]. Footer tabular-index (newsletter + accordion nav + house tagline); no loader (instant paint, winner-verified absence). No climax spike, since restraint is the register; even intensity; the tabular footer is close and rest at once. Fits a heritage maison or luxury commerce where commerce hides behind Discover and even, restrained intensity is the point.

**Son Daven (argument-scroll).** Awwwards SOTD 5 Jun 2026, 7.62, Developer Award 8.09, SOTM Jun 2026 ([award page](https://www.awwwards.com/sites/son-daven)) `(winner-verified)`. hero (hero-masthead, media back) [8] → prologue (editorial-split, media right) [5] → place-tour [7] → financials (stat-band) [6] → legend-close (close-panel) [9, climax]. Footer contact-first (sales departments by city); loader is a flip handoff, the master preloader scene Flipping the logo into the header. 15+ sections; the late "Become part of the legend" buy-moment fuses climax and close; place tour and financials build proof; rest at the contact footer. Fits an investment, real-estate, or heritage venture with a long argued scroll and a join-the-legend close.

**Depo Luxe (engine-world).** Awwwards SOTD 7 Jul 2026, 7.62, Developer Award 7.53 ([award page](https://www.awwwards.com/sites/depo-luxe)) `(winner-verified)`. hero (in-engine-hero) [8] → nav-index (index-reel-header + index-list) [6]. Footer oversized-wordmark, signed "All work © DEPO LUXE, 2026"; loader is an SVG logo path fill into a dissolve, no hard cut. The WebGL field is the ground, not a spike; the index's spotlight-dim carries the middle; the signed wordmark footer is the quiet rest-close. Requires a WebGL runtime. Fits a luxury creative folio wanting a living WebGL ground under a spotlight-dim index.

## Immersive Cinematic

**Lando Norris (portrait-procession).** Awwwards SOTD 17 Nov 2025, 8.18; Site of the Year 2025 and Site of the Year Users' Choice 2025 on the [annual winners page](https://www.awwwards.com/annual-awards/winners) ([award page](https://www.awwwards.com/sites/lando-norris)) `(winner-verified)`. portrait-hero (hero-masthead, media back, align start) [9] → pinned-gallery (pinned-filmstrip) [8] → on-off-split (editorial-split) [6] → helmet-gallery (webgl-scene) [9, climax] → honors-partners (logo-wall + stat-band) [7] → valediction (valediction-footer) [9, climax]. Footer valediction-fold: the valediction footer is the footer, and the palette flips light→dark once; loader assembles a brand object, then an ellipse wipe reveals and the loader node unmounts. Climax doubled, at the mid-page 3D helmet gallery and the inverted valediction close; short bridge rests between facet chapters. Requires a WebGL runtime. Fits a personality, athlete, or ambassador site with a hero portrait, a 3D signature object, and a cinematic inverted close.

**Lusion v3 (studio-reel).** Awwwards SOTD 2 Oct 2023, 8.25, Site of the Year 2023 and Developer Site of the Year 2023; CSSDA Website of the Year 2023; FWA of the Year 2023 ([award page](https://www.awwwards.com/sites/lusion-v3)); carried by the immersive-cinematic report, its copy by the experimental report `(winner-verified)`. hero (in-engine-hero) [8] → manifesto (type-as-image) [6] → reel (index-reel-header + index-list) [7] → contact-close (close-panel) [7]. Footer contact-first (Let's talk + Bristol address + socials + newsletter); no loader (scroll cue + scene settle, winner-verified). Even-high intensity carried by the live 3D ground; the manifesto is the one understanding beat; contact-first close. The live-3D hero requires a WebGL runtime. Fits a 3D or interactive studio wanting a live-rendered ground under a manifesto and a discipline-tagged reel.

## Bento / Card

**Anime.js v4 (specimen-tour).** Awwwards SOTD 6 May 2025, 7.62, Developer Award 7.84, SOTM May 2025 ([award page](https://www.awwwards.com/sites/anime-js)) `(winner-verified)`. hero (hero-masthead, media right) [8] → toolbox-grid (feature-card-grid) [7] → demo-panels (pinned-demo-panels) [9, climax] → modules-bento (feature-card-grid) [6] → sponsors (logo-wall) [4] → get-started (close-panel) [6]. Footer tabular-index, product variant (sponsor-first block, instant fill-swipe hovers, newsletter); no preloader at all: the hero stagger is the entrance, and a 0→100 counter curtain is an anti-signal here. One climax at the pinned demo panels; sponsors are the rest before the get-started close; the footer adds a designed fill-swipe cue, not spectacle. Fits a developer tool, library, or API product where the artifact demonstrates itself, one capability per pinned panel.

**Endex (capability-grid).** Awwwards Honorable Mention 24 Mar 2025, 7.91 ([award page](https://www.awwwards.com/sites/endex)) `(winner-verified)`. hero (hero-masthead, no media) [7] → capability-strip (divided-strip) [5] → feature-grid (feature-card-grid, 12-col, product-UI slices) [7] → cta-close (close-panel) [6]. Footer compact tabular-index, or an oversized-wordmark reprise as Linear ships it `(design-canonical)`; no loader: SSR paints copy pre-hydration, and a 0→100 counter curtain is an anti-signal. Climax is diffuse, the 12-col feature grid carrying the proof; even build to a single CTA close; the compact footer is the rest. Fits a SaaS, AI, or enterprise product needing feature cards that carry real product UI in an editorial 12-col grid, the bento-fatigue correction.

## Bold Maximal

**Exat (specimen-tour).** Awwwards SOTD 3 Apr 2025, 7.73; CSSDA Website of the Day 25 Mar 2025 and Website of the Month Mar 2025; FWA of the Day 20 Mar 2025 ([award page](https://www.awwwards.com/sites/exat-typeface)) `(winner-verified)`. hero (type-as-image) [8] → about (editorial-split, no media) [5] → type-tester [6] → specimen-grid [9, climax] → capability-sections (editorial-split ×n) [6] → close (close-panel) [6]. Footer CTA-reprise ("Get Exat →" + credits); no loader: the glyph grid is the intro. Climax at the specimen glyph grid; capability sections quiet after; CTA reprise close; the proximity recolor is the signature, driven by cursor rather than scroll. Fits a type foundry or typography product where the specimen performs itself and type is the image.

**Cuberto (argument-scroll).** Awwwards SOTD 22 Jun 2018, 7.37, Developer Award 7.62 ([award page](https://www.awwwards.com/sites/cuberto)) `(winner-verified)`; the argument-scroll ordering recurs in Terminal, Son Daven, and FlowFest. hero (hero-masthead, no media, align start) [7] → featured-projects (full-bleed-figure ×n) [9, climax] → services (editorial-split) [5] → blog (card-list) [4] → close (close-panel) [6]. Footer contact-first ("Have an idea?" → Tell us + dual real addresses); loader is a `cb-loader` white-fill curtain, fixed and `display:none` post-load, so it ran and dismissed, and the same panel doubles as the SPA route cover ([`../surfaces/navigation-and-hover.md`](../surfaces/navigation-and-hover.md), [`../surfaces/route-transitions.md`](../surfaces/route-transitions.md)). Climax early at the featured projects (proof); services then blog quiet the page as rest; the "Have an idea?" reprise closes. Fits a digital agency or studio with a declarative pitch hero and work-as-proof up front.

**Ponpon Mania (chapter-world).** Awwwards SOTD 22 Oct 2025, 7.64, Developer Award 7.72, SOTM Oct 2025 ([award page](https://www.awwwards.com/sites/ponpon-mania)) `(winner-verified)`. cover (chapter-cover) [9] → chapter-select [6] → chapter-scenes (webgl-scene) [9, climax] → about (editorial-split) [4]. Footer bare-cue (minimal legal chrome); loader is a narrative first scene: "read now" hands the live cover into the reader. The cover is scene one, with no separate hero; climax at the chaptered panel scenes with camera moves and physics; About is the rest and close; scroll is a playhead, so replays differ. Requires a WebGL runtime. Fits a story brand, comic, or exhibition where the page is a chaptered world you operate.

## Brutalist

**FlowFest 2025 (argument-scroll).** Awwwards SOTD 29 Jul 2025, 7.36 ([award page](https://www.awwwards.com/sites/flowfest-2025)) `(winner-verified)`. hero (type-as-image, drawn SVG-path H1 slab) [8] → what-is (editorial-split) [5] → lineup (lineup-grid) [9, climax] → what-to-expect (editorial-split) [5] → community-band (logo-wall) [6] → faq (faq-accordion) [4] → invitation-close (close-panel) [7]. Footer CTA-reprise, an oversized invitation: "See you there!" + newsletter + reprised Buy Tickets + flanking illustrations; loader is a chat cloud with typing beats and a stepped counter, in character. Climax around 40% at the lineup (proof); the FAQ is the rest before the oversized invitation close; no zero-intro instant paint, since the loader speaks in character. Fits an event, festival, or conference with a lineup-as-proof and a warm-communal in-character voice.

**Eloy Benoffi, Treize Grammes (studio-index).** Benoffi: Awwwards Honorable Mention 4 Jul 2025, plus GSAP Site of the Day and CSSDA honors ([award page](https://www.awwwards.com/sites/eloyb-design)); Treize Grammes: Awwwards Honorable Mention 11 Oct 2024 ([award page](https://www.awwwards.com/sites/treize-grammes)) `(winner-verified)`. identity-hero (identity-terminal-hero) [7] → about (editorial-split) [5] → work-index (index-reel-header + index-list) [7] → footer-finale (footer-spectacle, clone machine) [9, climax]. Footer footer-spectacle, the Eloy clone machine, so the loudest interaction lands last; loader turns progress into UI, the loading bar growing into the navbar. Peak at the bottom, the footer-as-finale being the climax; even build through identity hero, about, and the hover-charged work index; no in-fold CTA. Fits a brutalist or terminal studio index where the footer is the spectacle finale and the work index carries the proof.

## Experimental

**Bruno Simon (engine-world).** Awwwards SOTD 21 Jan 2026, 8.11, Developer Award, SOTM Jan 2026, for the 2025 rebuild read here; the 2019 build holds SOTD 11 Nov 2019, 8.04 ([award page](https://www.awwwards.com/sites/brunos-portfolio)) `(winner-verified)`. world-boot [8] → free-roam (webgl-scene) [9, climax] → sign-off (in-world) [5]. Footer is an in-world sign-off with no DOM footer, "Thank you for visiting my portfolio! — Bruno"; loader is the start gate, doubling as the sound gate, over a diegetic asset-gated ratio: `.global-progress .ratio` climbs with the real load, recolors to `#d5ff95` on completion, and prints the elapsed time ([`../surfaces/preloaders.md`](../surfaces/preloaders.md)). No scroll, since funnel jobs collapse into the 3D space; understanding arrives in ten seconds via "click to start"; the world is the climax; an in-world sign-off closes. Requires a WebGL runtime. Fits a creative-developer portfolio or playable brand world where the engine is the page and discovery is the proof.

**Aristide Benoist, Obys (type-index).** Benoist: Awwwards SOTD 24 Jun 2021, 8.01, SOTM Jun 2021 ([award page](https://www.awwwards.com/sites/aristide-portfolio-2021)); Obys: Awwwards SOTD 4 May 2026, 7.46, Developer Award 7.98 ([award page](https://www.awwwards.com/sites/obys-2)); carried by the experimental and spatial-organic reports `(winner-verified)`, the Obys loader excepted. counter-boot (corner-counter-boot) [7] → type-index (type-index-grid, no hero headline) [8] → route-morph (webgl-scene) [9, climax] → about-overlay (about-overlay-footer) [5]. Footer tabular-index, carried by the About overlay on Benoist's site (clients wall + awards tally, typeset) and by a statement + email + © block with socials, clients wall, and awards tally on Obys's; loader is a corner 0→100 counter booting straight into the index on Benoist's site, while Obys's own entrance runs in bundled JS and is unverified ([`./studio-obys.md`](./studio-obys.md)). No marketing hero: the giant-type index over WebGL is the page, proof-by-density; climax is on click, at the route morph; the About overlay doubles as close and footer, and Obys's view toggle is within-page, with no route curtain. Requires a WebGL runtime. Fits a developer or designer folio, studio, or agency index where a giant-type index over WebGL is the whole page and a click plays an in-engine route morph.

## Spatial Organic

**Igloo Inc (engine-world).** Awwwards SOTD 23 Jul 2024, 7.92, Site of the Year 2024 and Developer Site of the Year 2024 ([award page](https://www.awwwards.com/sites/igloo-inc)); carried by the spatial-organic and experimental reports `(shipped)`: live shell read, in-engine sequence from the case study. in-engine-fold (in-engine-hud-fold) [8] → zones (webgl-scene, scroll-scrubbed, one per project) [8] → scrub-assembly and particle-sim (webgl-scene) [10, climax]. Footer is an in-world sign-off, "// Copyright © 2026 Igloo, Inc." in the HUD, no DOM footer; no loader and no boundary: the intro flows into the scene, HUD from frame one, no loader DOM. Attention and understanding fuse in the engine; the scroll-assembled igloo's dark entrance and the late interactive particle sim are the climax; rest is ambient drift, or a generative or contact close; `scrollHeight` pins at roughly one viewport. Requires a WebGL runtime. Fits a fully in-engine, zero-text-node brand world scrubbed by scroll: one shader-seamed continuous scene, one zone per project, a single real-time simulation as the whole page.

**Cyd Stumpel (studio-reel).** Awwwards SOTD 9 Mar 2025, 7.22, Developer Award 7.74 ([award page](https://www.awwwards.com/sites/cyd-stumpel-portfolio-2025)) `(winner-verified)`. marquee-hero [9, climax] → role-band (type-as-image) [5] → morph-tile-grid [7] → blogs (card-list) [4] → services (editorial-split) [5] → contact-footer (close-panel) [6]. Footer contact-first: project prompt, availability, copy-email pill, offset shadow on the red accent, clip-path edge; no loader (instant paint plus animation-timeline reveals, no 0→100 gate). Climax at the fold, on the marquee hero; the morph-tile grid carries proof; blogs are the rest before services and the contact-first close; View Transitions drive shared-element morphs on route. Fits a warm-organic solo or studio portfolio: real portrait on organic clip-path shapes, morph-tile work grid, availability-as-fact copy.

## Section forms across the 21 chains

Ranked by recurrence. The no-CTA hero folds are the fold forms that carry no filled CTA at all.

| Section form | Class | Chains | What it is | Where |
|---|---|---|---|---|
| `index-list` | high recurrence | 5 | the row-list body under an index or reel header | Anthropic belief index, Lusion reel, Depo nav-index, Truekind product index, Eloy work index |
| `logo-wall` | high recurrence | 4 | restrained proof strip of client, partner, or sponsor logos | Terminal, Anime.js, Lando honors, FlowFest community |
| `card-list` | high recurrence | 4 | release, journal, or blog card list | Anthropic, Truekind, Cyd, Cuberto |
| `feature-card-grid` | high recurrence | 3 | bento or 12-col grid of cards carrying real product-UI slices; spans vary | Endex, Anime.js toolbox + modules |
| `stat-band` | high recurrence | 3 | standalone big-number strip | Terminal odometer, Anime.js bundle-KB, Son Daven financials |
| `full-bleed-figure` | high recurrence | 2 | one full-bleed project or still per viewport, masked reveal plus caption | gallery-stack, Cuberto projects |
| `name-card` | no-CTA hero fold | 1 | text-only hero: oversized name, role line, scroll cue | Contassot, Vitasović |
| `in-engine-hero` | no-CTA hero fold | 3 | statement or H1 over a live 3D field, scroll cue, no filled CTA | Lusion, Depo, Igloo |
| `in-engine-hud-fold` / `in-engine-intro` | no-CTA hero fold | 1 | live-scene fold with monospace HUD corners from frame ~0, zero text nodes | Igloo |
| `identity-terminal-hero` | no-CTA hero fold | 1 | corner identity tags, diff/scramble swaps, forced-open scramble nav | Eloy |
| `marquee-hero` | no-CTA hero fold | 1 | repeating-wordmark strip, portrait on an organic clip-path shape, serif role headline | Cyd |
| `type-index-grid` | no-CTA hero fold | 1 | giant-type project index over WebGL imagery, no marketing hero, no prose | Aristide, Obys |
| `corner-counter-boot` | no-CTA hero fold | 1 | corner 0→100 counter that boots straight into the index (digit `translate3d(-110%)` exit) | Aristide |
| `chapter-cover` | no-CTA hero fold | 1 | wordmark, entry CTA, and chapter nav over a live canvas; the cover is scene one | Ponpon |
| `swiper-strip` | lower recurrence | 1 | triple-image / campaign-frame carousel, hand-driven | Delvaux |
| `faq-accordion` | lower recurrence | 2 | FAQ or accordion rest band | FlowFest, Delvaux |
| `lineup-grid` | lower recurrence | 1 | event lineup or name grid as proof | FlowFest |
| `chapter-select` | lower recurrence | 1 | chapter nav or index | Ponpon; Mat Voyce outside these chains |
| `place-tour` | lower recurrence | 1 | landmark reveals plus walk-time counters, a distance map explored rather than reeled | Son Daven |
| `morph-tile-grid` | lower recurrence | 1 | work tiles, border-radius morph plus crossfade on hover | Cyd |
| `type-tester` | lower recurrence | 1 | interactive glyph or type input specimen | Exat |
| `specimen-grid` | lower recurrence | 1 | glyph specimen grid with proximity-ring reactions, the climax band | Exat |
| `pinned-demo-panels` | lower recurrence | 2 | pinned 100lvh panels, copy cross-fading over a persistent live demo | Anime.js, Exat |
| `divided-strip` | lower recurrence | 1 | divide-x capability strip, marquee on mobile | Endex |
| `about-overlay-footer` | lower recurrence | 1 | About overlay doubling as the footer: clients wall plus awards tally, typeset | Aristide |
| `world-boot` | lower recurrence | 1 | WebGL world plus start gate, no DOM `<h1>`, landmarks-as-nav | Bruno |

## Loader patterns beyond the numeric counter curtain

Six appear once each across the 21 chains.

| Pattern | Mechanism | Chain |
|---|---|---|
| Flip handoff | the preloader scene Flips a logo into the header (GSAP Flip) | Son Daven |
| SVG path fill | SVG logo path fills, then dissolves, with no hard cut | Depo Luxe |
| Brand-object assembly | a brand object assembles, then an ellipse or clip wipe reveals; the loader node fully unmounts | Lando |
| Narrative first scene | "read now" hands the live cover into the reader | Ponpon |
| Chat cloud | chat-cloud typing beats plus a stepped counter, in character | FlowFest |
| Progress-becomes-UI | the loading bar grows into the navbar | Eloy |

## Refuted

- **Siena's footer as an oversized wordmark**: the served homepage has no `<footer>` and no wordmark element; the credits line is `.copyright-menu-text` at the foot of the menu overlay, so the footer is bare-cue / costumed-credits, as [`../archetypes/immersive-cinematic.md`](../archetypes/immersive-cinematic.md) also records.
- **Exo Ape as an `in-engine-hero` example**: [`../archetypes/spatial-organic.md`](../archetypes/spatial-organic.md) reads its hero as a full-bleed photograph with intro and XXL display type, eight `<video>` elements and no `<canvas>`, so it is dropped from that row.
