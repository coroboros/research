---
title: "Interaction Channels on Winners — The Six Channels, One Idea Restated Across Surfaces"
date: "2026-07-30"
author: "Coroboros"
tags: ["interaction-design", "motion-design", "micro-interactions", "design-archetypes", "scroll-driven-animation", "gsap", "awwwards", "signature-design"]
sources:
  - "https://flowfest.co.uk"
  - "https://eloyb.design"
  - "https://cuberto.com"
  - "https://ponpon-mania.com"
  - "https://matvoyce.tv"
  - "https://exat.hottype.co"
  - "https://lusion.co"
  - "https://aristidebenoist.com"
  - "https://bruno-simon.com"
  - "https://terminal-industries.com"
  - "https://landonorris.com"
  - "https://animejs.com"
  - "https://www.delvaux.com"
---

# Interaction Channels on Winners — The Six Channels, One Idea Restated Across Surfaces

Winners run three to five distinct interaction **channels**, band varying by archetype, restate one idea in three or more transformed forms across loader, nav, body, and footer, and commit a scroll texture that carries the eye down the page. A page that responds to every input but commits to none of the three still reads as inert. Channel inventories below are counted across the nine archetype reports in this corpus; archetypes and their canonical winners live in [the parent reference](../award-winning-websites-2025-2030.md).

**Channel taxonomy.** **C1** per-class hover and tap · **C2** display-type text effects · **C3** cursor identity · **C4** idle and ambient life · **C5** scroll textures (marquee, parallax, scrubbed accent, pinned scrub) · **C6** replayable signature mechanic.

---

## Channel inventory by archetype

### Brutalist — band 3–5

| Winner | C1 | C2 | C3 | C4 | C5 | C6 | Count |
|---|---|---|---|---|---|---|---|
| FlowFest (winner-verified) | hard-shadow press button, underline-draw link, ±3° card tilt with sticker peel | SVG-drawn H1 whose spans stagger in, chat-cloud typed text (TextPlugin) | default | 4 rainbow arches draw over ~3s (stated, unconfirmed by the CSS read), chat mascot idle | photo shuffle carousel | chat-cloud → hero reveal | 5 |
| Eloy (winner-verified / technique) | clone CTA | char-diff swap (TextPlugin `type:"diff"`), scramble nav, RGB-split type | bitmap swap `url(cursor.svg)` | forced-open scramble nav | — | clone-machine footer (≤200 clones, `back.in(1.7)`) | 5 |
| Naked City (technique) | color-dim link, CRT-dissolve figure | RGB-split type | OS default (browser-blue anchors) | — | CRT shader video autoplay on hover | CRT thumbnail dissolve | 4 |
| Joffrey (technique) | — | `steps(14)` counter | — | — | vertical case slider scale-up, Flip morph | counter → Flip showreel | 3 |

Cursor identity appears in only one of six brutalist winners, as a bitmap swap, and no brutalist winner ships the lerped follower ([brutalist](../archetypes/brutalist.md)). C3 is genuinely optional here.

### Bold-maximal — band 4–5

| Winner | C1 | C2 | C3 | C5 / C6 | Count |
|---|---|---|---|---|---|
| Cuberto (winner-verified) | dome-fill CTA, 7° skew text-roll links, scaling underline | SplitText headline | contextual-state follower (`mouse-follower`, `::before` rescales per target, `stickDelta: 0.15`) | — | 4 |
| Ponpon (winner-verified) | in-canvas physics shoves | SplitText elastic-skew headline | — | scroll-as-playhead WebGL, chaptered physics reader | 4 |
| Mat Voyce (winner-verified) | — | per-letter kinetic roll on every nav item, label, and social link (DOM-doubled `WWoorrkk`) | — | oversized type beyond the viewport, kinetic-type spectacle | 3 |
| Exat (winner-verified / technique) | — | 3D X-axis type rotation | proximity glyph grid, cursor-distance weight | proximity glyph grid | 4 |

Bold-maximal licenses the bespoke contextual cursor — the differentiator against brutalist and minimalist — and runs pervasive kinetic type on *every* label rather than one hero moment.

### Experimental — band 4–5

| Winner | Signature channels | Count |
|---|---|---|
| Igloo (shipped / case study) | C1 WebGL scramble and flowmap buttons · C2 SDF-offset scramble text · C4 ambient snow drift plus a live node-graph animating values · C5 scroll scrubs a real-time simulation as the igloo assembles · C6 links run a particle sim, one model per link | 5 |
| Lusion (winner-verified copy) | C1 magnetic pull with label-follow · C2 SplitText · C3 magnetic elastic follower · C5 scroll over 3D · C6 reel | 5 |
| Aristide (winner-verified) | C2 scramble-decode plus TNY counter · C3 `.e` explore indicator, no lag-dot · C5 sliced-filmstrip scrub with ruler-tick scrubber · C6 click-into-project morph, 30 per-color variants | 4 |
| Bruno Simon (winner-verified copy) | C3 deliberate no-cursor, the car is the pointer · C4 physics-world idle plus whispers · C6 drive-and-discover · a sound layer | 3+ |

