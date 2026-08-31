---
title: "Awwwards 2024–2025 Winners — Mechanics Sweep"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "site-of-the-day", "site-of-the-month", "webgl", "threejs", "gsap", "scroll-interaction", "motion-design", "immersive-garden"]
sources:
  - "https://www.awwwards.com/sites/100-lost-species"
  - "https://www.awwwards.com/sites/aramco-the-birth-of-oil"
  - "https://www.awwwards.com/sites/montfort"
  - "https://www.awwwards.com/sites/david-whyte-experience"
  - "https://www.awwwards.com/sites/hatom"
  - "https://www.awwwards.com/sites/omega-clearspace"
  - "https://www.awwwards.com/watches-wonders-immersive-experience-for-cartier.html"
  - "https://www.awwwards.com/sites/ponpon-mania"
  - "https://www.awwwards.com/sites/terminal-industries"
  - "https://www.cssdesignawards.com/sites/terminal-industries/47847/"
  - "https://www.awwwards.com/sites/mindmarket"
  - "https://www.awwwards.com/annual-awards/winners"
  - "https://www.awwwards.com/websites/sites_of_the_month/"
  - "https://web.archive.org/web/20240307133625id_/https://www.awwwards.com/annual-awards-2023/"
  - "https://web.archive.org/web/20250313114414id_/https://www.awwwards.com/annual-awards-2024/"
  - "https://www.webgpu.com/showcase/cartier-watches-and-wonders-immersive-garden/"
  - "https://www.webgpu.com/showcase/hatom-griffin-mythology-webgl/"
  - "https://www.webgpu.com/showcase/omega-clearspace-orbital-debris-threejs/"
---

# Awwwards 2024–2025 Winners — Mechanics Sweep

Ten Awwwards-decorated sites read at component level yield eleven mechanics beyond the parent article's catalog, seven of the ten being Immersive Garden work converging on one house style, while Terminal Industries reaches award tier on CSS and Vue with no WebGL and no new mechanic at all. The 2025 annual titles sit outside the ten: Site of the Year and Users' Choice went to Lando Norris and Developer Site of the Year to Messenger, while the ten are Site of the Day and Site of the Month winners of 2024–2025. What each site ships and what each mechanic costs in stack terms follows. Archetype labels follow the taxonomy of the parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

## Award sites → mechanics table

Award status is stated only where direct evidence exists. Case pages and webgpu.com write-ups read 16 Jul 2026; the annual winners page and the monthly listing read 29 Aug 2026.

