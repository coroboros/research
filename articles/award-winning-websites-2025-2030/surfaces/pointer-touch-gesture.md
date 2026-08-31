---
title: "Pointer, Touch and Gesture on Winners — The Pointer Layer Goes Dormant on Touch"
date: "2026-07-30"
author: "Coroboros"
tags: ["pointer-events", "touch", "mobile", "gestures", "custom-cursor", "parallax", "scroll-snap", "gsap", "lenis", "accessibility", "awwwards", "mobile-excellence"]
sources:
  - "https://www.awwwards.com/mobile-excellence-guidelines.pdf"
  - "https://www.awwwards.com/how-to-win-the-mobile-excellence-award-checklist.html"
  - "https://www.awwwards.com/customize-your-mouse-cursor-inspirational-examples-implementation-tricks.html"
  - "https://www.awwwards.com/sites/exat-typeface"
  - "https://www.awwwards.com/sites/cuberto"
  - "https://www.awwwards.com/sites/mouse-parallax-wonderland"
  - "https://www.awwwards.com/sites/dennis-snellenberg"
  - "https://www.awwwards.com/sites/project-parallax"
  - "https://www.awwwards.com/sites/parallax-js"
  - "https://www.awwwards.com/sites/igloo-inc"
  - "https://github.com/Cuberto/mouse-follower"
  - "https://github.com/darkroomengineering/lenis"
  - "https://gsap.com/docs/v3/Plugins/Draggable/"
  - "https://tympanus.net/codrops/2019/08/07/image-trail-effects/"
  - "https://tympanus.net/codrops/2026/05/20/made-with-gsap-building-a-fun-gravity-based-mouse-trail/"
  - "https://tympanus.net/codrops/2025/04/21/mastering-carousels-with-gsap-from-basics-to-advanced-animation/"
  - "https://tympanus.net/codrops/2021/05/04/dynamic-css-masks-with-custom-properties-and-gsap/"
  - "https://www.cssdesignawards.com/sites/exat-typeface/47246"
  - "https://thefwa.com/cases/exat-typeface-p2"
---

# Pointer, Touch and Gesture on Winners — The Pointer Layer Goes Dormant on Touch

On winner mobile renders the pointer-move classes (cursors, cursor proximity, pointer parallax, tilt) are **not ported to touch**: they go dormant, and the mobile page is carried by scroll-driven reveals, swipe galleries, a tap-flash on press elements, and one ambient idle channel. This is the convention, not a gap in those builds. The pointer-move, tap, swipe, and mobile-gesture record across award winners, 2024–2026, rests on two winners inspected first-hand under phone emulation. Archetypes and their canonical winners live in [the parent reference](../award-winning-websites-2025-2030.md).

Evidence tags: **winner** (named Awwwards Site of the Day (SOTD) or Site of the Year (SOTY)) · **official** (Awwwards or Google criteria) · **technique** (documented, no specific winner grounding) · **unverified** (could not be grounded, flagged).

## Pointer kit

### Pointer parallax — multi-layer differential

- **Winners.** Wix "Mouse Parallax Wonderland" (SOTD); Dennis Snellenberg's portfolio (SOTD, parallax-rich, GSAP + Locomotive); Project Parallax (Honorable Mention).
- **Mechanic.** On `pointermove`, normalize the pointer to `nx = (e.clientX / vw) - 0.5` and `ny = (e.clientY / vh) - 0.5`, giving a −0.5…0.5 range. Each layer carries a `data-depth` (0.02 background through 0.12 foreground). Per rAF, `target = depth * n * maxShiftPx`, then `current += (target - current) * 0.1`, writing `transform: translate3d(x, y, 0)`, compositor-only, never `top`/`left`. Foreground layers move opposite in sign to the ground for depth. Cap `maxShift` at 12–24px so it reads as depth rather than drift.
- **Touch.** Dormant. There is no `pointermove` on touch. Layers rest at `translate3d(0,0,0)` and depth comes from scroll instead. Binding the same layers to `deviceorientation` is possible but rare and gated.
- **Cost.** Vanilla plus rAF, no rig.