Here C3 is the default — a magnetic follower, or a justified no-cursor — and C4 idle is strong.

### The standard archetypes

| Archetype | Band | Committed channels | Cursor (C3) | Idle (C4) |
|---|---|---|---|---|
| **Minimalist** | 3–4 | C1 hairline underline, contained low-amplitude figure zoom · C2 per-char masked reveal, odometer recolor, two-layer label roll, scramble/decode · C5 masked and inverse-scale figure reveals, canvas frame-sequence photo · C6 curtain → odometer recolor → char cascade as one seamless move | none (system cursor, canon) | minimal, ~1 |
| **Editorial** | 3–4 | C1 kinetic-marquee-label button, variable-font axis morph (`opsz`) · C2 two-layer label roll, scroll emphasis-fill, semantic accent · C5 floating-product parallax, hold-and-drag filmstrip, WebGL displacement · C6 product-color flood, focus-defocus | default, but one that does work (lens unblur, glyph weight) | thin |
| **Immersive-cinematic** | 4–5 | C1 magnetic pull, accent-swap face · C2 masked-line reveal, split-color valediction · C5 pinned horizontal-track interlude, `ellipse()` seams · C6 palette-flip valediction, ticket admission, delivery world · sound | a Cuberto-class follower when earned | Rive idle (35 Rive plus 21 canvas), audio, status card |
| **Corporate-luxury** | 4–5 | C1 roll-swap doubled-label CTA, stroke-draw, spotlight-dim siblings · C2 SplitText masked lines (`power4.inOut`, `yPercent 250→0`) · C5 clip-path figure reveal, `data-scroll-displace` footage, swipers · C6 six-universe gesture reveal, place tour, AI dialogue | scoped `cursor: none` over WebGL, magnetic on a circular CTA, or none | bespoke soundscape or sound toggle |
| **Bento-card** | 3–4 | C1 ghost-button transform, footer colored-fill swipe (`transition-duration: 0s`) · C2 headline char-stagger, red-dot period loop, word-swap loop, command-input typewriter · C5 pinned `100lvh` demo panels cross-fade, lag-based grid scroll · C6 a live demo proves each heading (drag or scrub) | native, powers `--x`/`--y` border-shine | perpetual micro-loops (red dot, clockwork counter) |
| **Spatial-organic** | 4–5 | C1 radius-morph figure, accent-displacement button, underline link · C2 wordmark marquee, cycling role headlines, kinetic condensed type · C4 ambient DNA (orbs drifting 15–25s, snow drift, node graph, CET clock, procedural noise) · C5 marquee `overflow-x`, WebGL scroll scrub · C6 scroll-assembled igloo, work-thumb-to-page morph, music-synced type | follower (Exo Ape), system (Cyd), or in-engine (Igloo) | strong — the ambient *is* the DNA |

---

## The echo pattern

The continuous signature is **a single idea restated across surfaces**, not an emblem tracking scroll.

- **Aristide** (winner-verified) — the TNY display face and the `translate3d(-110%,0,0)` slide idiom recur as the loader counter (`#load` digits exit at `-110%`), the giant index title in the same face, the `.e` explore indicator (revealing at `translate3d(0,-110%,0)`), and the per-project click-morph. One face, one slide, transformed across every surface.
- **Terminal Industries** (winner-verified) — the odometer recolor `light-gray → lime → dark-green` at load pre-states the palette; the same recolor re-fires mid-page on stat counters; the final dark-green *is* the footer ground and the lime *is* the CTA. One recolor mechanic, loader through footer.
- **Mat Voyce** (winner-verified) — the per-letter kinetic roll runs identically on nav, section labels, and the footer social row (`IINNSSTTAAGGRRAAMM`). Navigation itself is the animation, hero to footer.
- **Cuberto** (winner-verified) — dome-fill CTA, 7° skew-roll, scaling underline, and contextual cursor are visibly different mechanics all riding one expo-out curve, `cubic-bezier(0.16,1,0.3,1)`. The grammar is the through-line.
- **Igloo and Ponpon** — one substrate (Igloo's ice-and-chromatic shader; Ponpon's "scroll is a playhead, nav is a track list" metaphor) renders loader, buttons, text, and transitions as transformed forms of one world.
- **Lando** (winner-verified) — the hero portrait on cream inverts in the footer to the same subject, the helmet, on dark. The palette flips light to dark exactly once, bookending, and the `ellipse(100% 120% at 50% 0%)` clip recurs site-wide as the seam.

---

## Standing affordances

How a signature invites its gesture at rest, before any input.

- **Eloy** — a forced-open scramble nav. **Ponpon** — a "read now" pill. **Bruno** — a hand-drawn "click to start" plus a floor-tile path (winner-verified copy).
- **FlowFest** — the hard-shadow button visibly sits on the shadow it will collapse into (winner-verified).
- **Exat** — the proximity glyph grid reacts immediately: "There are no instructions. The behavior is immediate and readable" (technique).
- **Cuberto** — the contextual cursor re-modes over each target; magnetic pull tugs elements toward the cursor at rest (winner-verified).
- **Igloo** — a "Scroll down to discover" HUD plus live node-graph values. **Aristide** — a bottom-centered `.e` explore indicator (winner-verified).