**Annual titles.** The [Awwwards Annual Awards winners page](https://www.awwwards.com/annual-awards/winners) (current edition) lists Site of the Year 2025 = Lando Norris (43 votes), Site of the Year Users' Choice 2025 = Lando Norris (596 votes), Developer Site of the Year 2025 = Messenger (54 votes), and Agency of the Year = Immersive Garden. Lando Norris also holds Site of the Day (SOTD) 17 Nov 2025 (8.18); Messenger holds SOTD 10 Nov 2025 with a Developer Award of 8.21 at `messenger.abeto.co` ([`../archetypes/immersive-cinematic.md`](../archetypes/immersive-cinematic.md)). None of the ten sites below holds a 2025 annual title, and no listing establishes nominee status for any of them, so every "SOTY nominee" framing is `(stated, unconfirmed)`. The corpus's other annual titles have listing-grade support: Lusion's Site of the Year 2023 and Developer Site of the Year 2023 on the [archived Annual Awards 2023 page](https://web.archive.org/web/20240307133625id_/https://www.awwwards.com/annual-awards-2023/), Igloo's Site of the Year 2024 and Developer Site of the Year 2024 on the [archived Annual Awards 2024 page](https://web.archive.org/web/20250313114414id_/https://www.awwwards.com/annual-awards-2024/). Three of the ten sites below are 2024-cycle SOTDs (David Whyte, Hatom and Omega Clearspace), carried for their mechanics rather than for any 2025 standing; the contender set spans 2024–2025.

Every site except Ponpon/Terminal/MindMarket is **Immersive Garden** and their mechanics converge on one house style (Three.js + GSAP + Lenis scroll-cinema); the three independent Site of the Month (SOTM) winners diversify the sample. SOTM months are read from the [monthly listing](https://www.awwwards.com/websites/sites_of_the_month/), not from site pages ([corporate-luxury corpus](../archetypes/corporate-luxury.md#corpus)).

| Site | Award + date | Archetype | Signature mechanics | Evidence |
|---|---|---|---|---|
| **100 Lost Species** [awwwards](https://www.awwwards.com/sites/100-lost-species) · 100lostspecies.com | SOTD 20 Oct 2025 (7.56) | spatial-organic / experimental | (1) **Timed self-erasing site** — a continuously-running 100s countdown that dissolves the whole experience at zero; (2) free-scroll species gallery; (3) watercolor textures, controlled asset streaming for 60fps | Awwwards tags: Contentful, Experimental, Animation, Gallery. Desc: *"In 100 seconds, 100 lost species are remembered, before the site itself disappears."* Studio: Immersive Garden + 60FPS. WebGL rendering `(inferred)`, no WebGL tag |
| **Aramco — Birth of Oil** [awwwards](https://www.awwwards.com/sites/aramco-the-birth-of-oil) | SOTD 27 May 2025 (7.3) | immersive / corporate-luxury | (1) **Scroll-scrubbed 3D camera path** through sequential scenes; (2) scrollytelling section continuity | Tags: 3D, Scrolling, Storytelling, Gestures/Interaction. Studio: Immersive Garden. Stack (GSAP/Three) `(inferred)` from the studio pattern, not tagged |
| **Montfort** [awwwards](https://www.awwwards.com/sites/montfort) | SOTD 23 Jun 2025 (7.62) · SOTM Jun 2025 (listing) | corporate-luxury / immersive | (1) scroll-driven 3D; (2) gesture/interaction layer | Tags: 3D, Scrolling, Gestures/Interaction, UI design. Studio: Immersive Garden |
| **David Whyte Experience** [awwwards](https://www.awwwards.com/sites/david-whyte-experience) | SOTD 31 Dec 2024 · +SOTM/FWA/CSSDA | immersive / spatial-organic | (1) **Cursor-driven watercolor displacement** shader over paintings; (2) **long-press to reveal location video**; (3) scroll transitions between watercolor scenes; (4) full-screen poetry | Tags: Experimental, Colorful, Gestures/Interaction. Desc + case study: *"a dynamic watercolor effect animates… as users move their cursors… a long press on any painting reveals a video."* Studio: Immersive Garden + painter Matthew Phinn |
| **Hatom** [awwwards](https://www.awwwards.com/sites/hatom) | SOTD Nov 2024 (+FWA/CSSDA SOTM) | immersive / experimental | (1) **Scroll-as-film-reel 3D camera** across 5 phases; (2) **cursor displacement distortion** of hovered content; (3) **procedural 3D metamorphosis** (egg cracks → griffin → armored); (4) custom progressive multi-scene preloader | webgpu.com write-up: Three.js + Vue/Nuxt + GSAP + Lenis; *"cursor movement… distorts the content it hovers over"*, *"custom progressive preloader feeds assets in behind the curtain."* Studio: Immersive Garden |
| **Omega Clearspace** [awwwards](https://www.awwwards.com/sites/omega-clearspace) | SOTD 24 Aug 2024 (7.31) | immersive / experimental | (1) **Wireframe ↔ textured-render morph on scroll**; (2) scroll-driven orbital-debris camera; (3) **scroll-depth audio layering** | webgpu.com: Three.js; *"3D models shift between textured renders and clean wireframes as you scroll"*, *"audio layers in as you move deeper."* Studio: Immersive Garden |
| **Cartier — Watches & Wonders 2025** [awwwards](https://www.awwwards.com/watches-wonders-immersive-experience-for-cartier.html) | **SOTD 18 Aug 2025 (7.64)** · Developer Award 7.55 · **SOTM Aug 2025** (listing) | corporate-luxury / spatial-organic | (1) six self-contained 3D "alcove" scenes `(stated, webgpu.com)` with **dispose/load scene streaming**; (2) **hidden per-scene gestures** (reward-on-discovery); (3) **Web Audio narrative score** ("Mooders") threaded through scroll; (4) mirror/water shader environments | webgpu.com: *"Three.js… Blender feeds GLBs, GSAP and Lenis… Web Audio threads a Mooders score,"* *"scenes dispose and load as you cross between alcoves,"* *"hidden gestures in every scene."* Studio: Immersive Garden |
| **Ponpon Mania** [awwwards](https://www.awwwards.com/sites/ponpon-mania) | SOTD 22 Oct 2025 (7.64) · **SOTM Oct 2025** | bold-maximal / experimental | (1) **Video-based panel transitions**; (2) **3D camera moves within comic panels**; (3) **mouse-controlled physics playground** (About); (4) cursor-driven panel micro-interactions | Tags: WebGL, GSAP, Nuxt.js, 3D, Parallax, Microinteractions, Unusual Navigation. 8 named interactions incl. "Panel Camera Movement", "About Physics". By Justine Soulié + Patrick Heng |
| **Terminal Industries** [awwwards](https://www.awwwards.com/sites/terminal-industries) | SOTD 3 Sep 2025 (7.68) · SOTM Sep 2025 · CSSDA Website of the Day 4 Aug 2025 (8.42) | minimalist, per the live CSS read in [`../archetypes/minimalist.md`](../archetypes/minimalist.md); the case-page prose reads editorial-dark / corporate, and neither award page carries an archetype tag | (1) **CSS-driven scroll storytelling** (no WebGL); (2) high-craft motion/transition system (dev anim 8.80) | Tags: **CSS, Vue.js, Vercel**, Scrolling, Storytelling, Interaction Design. Studios: REJOUICE + PROPAGANDE. Notable: award-tier motion with zero WebGL |
| **MindMarket** [awwwards](https://www.awwwards.com/sites/mindmarket) | SOTD 29 Dec 2025 (7.85) · **SOTM Dec 2025** | bold-maximal / editorial | (1) "**the thread**" — a continuous connecting-line motif driving scroll progression; (2) animated hand-drawn characters; (3) rhythm-over-distraction scroll transitions | Case study: *"the thread… scroll-based transitions kept smooth to preserve readability while adding progression"*, hand-drawn illustration, no stock/AI. Dev: Louis Paquet |

## New mechanics beyond the parent catalog

The 2026 sweep keeps its own table ([`./awwwards-2026-winners.md#mechanics-not-already-cataloged`](./awwwards-2026-winners.md#mechanics-not-already-cataloged)); its rows 2 and 6 are the 2026 instances of rows 1 and 6 here.

| # | Mechanic | Site(s) | How it works | Stack | Source |
|---|---|---|---|---|---|
| 1 | Scroll-scrubbed 3D camera path with scene streaming | Aramco, Hatom, Cartier, Omega | a camera dollies along a fixed spline; each scene's GLB assets `dispose()`/load at section boundaries so memory stays bounded and transitions never stall, the progressive preloader feeding the next scene behind the curtain | Three.js/OGL WebGL + GSAP ScrollTrigger + Lenis | [Cartier](https://www.webgpu.com/showcase/cartier-watches-and-wonders-immersive-garden/) · [Hatom](https://www.webgpu.com/showcase/hatom-griffin-mythology-webgl/) |
| 2 | Fluid/displacement cursor distortion of hovered media | Hatom, David Whyte | cursor position feeds a displacement/flowmap shader that warps the image or 3D content under the pointer | Three.js/OGL fragment shader (flowmap + displacement texture) | [Hatom](https://www.webgpu.com/showcase/hatom-griffin-mythology-webgl/) · [David Whyte](https://www.awwwards.com/sites/david-whyte-experience) |
| 3 | Wireframe ↔ textured-render morph on scroll | Omega Clearspace | the model cross-fades between clean wireframe and fully textured material as scroll progresses, exposing "the engineering beneath the spectacle" | Three.js (dual material or shader `mix()` keyed to scroll uniform) | [Omega](https://www.webgpu.com/showcase/omega-clearspace-orbital-debris-threejs/) |
| 4 | Timed self-erasing / self-destructing narrative | 100 Lost Species | the countdown advances regardless of interaction; the erasure is the message | Vanilla JS (interval timer + CSS/canvas dissolve transition) | [100 Lost Species](https://www.awwwards.com/sites/100-lost-species) |
| 5 | Long-press-to-reveal hidden video layer | David Whyte | press-and-hold rather than click; press duration drives the reveal, tuned separately for touch and mouse | Vanilla JS (pointerdown timer + reveal transition) | [David Whyte](https://www.awwwards.com/sites/david-whyte-experience) |
| 6 | Scroll-depth progressive audio layering | Cartier, Omega | tracks fade and stack as a function of scroll progress / scene depth, treating the score as a narrative layer rather than a background bed | Vanilla JS + Web Audio API (per-track `GainNode` automation keyed to scroll) | [Cartier](https://www.webgpu.com/showcase/cartier-watches-and-wonders-immersive-garden/) |
| 7 | Hidden per-scene gesture rewards ("trip every interaction") | Cartier, Ponpon | each scene conceals an interaction the user must discover to progress; discovery-gated, mapped per scene | Vanilla JS event mapping (or in-engine for WebGL scenes); a pattern, not a library | [Cartier](https://www.webgpu.com/showcase/cartier-watches-and-wonders-immersive-garden/) |
| 8 | Mouse-controlled physics playground | Ponpon Mania ("About Physics") | cursor drives a 2D rigid-body sim of draggable/collidable illustrated objects | a physics lib (Matter.js/Rapier) + canvas/WebGL render | [Ponpon Mania](https://www.awwwards.com/sites/ponpon-mania) |
| 9 | Video-clip section/panel transitions | Ponpon Mania ("Panel Navigation — video-based transitions") | pre-rendered clips play through as the transition between sections on a nav event; distinct from scrubbed-video, which maps a clip to a scroll/pointer timeline, this is event-triggered playthrough | Vanilla JS (preloaded `<video>` swap, play on navigate) | [Ponpon Mania](https://www.awwwards.com/sites/ponpon-mania) |
| 10 | Procedural 3D object metamorphosis on scroll beat | Hatom | narrative states stepped by scroll (egg → hatch → griffin → armored + city grows) | Three.js morph targets / GLB animation clips | [Hatom](https://www.webgpu.com/showcase/hatom-griffin-mythology-webgl/) |
| 11 | Continuous "thread" connective-line scroll motif | MindMarket | one drawn line persists across sections, extending and redrawing with scroll to signal progression and connection (the brand concept drives the whole UX) | Vanilla JS / SVG path animation: a single SVG line-draw extended into a persistent cross-section spine, or GSAP for easing | [MindMarket](https://www.awwwards.com/sites/mindmarket) |

**Winner-verified negative:** Terminal Industries (minimalist) hits award tier with **CSS + Vue only, no WebGL**; its differentiator is motion-system craft, not a novel mechanic, so it adds nothing to the catalog above.

## Could not verify

- Aramco and Montfort stacks (GSAP/Three): inferred from the studio pattern, not from Awwwards tags `(inferred)`.
- 100 Lost Species: whether it renders in WebGL; the entry carries no WebGL tag.
- Cartier's six alcoves on Three.js: stated by the webgpu.com write-up linked in the mechanics table, not by the Awwwards case study `(stated, webgpu.com)`; the award line itself sits in the [corporate-luxury corpus](../archetypes/corporate-luxury.md#corpus).
- The nominee lists behind the 2025 annual titles: not reachable, so no site's nominee status is established.