### Image-trail cursor

- **Winners.** Cuberto ([bold maximal corpus](../archetypes/bold-maximal.md#corpus)). The Codrops "Image Trail Effects" set is the canonical implementation, refreshed in 2026 as a gravity variant.
- **Mechanic.** Cache the last mouse position; each frame compute `dist = Math.hypot(x - lastX, y - lastY)`; when `dist > threshold` (default **100px**), activate the next `<img>` from a fixed pool, cycling and repeating, place it under the pointer with an incrementing z-index, animate it in by scale and opacity, and auto-deactivate older items after N. Smoothness via `lerp = (1 - n) * a + n * b` with n ≈ 0.1–0.2. The pool is DOM `<img>` under GSAP, or WebGL/OGL for stylized trails.
- **Touch: dormant, verified first-hand.** Under iPhone emulation (390×844, `hover: hover` false, `pointer: coarse` true) `cuberto.com` instantiates **no cursor DOM at all**: `.mf-cursor` absent, `body { cursor: auto }`. Mobile is a vertical scroll of full-bleed autoplaying case tiles. The trail is never ported.
- **Cost.** The vanilla-DOM version is a light rig; the WebGL version is a real one. Desktop-gate behind `@media (hover: hover) and (pointer: fine)`.

### Cursor-proximity weight

- **Winner.** **Exat** typeface ([bold maximal corpus](../archetypes/bold-maximal.md#corpus)): kinetic type whose glyphs respond to pointer distance.
- **Mechanic.** For each target (letter, cell, dot), each frame compute `d = hypot(cx - px, cy - py)`, map through a falloff `f = clamp(1 - d / radius, 0, 1)` with radius ~200–400px, and drive a property by `f`: `scale = 1 + f * k`, a `font-variation-settings` axis, a `color-mix()`, or a translate toward or away. Lerp per element to avoid snap. Batch reads in one rAF and write only transforms or custom properties.
- **Touch: dormant, verified first-hand.** Under the same phone emulation, `exat.hottype.co` renders the kinetic mark as a **static giant wordmark**, type-as-image, with no canvas and no proximity; the specimen becomes a plain vertical scroll.
- **Cost.** Vanilla plus rAF; cost scales with target count, so cap the field. Exat drives display type, never body copy.

### Contextual cursor — state-morphing plus magnetic

- **Winner.** Cuberto, whose `mouse-follower` library powers it (Lando Norris does not belong here; see Refuted).
- **Mechanic.** One follower element lerped to the pointer, with the DOM declaring state through data attributes: `data-cursor="-pointer"`, `data-cursor-text`, `data-cursor-icon`/`img`/`video`, `data-cursor-stick[="#sel"]` for magnetic attach. Cuberto's defaults, verbatim: `speed: 0.55`, `ease: 'expo.out'`, `stickDelta: 0.15` (magnet strength), `skewingDelta: 0.001`, `skewingDeltaMax: 0.15`, `hideTimeout: 300`. Magnetic pull on a target translates the element toward the pointer by `(pointer − center) * pull` with pull ~0.2–0.4, clamped to a maximum and lerped.
- **Touch.** Dormant, corroborated by Awwwards' own cursor guidance: "custom cursors don't work well on mobile." The morphing-label layer drops with it.

### Pointer spotlight — technique, not winner-grounded

- **Winners.** None named; a documented premium technique, see Could not verify below.
- **Mechanic.** Feed the pointer into CSS custom properties `--mx` / `--my`; a top layer uses `mask-image: radial-gradient(circle at var(--mx) var(--my), …)`, or a `mix-blend-mode` grayscale-to-color pair, so only the disc under the pointer reveals the treated layer. Compositor-friendly; update the properties in rAF, not per event.
- **Touch.** Dormant. Ship the revealed color layer flat, or drop the effect.

### Tilt card — unverified as a winner mechanic

- **Winners.** None named; it survives as a documented technique only, see Could not verify below.
- **Mechanic.** On `pointermove` within bounds, `rotateY = (offsetX / halfW) * maxDeg` and `rotateX = -(offsetY / halfH) * maxDeg` with maxDeg ~8–12, under `perspective: 800–1200px`; reset on leave; an optional glare layer tracks the pointer.
- **Verdict: hold.** Tilt on every card is a generic tell, the "one trick stamped on every class" failure, and it is not award-differentiating in the current record. If used at all, apply it to a single restrained hero object, never a grid.

### Physics conventions the award tier keeps

- **Smooth scroll.** Lenis, default `lerp: 0.1`, common winner config `duration: 1.5`, synced to `gsap.ticker` with `lagSmoothing(0)`. Touch stays on native inertia.
- **Follower and parallax lerp.** 0.1 per frame is the house value; 0.08 is slower and heavier, 0.2 snappier.
- **Image trail.** Threshold ≈ 100px via `Math.hypot`, pool-cycled.
- **Magnetic.** Pull 0.2–0.4, `stickDelta: 0.15`.

## Touch kit

### Swipe-snap gallery

- **Grounding: official.** The Awwwards/Google Mobile Excellence criteria state verbatim: **"Possible to swipe to see more images or tap to enlarge them."** An explicitly scored line, not inference.
- **Native-first mechanic.** `scroll-snap-type: x mandatory` on the track, `scroll-snap-align: center` or `start` on each cell, `overflow-x: auto` plus `-webkit-overflow-scrolling: touch` for iOS momentum. Add `scroll-padding` for peek. A dot or index indicator reflects the snapped cell via IntersectionObserver on the cells. No JS momentum needed: the OS provides it.
- **Rig variant**, when drag-with-inertia beyond a viewport is wanted: GSAP Draggable plus InertiaPlugin, `inertia: true`, `throwResistance: 1000` (the default; higher stops quicker), and a `snap` function landing on cell width.

### Tap-flash — the touch verb

- **Grounding.** The Mobile Excellence lines "Size tap targets appropriately" and "tap to enlarge." Every winner element that carried a hover state resolves its touch state as a **press response**, not a hover port.
- **Mechanic.** On press and strike elements, the `:active` / `pointerdown` transient is the response the finger feels: a quick flood, tint, or recoil that peaks and settles over roughly 140–300ms. The element keeps its action (a link still navigates) and the flash rides the response's presentation without hijacking a scroll-intent tap. It is measured at peak-hold, not at rest.
- **First-tap-preview, second-tap-navigate** is a real pattern only where a hover genuinely carried information a tap cannot reach: a hover dropdown, a hover caption. For cards and figures, winners overwhelmingly ship **direct tap-to-open plus a tap-flash**, not a two-tap gate.

### Drag-explore

- **Grounding.** The winner-verified instance is a hold-and-drag horizontal strip with native touch overflow and release momentum (Siena's filmstrip).
- **Mechanic.** `overflow` scroll for the native path; enhance with GSAP Draggable `type: "x"` (or `"x,y"` for a canvas or board), `inertia: true`, bounds, and `edgeResistance`. On touch this is just native scroll; the rig adds throw physics and non-scroll-axis exploration for a map, a moodboard, or a spatial index.

### Gyro parallax — winner-grounded but rare and gated

- **Winner.** parallax.js (SOTD), which "reacts to the orientation of a smart device." Beyond dedicated parallax demos, gyro is uncommon on flagship winners. Treat it as spice, not a default.
- **Mechanic.** `deviceorientation` gives `beta` (front-back, −180…180) and `gamma` (left-right, −90…90); clamp and map to the same layer translate as pointer parallax (`x = gamma / 45 * maxShift`, `y = (beta − baseline) / 45 * maxShift`), lerped. Establish a baseline on the first reading, since users do not hold phones flat.
- **The iOS gate is mandatory.** iOS 13+ requires `DeviceOrientationEvent.requestPermission()`, which **only** resolves inside a user gesture (never on load) and needs HTTPS. Feature-detect `typeof DeviceOrientationEvent.requestPermission === 'function'` and bind directly on other platforms. Winners that bother wire it to an existing tap, such as an enter gate or a start button. Ship dormant if permission is denied.

### Momentum — shared physics, not a component

On touch, keep native inertia: `-webkit-overflow-scrolling: touch` and passive listeners (Mobile Excellence: "Uses passive listeners to improve scrolling performance"). Do **not** smooth-scroll touch with Lenis by default: smoothing fights OS momentum. Lenis exposes `syncTouch`; reserve it for a pinned scroll-scrub that must stay synced on touch, never as a global.

## The mobile grammar

1. **Winner mobile is not the desktop hover palette re-triggered on touch.** Cursor, cursor-proximity, pointer-parallax, and tilt classes go dormant rather than being ported. Verified: Cuberto instantiates zero cursor DOM on touch; Exat's proximity type renders as a static wordmark. The page is carried by scroll, swipe, tap, and idle.
2. **Press and strike elements must answer the tap**: a peak-and-settle flash, flood, or recoil on `:active` / `pointerdown`, keeping the element's action. The tap works where the cursor cannot; this is the invitation floor.
3. **Figures and cards answer touch with tap-to-open plus a tap-flash**, never a ported hover-zoom. Galleries of images become swipe-snap tracks; "swipe to see more, tap to enlarge" is a scored line.
4. **Reveal, scrub, counter, curtain, valediction (all scroll-driven) keep as-is.** Scroll is the same on touch. These carry the mobile motion.
5. **At least one ambient idle channel stays on** (grain, glow, float). It is the mobile lifeline once hover is gone; a page whose every move waited for a cursor reads embalmed on a phone.
6. **Gyro parallax is optional and rare**: only behind a tap-triggered iOS permission gate, dormant if denied.
7. **Native touch momentum stays native.** Passive listeners, `-webkit-overflow-scrolling`. Tap targets ≥ 44×44, with 24 as the accessibility floor.
8. **An honest resting state is legal.** If a class has no meaningful touch verb, it rests static and legible. Dormant-at-rest is a winner answer, not a failure.

## Touch answers by dependency

- **Scroll-dependent.** Entrance and curtain reveals, per-char assembles, emphasis fills, odometers and load counters, pinned scrubs, route curtains, footer valedictions: unchanged, because scroll is unchanged. Smooth scroll is the exception: desktop layer only, touch on native inertia.
- **Hover-dependent but action-bearing.** CTAs, cards, figures, label wipes, accent links: the response moves to `:active` / `pointerdown` at peak-hold and the action is preserved. Figures open on tap; image galleries become swipe-snap tracks.
- **Pointer-position-dependent.** Followers, proximity fields, parallax layers, tilt, spotlight masks: dormant. A pointer-driven scrub runs from scroll or drag instead, and a pointer-driven shader can run from `touchmove` or fall back to its ambient noise-field mode, which doubles as the idle channel.
- **Layout-only.** Mastheads, splits, type-as-image, lists, logo walls, stat bands, card grids, full-bleed figures: no pointer dependency at all. A logo wall's grayscale-to-color hover rests grayscale on touch, which is honest.
- **Ambient and idle.** Unchanged, and load-bearing on mobile as the idle lifeline.

**Net.** The `(hover: none)` state is not filled by porting hover effects: winners deliberately let those effects go dormant. The two touch verbs that carry the record are a committed **tap-flash** on press and strike elements and a **swipe-snap gallery**, which Awwwards scores explicitly. Everything scroll-driven works on touch unchanged.

## Refuted

- **Lando Norris ships a contextual cursor.** False: the live read finds `body { cursor: auto }` and no follower element at all ([immersive-cinematic](../archetypes/immersive-cinematic.md), [bold-maximal](../archetypes/bold-maximal.md)). The contextual-cursor winner in this record is Cuberto alone.

## Could not verify

- **Pointer spotlight.** No SOTD in 2024–2026 was found shipping the mask-and-blend reveal. The mechanic above is documented technique, ungrounded in a named winner.
- **Tilt card.** No 2024–2026 SOTD leaning on tilt cards could be grounded. The rotation math above is documented technique, and tilt on every card remains the "one trick stamped on every class" tell.