---

## Slot counts and failure modes

| Archetype | Committed slots | Optional | Total band | Echo (transformed forms) |
|---|---|---|---|---|
| Brutalist | C1, C2, C6 | C3 (bitmap or none), C5, C4 (1–2) | 3–5 | ≥3 |
| Bold-maximal | C1 (rich), C2 (pervasive kinetic), C3 (contextual-state), C6 | C5, C4 (1) | 4–5 | ≥3 |
| Experimental | C2, C3 (follower or justified none), C5, C6 | C1 (magnetic), C4 (strong) | 4–5 | ≥3 |
| Minimalist | C1 (low amplitude), C2, C6 | C5, C4 (1); **C3 none** | 3–4 | ≥3 |
| Editorial | C1, C2, C5 | C6, C4 (thin) | 3–4 | ≥2 |
| Immersive | C1, C2, C5, C6 | C3 (earned), C4 (Rive or audio) | 4–5 | ≥3 |
| Corporate-luxury | C1, C2, C5, C6 | C3 (scoped, magnetic, or none), C4 (soundscape) | 4–5 | ≥3, with the loader sharing type or material with the fold |
| Bento-card | C1, C2, C5 (pinned demo), C6 (live demo) | C4 (perpetual micro-loop), C3 (native, powers the shine) | 3–4 | ≥2 |
| Spatial-organic | C1, C2, C4 (ambient DNA), C5 | C6, C3 | 4–5 | ≥3 |

Three slots carry the continuity:

- **C5, a committed scroll texture** — marquee, parallax layer, scrubbed cross-section transformation, or pinned scrub. The evidence is broad: Cyd's wordmark marquee, Mat Voyce, Endex on mobile, Aristide's sliced-filmstrip scrub, Anime.js's pinned `100lvh` demo reel, Igloo's scroll-assembled simulation, Truekind's floating-product parallax, Gabriel's inverse-scale figure reveal.
- **C6 as a stateful, replayable spectacle** that differs each run — clone storm, physics world, per-link particle formation, drag reel, per-project morph. A hero climax that plays identically every time is not this.
- **The echo count itself.** "One signature element travels" is weaker than "the signature appears in N transformed forms across loader, nav, body, and footer." The second is countable.

Two failure modes survive a high channel count:

1. **The signature stays an episode.** A physics or gesture idea confined to the hero — never becoming the nav hover, the figure response, or the footer moment — does not travel and does not accumulate through content, so it reads as one trick rather than a thread. Winners transform theirs instead: Aristide's `-110%` slide runs loader through project morph, Mat Voyce's kinetic roll nav through footer.
2. **C5 near-absent.** Without a marquee, a parallax layer, or a scrubbed transformation, nothing carries the eye continuously down the page; idle loops keep a hero alive while the rest reads disconnected. Even the quietest register commits one — brutalist winners run scroll-scrubbed transformations (Joffrey's slider scale-up, Naked City's CRT scrub).

---

## Density versus coherence and budget

More channels risk incoherence, restraint, and performance. Winners resolve all three.

- **Against one grammar.** Winners bind channels through one easing family plus one metaphor. Cuberto's four interactions all ride one expo-out curve. Delvaux ships a byte-identical `cubic-bezier(0.25,1,0.5,1)` across CSS and GSAP. FlowFest binds every transform to `0.25s cubic-bezier(0.625,0.05,0,1)` under an "objects on a table" metaphor. All three are live-read values. Density coheres *because* of the grammar.
- **Against restraint.** Quiet archetypes keep the count and drop the amplitude. Restraint lowers amplitude, never coverage — Terminal, a minimalist winner, still ships C1, C2, C5, and C6, just quietly. The band holds; the amplitude dial handles restraint.
- **Against reduced motion and WCAG 2.2.2.** Every idle and scroll channel needs the reduced-motion strip and a pause path. This is a per-channel checklist, not a blocker.
- **Against 60fps and INP.** Winners gate by capability: kill cursor and magnetic effects on small screens, IntersectionObserver-gate idle channels to in-view only, desktop-gate scroll textures behind a width threshold. The density is real but budget-scoped by construction.

---

## Refuted

- **Exat's glyph-grid recolor is scroll-driven** — false: it is cursor-proximity driven.
- **Igloo's footer particle journey is a confirmed mechanic** — overstated: single-source.
- **Aristide's `.e` / `.e-s`** — corrected: they are CSS classes.
- **FlowFest's C2 runs on SplitText spans** — false: SplitText ships in a script tag and is never registered — L4 registers ScrollTrigger, CustomEase, DrawSVGPlugin, TextPlugin, and Draggable only ([brutalist](../archetypes/brutalist.md)). The C2 channel is real and stays: the H1 is inline `<svg><path>` whose spans stagger in on the loader handoff, and the chat cloud types through TextPlugin. The count of 5 is unaffected.
