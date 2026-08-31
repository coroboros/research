---
title: "Experimental — Effect Palette, Page Recipe, Mid-Page Aliveness"
date: "2026-07-30"
author: "Coroboros"
tags: ["web-design", "design-archetypes", "experimental", "art-directed", "webgl", "threejs", "shaders", "gsap", "kinetic-typography", "custom-cursor", "awwwards", "scroll-driven-animation"]
sources:
  - "https://bruno-simon.com/"
  - "https://www.awwwards.com/sites/bruno-simon-portfolio"
  - "https://www.awwwards.com/sites/brunos-portfolio"
  - "https://www.awwwards.com/brunos-portfolio-case-study.html"
  - "https://medium.com/@bruno_simon/bruno-simon-portfolio-case-study-960402cc259b"
  - "https://thefwa.com/cases/bruno-simon-portfolio"
  - "https://igloo.inc"
  - "https://www.awwwards.com/sites/igloo-inc"
  - "https://www.awwwards.com/igloo-inc-case-study.html"
  - "https://web.archive.org/web/20250313114414id_/https://www.awwwards.com/annual-awards-2024/"
  - "https://www.webgpu.com/showcase/igloo-inc-procedural-crystals/"
  - "https://lusion.co"
  - "https://www.awwwards.com/sites/lusion-v3"
  - "https://web.archive.org/web/20240307133625id_/https://www.awwwards.com/annual-awards-2023/"
  - "https://www.cssdesignawards.com/blog/2023-website-of-the-year-winners/394/"
  - "https://www.cssdesignawards.com/woty-award-winners"
  - "https://www.cssdesignawards.com/wotm/lusion-v3/44311/"
  - "https://thefwa.com/api/cases/lusion-v3"
  - "https://aristidebenoist.com/static/css/d.css"
  - "https://aristidebenoist.com/static/js/d.js"
  - "https://www.awwwards.com/sites/aristide-portfolio-2021"
  - "https://www.awwwards.com/sites/aristide-benoist-portfolio"
  - "https://obys.agency"
  - "https://www.awwwards.com/sites/obys-2"
  - "https://www.awwwards.com/obys/"
  - "https://www.awwwards.com/inspiration/active-theory-v5-homepage"
  - "https://www.awwwards.com/30-experimental-webgl-websites.html"
  - "https://www.awwwards.com/websites/sites_of_the_year/"
  - "https://www.awwwards.com/websites/sites_of_the_month/"
  - "https://www.awwwards.com/annual-awards/winners"
  - "https://www.awwwards.com/sites/terminal-industries"
  - "https://www.awwwards.com/sites/lando-norris"
  - "https://www.inkandswitch.com/static/base.css"
  - "https://thesephist.com/css/main.css"
  - "https://tympanus.net/codrops/2026/05/06/from-shader-uniforms-to-clip-path-wipes-how-gsap-drives-my-portfolio/"
  - "https://tympanus.net/codrops/2025/10/08/how-to-animate-webgl-shaders-with-gsap-ripples-reveals-and-dynamic-blur-effects/"
  - "https://tympanus.net/codrops/2025/05/14/from-splittext-to-morphsvg-5-creative-demos-using-free-gsap-plugins/"
  - "https://tympanus.net/codrops/2020/08/05/magnetic-buttons/"
  - "https://github.com/codrops/MagneticButtons"
  - "https://github.com/Cuberto/mouse-follower"
  - "https://github.com/Cuberto/cursor-magnetic-demo"
  - "https://cuberto.com/tutorials/27/"
  - "https://metabole.studio/en/blog/immersive-website-examples"
---

# Experimental — Effect Palette, Page Recipe, Mid-Page Aliveness

Across this corpus **the interaction layer renders inside the WebGL/canvas engine rather than being stamped on DOM elements with CSS**, and the line's overall jury scores cap at 7.9–8.25; Lusion's 8.25 is the corpus's highest whole-site score. Effect palette, page recipe, and mid-page aliveness for the experimental / art-directed archetype. Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

The lazy build ships one CSS hover (pale fill-sweep) and one CSS nav bar across every element. The winners give each element class its own behavior inside a single authored world.

## Corpus

Evidence tags: `(winner-verified)` = read from the awarded site's live CSS, JS, or DOM; `(shipped)` = observed live or in award-page media, implementation not read; `(technique)` = a documented method, typically Codrops; `(design-canonical)` = a documented design system with no verified award; `(single-source)` = one site only; `[CSS]` / `[JS]` = quoted from shipped code; **verified** / **stated** / **observed** = measured in source / claimed by the builder / seen but not read; `(stated, unconfirmed)` = a builder claim the source read could not confirm; `(inferred)` = derived from indirect evidence.

| Site | Award | Jury scores | Stack | URL |
|---|---|---|---|---|
| **Bruno Simon — 2019 build** | Awwwards Site of the Day (SOTD) 11 Nov 2019 + Developer Award 8.17 (Animations/Transitions 9.00) + FWA + CSSDA (both belong to this build, not the rebuild) | Design 7.94 / Usability 7.55 / Creativity 8.95 / Content 8.13 / **Overall 8.04** | Three.js + Cannon.js `(stated, Medium case study)`, matcaps, spatial audio; solo dev | `bruno-simon.com` |
| **Bruno Simon — 2025 rebuild** | Awwwards SOTD 21 Jan 2026 + Site of the Month (SOTM) Jan 2026 + Developer Award 7.65 (Animations/Transitions 8.60) + Portfolio Honors; no FWA or CSSDA on this entry | Design 8.05 / Usability 7.83 / Creativity 8.62 / Content 8.18 / **Overall 8.11** | same lineage, physics drop-in; the award page names no engine, Rapier `(stated, unconfirmed)` | `bruno-simon.com` |
| **Igloo Inc** (Abeto) | Awwwards SOTD 23 Jul 2024 + **Site of the Year (SOTY) 2024** + Developer Site of the Year 2024; Developer Award 7.66 (Animations/Transitions 9.60) | Design 8.05 / Usability 7.5 / Creativity 8.31 / Content 7.91 / **Overall 7.92** | Three.js + Svelte + GSAP + Houdini + Blender; entire UI in WebGL | `igloo.inc` |
| **Lusion v3** | Awwwards SOTD 2 Oct 2023 + **Site of the Year 2023** + **Developer Site of the Year 2023**; CSSDA Website of the Month Oct 2023 + **Website of the Year 2023 winner** (9.27, also Best Agency Site); FWA of the Day 21 Sep 2023 + FWA of the Month Sep 2023 + FWA of the Year 2023 | Design 8.26 / Usability 7.95 / Creativity **8.65** / Content 8.26 / **Overall 8.25**; Dev Award 8.41 (Animations/Transitions 10.00) | Three.js + GSAP; studio flagship | `lusion.co` |
| **Aristide Benoist** | Awwwards SOTD 24 Jun 2021 + SOTM Jun 2021 (also SOTD 2018, 2019) | Design 8.37 / Usability 7.37 / Creativity 8.18 / Content 8.17 / **Overall 8.01**; Developer Award 7.86, Animations/Transitions **9.20** | Solo WebGL dev, vanilla/OGL, custom Rollup bundle; design by Jon Way | `aristidebenoist.com` |
| **Obys Agency** | Awwwards **Studio of the Year 2023**; `obys.agency` SOTD 4 May 2026 + Developer Award 7.98; profile 42 SOTD, 2 SOTM, 33 Honorable Mentions | Design 7.56 / Usability 7.04 / Creativity 7.71 / Content 7.75 / **Overall 7.46** (the 2026 entry) | GSAP; magnetic cursor + kinetic type signature | `obys.agency` |
| **Active Theory** | Multiple Awwwards SOTY historically (Google/Nike/Netflix work) | — | Proprietary WebGL engine, "more engine than website" | `activetheory.net` |
| **Resn** | Multiple SOTY; *GOOD Meat* SOTM | — | Three.js + GSAP, animation-first builds | `resn.co.nz` |
| **Thibault Guignand** | Award-unverified; Codrops-documented build, 6 May 2026 | — | OGL + GSAP + React; single `progress` uniform pattern | `thibaultguignand.com` |
| **Ink & Switch**, **Thesephist** | Award-unverified, not Awwwards submissions | — | Research-publication sub-stack; CSS read for the quiet register | `inkandswitch.com`, `thesephist.com` |

Award lines are read from the Awwwards site pages; annual titles from the [archived Annual Awards 2023 page](https://web.archive.org/web/20240307133625id_/https://www.awwwards.com/annual-awards-2023/) (Lusion Site of the Year and Developer Site of the Year; Obys Studio of the Year) and the [archived Annual Awards 2024 page](https://web.archive.org/web/20250313114414id_/https://www.awwwards.com/annual-awards-2024/) (Igloo Inc Site of the Year and Developer Site of the Year); Lusion's CSSDA win from the [2023 Website of the Year winners post](https://www.cssdesignawards.com/blog/2023-website-of-the-year-winners/394/) and the [WOTY winners list](https://www.cssdesignawards.com/woty-award-winners), its [WOTM Oct 2023](https://www.cssdesignawards.com/wotm/lusion-v3/44311/) from the CSSDA page, and its FWA titles from the [FWA case record](https://thefwa.com/api/cases/lusion-v3); Bruno's SOTM Jan 2026 and Obys's profile totals from the [Site of the Month listing](https://www.awwwards.com/websites/sites_of_the_month/) and the [Obys profile](https://www.awwwards.com/obys/).

Named from the award record without a live read: **Terminal Industries** SOTD 3 Sep 2025 (7.68) + SOTM Sep 2025 · **Messenger** SOTD 10 Nov 2025 + Developer Award 8.21, Developer Site of the Year 2025 · **Lando Norris / OFF+BRAND** SOTD 17 Nov 2025 (8.18), Site of the Year 2025 and Site of the Year Users' Choice 2025 · **Immersive Garden** (Cartier W&W25's agency) Agency of the Year 2025. The 2025 annual titles are read from the [Awwwards Annual Awards winners page](https://www.awwwards.com/annual-awards/winners).

**Version caveat, Lusion.** The award (SOTY 2023) was for *Lusion v3*; quoted copy is verbatim from the current live `lusion.co` (©2026), the studio's continuously-evolving flagship. The voice formula is stable across versions; exact strings are tagged live-2026.

**Evidence base.** Every copy verdict rests on raw-HTML grep plus tag-strip, or on the rendered DOM; every award line on the award page, listing, or archived annual page named inline. Hero strings returning zero on literal grep do so because inline `<strong>` and SplitText spans split them; tag-stripping reassembles and they match.

### The score reality

Overall SOTD scores on this line cap around 7.9–8.25, and Lusion's 8.25 is the corpus's highest whole-site score. The Creativity sub-axis is what spikes: 8.65 Lusion, 8.95 Bruno (2019 build), 8.62 Bruno (2025 rebuild). Igloo's and Lusion's Site-of-the-Year titles are peer-voted annual awards, not jury scores; their underlying SOTD overalls are 7.92 and 8.25.

## Effect palette

### Hover and micro-interactions

The AI-default: every button gets `transition: background .3s` sweeping a pale, washed-out tint (10–20% brand-alpha) left to right; every link gets a CSS underline slide; every card gets `transform: scale(1.03)`. One trick cloned onto every element class.

The pale tint fill is **absent from the entire corpus**. When a button changes on hover it goes to a full opaque token, or it stops being a CSS treatment and becomes a magnetic/WebGL response.

- **Full-token fill** (button/CTA). Background animates to a solid token, the label inverting to the page background, often with a shadow layer for depth. Never a low-alpha wash. *When:* the one place a conventional HTML button survives in an otherwise-WebGL site (contact, "view work"). Cuberto's circular button "fills with a solid color, with a shadow element creating depth"; Codrops *Magnetic Buttons* documents the same solid fill. ≥2.
- **Magnetic pull + label follow** (button and nav item). The element (or an inner label) translates toward the cursor with elastic easing while hovered, snapping back on leave; the custom cursor scales to wrap it. *When:* primary CTAs and nav words on typography/agency builds, the archetype's default button behavior, replacing the fill entirely. Obys ("bold magnetic cursor that sticks to elements with smooth elasticity"), Cuberto `mouse-follower` / `cursor-magnetic-demo` (GSAP v3), Lusion v3 reactive cursor. ≥3.
- **WebGL scramble on hover (SDF offset)** (text/UI links inside a canvas). Hovering a word resolves it by shifting the SDF texture offset, not by relaying out DOM. Igloo Inc: "text scrambles by adjusting the offset of the SDF texture… avoids style recalculations". Guignand scramble charset `A!B@C#D$E%F&G*H?J[K]L{M}N=O+P-QRSTUVWXYZ`. ≥2.
- **Flowmap / velocity distortion under the pointer** (images and cards). Cursor velocity writes into an off-screen RG texture each frame, accumulating a fading brush stroke that warps the image and splits RGB along the mouse→pixel vector. *Verified magnitudes (Guignand, technique):* R ×1.5, G ×0.5, B ×1.8; rainbow activates when `uVelo > 0.01` via three sines at 120° phase (2.094, 4.188 rad). Igloo applies chromatic aberration on the same aesthetic; Active Theory "elements light up/shift as you hover". ≥2 for the chromatic-hover family; exact flowmap numbers single-source.
- **Soft circular texture-reveal on hover** (card/media swap). `uMixFactor` 0→1 masked by `smoothstep(0.0, 0.5, distance)`; enter `duration: 3, power3.out`, exit `duration: 0.5, power3.out`. *When:* image-grid hover where the reveal is the content. Codrops *Animate WebGL Shaders with GSAP* (Oct 2025). `(technique, single-source)`.

#### The nav bar

The corpus does not hang a scrolled solid nav bar with a contrasting `border-bottom`. That pattern is absent. Two winner treatments instead:

- **No HTML nav bar at all: UI lives in the engine.** Bruno Simon: "everything had to be part of the 3D world"; the menu, clicks, and scroll are 3D models, wayfinding is colored floor tiles reading as a path. Igloo Inc: "the entire UI is rendered in WebGL rather than HTML." Active Theory renders nav in-canvas, "training you how to use the site without explaining anything." ≥3.
- **When an HTML nav survives, it is a transparent fixed corner:** logo plus a menu word or magnetic dot, floating over the canvas with no background fill and no border; the menu opens a full-screen overlay rather than the bar gaining a surface. Obys, Aristide Benoist. `(shipped)`.

In this archetype the nav-bar-gains-a-surface-on-scroll pattern is a category error: there is usually no bar to give a surface to.

### Motion and scroll

The AI-default: one `AOS`/IntersectionObserver `fade-up 20px, .6s ease-out` on every section, a uniform `translateY` parallax on the hero, nothing tied to the concept.

Winner motion is the medium. Reveals decode or unclip; scroll drives a single progress number a shader reads; transitions carry a physical or optical signature consistent across the whole site.

- **Objects rise from the ground as the intro:** the reveal *is* the world assembling. Bruno Simon: on start, "all the objects were going up from the ground while the [paper-unwrap] sound was playing." `(single-source, definitional for the stack)`.
- **Single `progress` 0→1 drives everything:** load-bearing architecture, not a single effect. One GSAP timeline with a custom ease tweens a number copied into a shader uniform each frame; the shader stays stateless, GSAP owns the curve. Guignand `(single-source)`, matching Igloo and Active Theory's GSAP-drives-shader model.
- **Scrub-linked next-project clip-path morph:** full-bleed unclip as the scroll reaches the page bottom. *Verified (Guignand):* `ScrollTrigger scrub: 1`; `insetV = max(0, 20 − 20·p)`, `insetH = max(0, 40 − 40·p)` → `inset(insetV% insetH% insetV% insetH%)`; background scale `1.3 − 0.3·p` (1.3×→1.0×); an SVG circle counter driven by `stroke-dashoffset = p·circumference`; a velocity ceiling skipping auto-nav if `getVelocity() > 2000`, and a 250ms commit timeout. `(technique, single-source)` for the numbers; the "preview expands into the next page" gesture is corpus-common.
- **Optically-signed scene transition:** chromatic aberration + displacement + frost between scenes, reused everywhere so the site has one look when it moves. *Verified curve (Guignand):* displacement and chromatic offset both follow `parabola(progress, 2.)`, peaking at 50%; the block-reveal mask uses pixelated UVs `step()` against the progress uniform. Igloo, verbatim from the case study: "a mix of chromatic aberration, tech displacement and frost effect". ≥2.
- **Scrub-blur depth carousel:** Kawase blur scales with scroll distance. *Verified (Codrops):* `scrub: 0.05`, blur `clamp(distance/maxDistance · 5, 0, 5)`, Kawase offsets 1/2/3, transition `duration: 1.5, power3.out`. *When:* horizontal media galleries. `(technique, single-source)`.
- **Reveal choreography timed to element count:** split-text reveals where stagger shrinks as the unit gets smaller, so the whole line lands tight. *Verified (Osmo/Codrops):* lines `duration 0.8, stagger 0.08`; words `0.6 / 0.06`; letters `0.4 / 0.008`; `yPercent 110→0`; ease `cubic-bezier(0.625, 0.05, 0, 1)`. `(technique)`: never verified against a named winner's bundle, so ship the pattern, not the exact curve.

### Text effects

The AI-default: `SplitText` + `stagger: 0.05, y: 20, fade` on the H1 and nothing else, plus a CSS `background-clip: text` gradient sold as kinetic.

Winner type is either **decoded** (scramble that resolves) or **kinetic** (letters scale/split/morph on scroll). In the WebGL stacks the type is rendered by the engine as SDF, so the effect is a texture operation, not a DOM animation.

- **Scramble-to-resolve decode, the signature.** Headline and label characters cycle through a punctuation-heavy set then settle, running *in parallel* with a clip-path wipe rather than after it. *Verified (Guignand):* charset `A!B@C#D$E%F&G*H?J[K]L{M}N=O+P-QRSTUVWXYZ`; clip-path `inset(0 0% 0 0)`, 0.6s `power2.out`; parent height locked via `getBoundingClientRect().height` before the split to stop reflow. Igloo does the same via SDF-offset scramble. ≥2.
- **Kinetic type on scroll, the signature for the typography stack.** Letters scale, split, and morph as the page scrolls, type carrying the layout instead of images. Obys Agency kinetic typography system. `(single-source as a named winner)`: stack-specific, not universal.
- **Per-char / per-line split reveal (supporting).** `yPercent 110→0` with count-scaled stagger. Connective tissue under the decode, not the headline moment. `(technique)`.
- **Physics text smash (accent only).** Characters fall and scatter under gravity. *Verified (Codrops GSAP Physics2D):* `velocity random(500,1000)`, `gravity 3000`, `rotation random(-90,90)`, fade `autoAlpha 0, 0.2s`. One deliberate moment (a 404, a manifesto line), never body copy. `(technique, single-source)`.
- **Variable-font weight tied to input.** Weight axis driven by mouse or audio amplitude. Igloo syncs particle and audio to motion, adjacent but not the same. `(shipped)`: ship no exact numbers.

### Cursor and pointer

The archetype where bespoke cursors live. The AI-default is a `mix-blend-mode: difference` white dot with ~0.15s lag and nothing else, a cursor that costs a library and adds no meaning. Winners bind the cursor to a mechanic, or leave the OS default because the whole surface is the pointer.

- **Magnetic elastic follower, the signature.** A dot, ring, or blob trails with spring easing, then snaps onto and scales around hoverable elements, pulling them slightly toward it. The default for typography/agency/portfolio builds. Obys, Cuberto (`mouse-follower`, GSAP v3), Lusion v3. ≥3.
- **WebGL flowmap cursor (velocity brush).** The pointer writes velocity into an RG texture, leaving a fading trail that distorts whatever sits under it, paired with an idle guard that stops the rAF loop after **90 frames** without cursor input. Guignand for the guard `(single-source)`; Active Theory canvas-cursor and Resn/aircord "3D WebGL cursor interaction" carry the family. ≥2.
- **Cursor-as-label / state morph.** The cursor swaps to a word ("drag", "view", "open") or an arrow near interactive zones instead of a tooltip. Draggable carousels, project tiles. Active Theory. `(shipped, corpus-common)`.
- **Deliberate default: no CSS cursor.** When the mechanic *is* the pointer, adding a bespoke cursor fights it. Bruno Simon drives a car (WASD; ZQSD on AZERTY layouts) plus click; the "click to start" gate and floor-tile path do the wayfinding a cursor would. `(single-source)` but the ceiling of the stack. A bespoke cursor is not mandatory; a meaningless one is worse than none.

### Loader effects

The one archetype where a loader is defensible, given heavy WebGL and asset payloads, but only as choreography tied to the concept. The AI-default is a centered `%` counter or CSS spinner over a blank page, then a hard cut to content.

- **Diegetic in-engine intro.** The loading moment is a real-time animation in the same shader style as the site, editable without re-renders. Igloo, verbatim from the case study: "animated in-engine using a combination of code and custom shaders", to "inject some additional tech vibes with an intro animation". Bruno Simon: objects rise from ground plus a paper-unwrap sound. ≥2.
- **Start button as audio-unlock gate.** A required click doubling as the intro trigger, because browsers block autoplay audio until interaction. Bruno Simon. `(single-source)` but a hard technical constraint, not a taste choice.
- **Preload racing inside the fade.** Image and code-chunk imports fire *before* the transition timeline starts and finish during the fade window. *Verified (Guignand):* WebGL, grid, side-text, and cursor fade together **0.3s `power2.inOut`**, content follows **0.35s at +0.25s offset**, giving a ~0.6s window the preloads race inside; `flushSync()` inside `document.startViewTransition()` prevents double-capturing the old DOM. `(technique, single-source)`.
- **Instant first paint is also valid.** The research-publication sub-stack (Thesephist, Ink & Switch) ships no preloader. A loader is earned by a heavy engine; a text-first experimental site gets none.

### Composition

Each winner varies its interactions across button ≠ link ≠ image ≠ nav, yet reads as one authored world because a single unifying rule governs all of them.

**Bruno Simon, unifying rule: everything is a physical object in one 3D world.**

| Element class | Interaction | Why it reads as one voice |
|---|---|---|
| Nav / menu | No HTML nav; sections are places to drive to; floor tiles form a path, walls bound space, panels label areas | Every UI is a 3D model obeying the same physics and matcap lighting |
| Button / CTA | 3D objects to drive into or click; "click to start" gate | Same collision and material system as the world — no CSS button exists to break the illusion |
| Link (project) | Camera tweens to an overhead read on entering the projects zone | Motion is camera plus easing, consistent with the car's momentum |
| Image / media | Textured surfaces in-scene (matcaps), not `<img>` | One rendering pipeline; no DOM layer to feel bolted on |
| Cursor | Deliberately absent — the visitor drives; the car is the pointer | A lag-dot would contradict "everything is physical" |
| Intro | Objects rise from ground plus paper-unwrap sound | The reveal is the world's physics booting — same system, first frame |

**Igloo Inc, unifying rule: one WebGL surface, one optical signature (ice + chromatic aberration).**

| Element class | Interaction | Why it reads as one voice |
|---|---|---|
| Nav / UI text | Entire UI in WebGL; labels scramble via SDF offset | Text is a texture op in the same renderer as the scene |
| Button / link | Glitch via a WebGL shader, not CSS clip/mask | Same shader vocabulary as the ice and the transitions |
| Image / scene | Procedurally-grown ice crystals; particles recolor by speed and glow as they reshape | One material language across every surface |
| Section transition | Chromatic aberration + tech displacement + frost | The optical signature tying intro, scroll, and hover into one look |
| Intro / loader | Real-time in-engine, same shaders as the site | No style seam between loading and loaded |
| Sound | Synced to particle motion | Every layer driven by the same timeline |

**The transferable rule.** Experimental variety coheres when a single substrate (Bruno's physics engine, Igloo's shader signature) renders every element class. The lazy build fails the opposite way: one identical CSS trick on top of a normal DOM, which reads as sameness *and* as bolted-on. The substrate comes first, and each element class expresses it differently.

## Page recipe

Three shapes hold this line, each defined by where the engine lives relative to scroll.

### Named page shapes

#### Shape A — World-as-page (no scroll)

**Fingerprint.** No vertical scroll, no section stack. The first fold *is* a 3D world; sections are physical rooms, landmarks, and zones discovered by moving a navigation primitive (a car, a walker, a camera) across a hand-coded landscape. The loader is the world booting; wayfinding is a floor-tile path plus a hand-drawn "click to start". Funnel jobs collapse into space: attention = the world rendering, understanding = intuitive controls within ten seconds, proof = the secret rooms the visitor discovers, close = an in-world sign-off. Usability rests entirely on the intuitiveness of the primitive.

**Ordered skeleton.** `world boot (loader) → spawn point with control affordance → drive/walk to discover landmarks (Home, Options, Achievements, Circuit, Behind-the-scene, Three.js Journey, Devlogs, Source code, Musics) → per-area rooms with bespoke interactions → in-world footer sign-off`.

**Fits.** Solo creative-developer portfolios, brand worlds, agency identity microsites, conference and experiential pages. Bruno Simon: copy `(winner-verified)`, engine model `(shipped)`.

#### Shape B — In-engine scroll journey

**Fingerprint.** Conventional top-to-bottom vertical scroll, every pixel rendered inside the WebGL engine, UI text, buttons, transitions included. Ordered zones read as one authored world because a single substrate renders them all; seams between zones are shader scene-transitions, not DOM section boundaries. Intensity climbs from an atmospheric intro to an interactive payoff, then rests. Igloo runs this in pure WebGL; Lusion runs a softer variant where mission-statement type is typeset over a live 3D field and the seams are scroll-driven reveals.

**Ordered skeleton (Igloo).** Intensity `[n]` is a comparative 1–10 estimate of attention load (defined in [Composition Chains](../winners/composition-chains.md)). `real-time in-engine intro (outdoor scene) [8] → per-project zones, each encased in a generated ice block [6–7] → interactive links = particle simulation forming a model per link [10, climax] → closing beat [4, rest]`. The case study describes "each project" generically.

**Ordered skeleton (Lusion, live-2026).** `hero statement H1 over 3D [7] → "Bold Ideas, Brought to Life" [6] → Featured Work reel [8] → "Where Creative Ideas Become Immersive Experiences" [6] → CTA "Step into a new world and let your imagination run wild" [7] → final CTA "Is Your Big Idea Ready to Go Wild?" [8, climax] → contact footer [3, rest]`. Seven zones, roughly 6–8 viewport-heights. All headings verbatim and in order by tag-strip.

**Fits.** Brand and product landings with narrative ambition, tech and crypto brands, studio flagships.

#### Shape C — Counter-boot index

**Fingerprint.** A numeric or typographic loader boots in a corner, then hands into a giant-type project index: case studies as a display-scale list (each a single "EXPLORE" link) or a numbered grid, rendered over WebGL imagery. No marketing hero and almost no prose; the type *is* the hero. Navigation is click-based with no scroll-jacking; clicking a project plays a JS/WebGL route morph; an About overlay is reachable from anywhere. Chrome is a thin transparent nav (word marks, optional clock); the pointer affordance is a bottom-centered indicator, not a lag-dot.

**Ordered skeleton.** `corner loader-counter (0→100) → giant-type project index (N projects as EXPLORE links / numbered grid, WebGL imagery) → click → in-engine route morph into case study → About overlay (clients, awards tally, sign-off) reachable anywhere`.

**Fits.** Freelance developer and designer portfolios, studio folios, agency work indexes. Aristide `(winner-verified)`, Obys grid variant `(shipped, via spatial-organic)`.

**Totals across the line.** Shape A: 0 scroll-heights (spatial). Shape B: 6–8. Shape C: the index is ~1–2 folds, with depth inside each project route. Climax placement is late and interactive in B and *on click* in C; rest is always a generative or contact footer.

### Hero architectures

**H1: World-boot hero (Shape A).** No DOM `<h1>`; the fold is the live 3D world. A hand-drawn "click to start" affordance doubles as the audio-unlock gate. Nav does not exist as a bar; landmarks are the nav. The CTA is the world itself.

| Element | Order | Transform | Duration | Easing |
|---|---|---|---|---|
| World canvas | 1 | fade/compose in-engine | — | — |
| Ground objects | 2 | rise from ground (physics drop-in) | staggered | physics: Cannon.js on the 2019 build `(stated)`; the 2025 rebuild's engine is unnamed on its award page, Rapier `(stated, unconfirmed)` |
| "Click to start" annotation | 3 | draw-in (hand-drawn) | — | — |
| Audio | 4 | unlocks on the start gesture | — | — |

**H2: In-engine statement hero (Shape B).** A real-time animated intro resolves into an atmospheric scene (Igloo: outdoor scene, ice metaphor) or a mission-statement `<h1>` typeset over a live 3D field; Lusion: *"We create 3D visual storytelling and interactive web experiences that help brands stand out"*. Nav is transparent and minimal; the CTA is a soft "CONTINUE TO SCROLL" or "Let's talk".

| Element | Order | Transform | Duration | Easing |
|---|---|---|---|---|
| In-engine intro | 1 | real-time shader animation | — | — |
| Scene/statement resolve | 2 | intro dissolves into fold (chromatic/frost seam) | — | — |
| H1 statement (Lusion) | 3 | SplitText line reveal, `yPercent 110→0` | ~0.8s / stagger 0.08 | `cubic-bezier(0.625,0.05,0,1)` |
| Scroll cue | 4 | fade in | — | — |

The Lusion row's SplitText numbers are `(technique, single-source)`, Codrops/Osmo values never verified against Lusion's own bundle: the pattern holds, the curve does not.

**H3: Giant-type index hero (Shape C).** A corner loader-counter hands into a display-scale project title or a numbered grid. No subhead. The only pointer-follower is a bottom-centered explore indicator, never a lag-dot.

| Element | Order | Transform | Duration | Easing |
|---|---|---|---|---|
| Loader counter `#load` | 1 | digits count 0→100, exit `translate3d(-110%,0,0)` | — | — |
| Giant title `#a-nif-w` | 2 | reveal | — | — |
| WebGL homepage imagery | 3 | shader-render behind type | — | — |
| Explore indicator `.e` | 4 | `translate3d(0,-110%,0)` reveal | — | — |

**Named CSS values, Aristide, live `d.css` `(winner-verified)`:**

```css
#load { position:absolute; z-index:9998; top:35px; left:38px;
        font-family:"TNY"; font-size:50px; line-height:44px;
        letter-spacing:-.01em; opacity:1 }
#a-nif-w { font-size:calc(17.5vh + 100px); line-height:calc(13.0725vh + 74.7px) }
.e   { bottom:49px; left:50%; transform:translateX(-50%); pointer-events:none }
.e-s { margin:13px auto 0; width:14px; height:14px; overflow:hidden }
.e-s div { transform:translate3d(0,-110%,0) }
```

The indicator selectors are classes. `d.css` carries no `clip-path` and no CSS page-transition rules; the morphs live in the JS bundle. File sizes measured live: `d.css` **9,485 bytes** (~9.5KB minified), `d.js` **69,520 bytes** (~67.9KB pre-gzip), single `/static/js/d.js` from a custom Rollup bundler. Fonts are declared in an inline `<style>` in the head, not in `d.css`: `TNY` (`t.woff2`, weight 400) and `jws` (`jw.woff2`, weight 700), with `body{font-family:"jws"}`. The designer attributions (Timmons NY by Matt Willey; Jon Way Studio) are plausible but unprovable from the woff2 filenames; the weights are verified, the names are not.

### Loader and intro

The loader is never a spinner. It is the concept booting, and it hands off without a hard cut.

- **Igloo** `(shipped, case study)`. The intro is animated in-engine with code and custom shaders, then transitions to the outdoor scene. No DOM preloader; loader and site share one renderer.
- **Bruno Simon** `(shipped, single-source)`. Objects rise from the ground with a paper-unwrap sound; the required start button doubles as the audio-unlock gate.
- **Aristide** `(winner-verified)`. `#load` is a TNY-typeset numeric counter at 50px in the top-left corner, counting 0→100, each digit exiting on `translate3d(-110%,0,0)`. The rendered loader div reads `<div id="load">0 0 1</div>` mid-count and "1 0 0" at completion, handing straight into the project index. The counter uses the same display face as the hero title: identity, not generic chrome.
- **Absence is data.** The research-publication sub-stack ships instant first paint and no loader. The reveals are the intro.

**Handoff rule.** The loader shares the site's own type, shader, or material with the first fold, so the boot dissolves into the hero rather than being replaced by it.

### Route transitions

- **Aristide** `(winner-verified structure; mechanism in JS)`. Click-based navigation with keyboard support and deliberately no scroll-jacking. Clicking a project plays a JS/WebGL transition (Awwwards Animations/Transitions sub-score **9.20**). Each of the 30 case studies carries a custom color scheme and per-title letter positioning. The About overlay is reachable from anywhere with transitions that differ per entry point. The rendered index numbers projects `01/30, 02/30…`.
- **Igloo** `(shipped, case study)`. Scene-to-scene transitions are "a mix of chromatic aberration, tech displacement and frost effect", all shader-driven inside the one renderer.
- **Guignand** `(technique, single-source)`. The exact clip-path route language the awarded sites keep closed, verbatim from Codrops: content fadeout **0.35s `power2.inOut`**, WebGL background fadeout **0.3s `power2.inOut`**, clip-path reveal **0.6s `power2.out`**; `Math.max(0, 20 - 20*progress)`, `Math.max(0, 40 - 40*progress)`, background scale `1.3 - 0.3*progress`; scramble charset `'A!B@C#D$E%F&G*H?J[K]L{M}N=O+P-QRSTUVWXYZ'`; the flowmap's rAF loop suspends after **90 frames** without input; `flushSync()` inside the page-transition wrapper.

**Rhyme.** In-engine sites make the route transition rhyme with the loader because both are the same shader pipeline. Aristide's transition language rhymes with its counter loader through the shared TNY display face and the same `-110%` slide idiom.

### Copy voice

**Bruno Simon** `(winner-verified, raw markup)`. Hero: "My name is Bruno Simon, and I'm a creative developer (mostly for the web)." Sub: "This is my portfolio. Please drive around to learn more about me and discover the many secrets of this world." Microcopy: "And don't break anything!" · "Whispers are messages left by visitors." UI labels: "Respawn" · "Leave a whisper" · "Start chating" *(sic)*. Sign-off: "Thank you for visiting my portfolio!" · "— Bruno".

**Lusion** `(winner-verified, live-2026)`. H1: "We create 3D visual storytelling and interactive web experiences that help brands stand out". Section headings: "Bold Ideas, Brought to Life" · "Where Creative Ideas Become Immersive Experiences" · "Is Your Big Idea Ready to Go Wild?". Body: "We do not chase trends or produce work that looks like everyone else." CTA labels: "Let's talk", "CONTINUE TO SCROLL", "Play Reel". Footer: "©2026 LUSION Creative Studio" · "Built by Lusion with ❤️".

**Obys Agency** `(shipped, via spatial-organic)`. Nav: "Work" · "About". Chrome: "CET 00:00 AM". Footer blurb: "The studio is shaped by people who care deeply about design and the process behind. Each project becomes a case study and a meaningful part of our portfolio, developed with care and attention." Footer: "All rights reserved. ©2026 Obys" · "Contact: info@obys.agency".

**Aristide Benoist** `(winner-verified, rendered DOM)`. Labels: "PROJECTS" · "ABOUT" · "CLOSE" · "EXPLORE". Identity: "INDEPENDENT DEVELOPER". Status: "AVAILABLE APR. 2023" *(stale, left in)*. Footer: "ALL RIGHTS RESERVED" · "ARISTIDE BENOIST 2026®".

**Voice formula.** Two poles of person: warm first-person or first-person-plural for makers who front themselves (Bruno, Lusion), near-personless terse labels for the studios (Obys, Aristide). Sentence length is either one humane full sentence or no sentence at all; the index stack speaks in one- and two-word labels. Verb temperature is inviting imperatives that hand the user the mechanic: "drive around", "explore", "go wild", "let your imagination run wild"; the verb points at action inside the site, not at a purchase. Punctuation stays minimal, an exclamation only where the voice is playful. The line refuses feature lists, adjective stacks, benefit bullets, and hedging. The copy recedes so the engine can speak.

### Imagery art direction

Imagery is generated or real-time inside the engine, never stock photography, and holds one coherent world-material per project.

- **Igloo** `(shipped)`. Procedurally-grown ice crystals: verbatim, a "custom algorithm that mimicked the growth of ice crystals inside a container", with "each project… represented by an object encased in ice". Procedural growth prevents monotony on scroll; the grade leans on chromatic aberration and frost; UI text lives in the same WebGL layer via SDF-offset scrambles.
- **Bruno Simon** `(shipped)`. Low-poly primitives, matcap materials, warm-light landmarks on dark navy, hand-drawn UI annotations: the found-not-marketed register.
- **Aristide** `(winner-verified)`. WebGL-rendered homepage imagery behind display type; 30 case studies each with its own color scheme and per-title letter positioning; the compressed TNY face used as image, not just as text. WebP delivery is conditional on capability detection (`window._A.webp:false` in the fetched context) and stays unconfirmed.
- **Lusion** `(shipped)`. Cinematic real-time 3D mograph authored in Houdini.
- **Obys** `(shipped)`. Project thumbnails in a numbered grid with kinetic type carrying the visual weight.

The line splits deliberately by project (Aristide's per-project color, Resn's "every case study has its own world") while the substrate stays single so the site reads as one authored world.

### Footer

The footer restates identity and contact in the site's own voice; studios add operational chrome. The oversized-wordmark footer common to editorial is not the default here; identity already lives in the type or the world.

- **Lusion** `(winner-verified, live-2026)`. Functional-plus: "©2026 LUSION Creative Studio", two routed emails (`hello@lusion.co`, `business@lusion.co`), a physical address ("Suite 2, 9 Marsh Street, Bristol, BS1 4AA, United Kingdom"), and a signed "Built by Lusion with ❤️".
- **Obys** `(shipped, via spatial-organic)`. Contact-first: a one-sentence studio blurb, `info@obys.agency`, the persistent "CET 00:00 AM" clock, "All rights reserved. ©2026 Obys".
- **Aristide** `(winner-verified)`. The About overlay functions as the footer: a clients list (BEAR GRYLLS, DRIBBBLE, FUSE PROJECT, GOOGLE, HIMS & HERS, INSTAGRAM, JACQUES MARIE MAGE, MGM STUDIOS, NETFLIX, OBAMA FOUNDATION, RAPPI, SUPER FRIENDLY, TWITCH, WATSON) and an Awwwards tally parsed count-before-label: Independent of the Year ×2, Site of the Month ×3, **Site of the Day ×30, Developer Award ×27**, Mobile of the Week ×6, Mobile Excellence ×22, closing on a display-set "ARISTIDE BENOIST 2026®". The sign-off and loader share `font-family:"TNY"`; the footer is typeset, not templated.
- **Bruno** `(winner-verified copy)`. In-world sign-off: "Thank you for visiting my portfolio!" / "— Bruno".

### Spectacle menu

- **Bruno Simon.** Driving the car through the low-poly town, discovering secret rooms and visitor whispers. Trigger: the start gesture. Payoff: physics to push against. Replayable because it is a game, not a scroll.
- **Igloo Inc.** The links section as an "interactive particle simulation that would form different models based on the selected external link". Trigger: hovering or selecting a link. Payoff: matter forming meaning in real time. Replayable because each link is a different formation.
- **Aristide.** The click-into-project route morph (Animations/Transitions **9.20**): the giant TNY title and its WebGL imagery transform into the case study, each project in its own color. Replayable because 30 projects means 30 distinct entries.
- **Lusion.** The Featured Work reveal and "Play Reel": the cinematic real-time mograph payoff.
- **Guignand** `(technique)`. Scroll to page bottom and the next project unclips full-bleed while the title scrambles to resolve.

Each spectacle is *stateful* (a physics world, a per-link formation, a per-project morph, a scrubbed reveal), so a second run differs from the first. The line never ships a one-shot hero animation as its spectacle.

### Page-level anti-signals

One list for the line, element level, page level, and mid-page together. Absent from every winner examined:

- **Pale, washed-out tint fill on button hover** (a 10–20% brand-alpha sweep). The single clearest tell. Winners fill to a full opaque token or replace the fill with magnetic/WebGL response.
- **One identical hover cloned onto every element class.** Every winner differentiates button vs. link vs. image vs. nav.
- **Scrolled solid nav bar with a contrasting `border-bottom`.** No corpus site does this; most have no persistent HTML nav bar at all.
- **CSS underline-draw as the signature text-link move.** Replaced by scramble-decode or magnetic response.
- **Generic `fade-up 20px` as the only reveal.** Replaced by scramble plus clip-path, physics, or clip-morph; mid-page, reveals are masked `translate3d` plus SplitText letter/word/line staggers, or nothing.
- **Spinner or bare `%` counter preloader untied to the concept.**
- **`mix-blend-mode` lag-dot cursor that adds no mechanic.** Aristide's body cursor computes to `auto` in the rendered DOM, with the bottom-centered `.e` indicator as the only follower; Bruno omits a cursor because the car is the pointer.
- **Framework-template motion** (AOS, one easing everywhere). The archetype is hand-coded from primitives.
- **A single CSS `background-clip: text` gradient sold as kinetic type.** Kinetic here means letters scale, split, morph, or decode.
- **A card-grid opener** with a conventional hero band above feature cards. The first fold is a world, an in-engine statement, or a giant-type index.
- **Stock photography.**
- **Feature-list or adjective-stack copy.**
- **A conventional footer nav sitemap.** The footer is a payoff, a signed identity block, or contact-first chrome.
- **A conventional scrolling prose middle** in the spectacle or index registers. It is virtualized into the engine or replaced by a hover-live index; a 7.2–7.4 build's dead prose section is itself slightly off-archetype here.
- **Hover on running body prose.**
- **Lenis or Locomotive** as the smoothing layer, and **GSAP ScrollTrigger scrub as the mid-page spine** in the readable index build.
- **Motion decor on the reading column in the quiet register.** Aliveness there is typographic: marginalia, sidenotes, hanging figures, randomized stamps.

## Mid-page aliveness

What keeps the middle of the page alive: the zone between hero and footer that reads dead on merely-good 7.2–7.4 builds.

### The register split

**Read depth.** Lusion v3 (live browser + `about.CNa9RfUh.css` 90,367B + `hoisted.CJiXW_YI.js` 1,251,704B), Aristide Benoist 2021 (`d.css` 9,485B + `d.js` 69,520B), Ink & Switch (`base.css` 16,645B + `/index.css` 6,474B), Thesephist (`main.css` + `paper.min.css`) are read at source level. Igloo and Bruno rest on award pages and a case study. Obys is a JS shell returning no readable markup to a non-JS fetch; its values are carried from [`spatial-organic.md`](./spatial-organic.md), which read the rendered DOM.

**The register split governs every answer.** This archetype is not one thing:

- **Spectacle** (Lusion, Igloo, Bruno). No conventional scrolling DOM middle exists. The page is a fixed WebGL stage; the middle is a real-time simulation.
- **Index** (Aristide, Obys). The middle is a giant-type index over WebGL, click-routed.
- **Research-publication quiet** (Ink & Switch, Thesephist). A genuine prose middle, kept alive by typography and structure, not motion.

### Inventory by register

**Spectacle: the middle is deleted and replaced by a live engine.**

The load-bearing finding, measured live on Lusion: `document.body.scrollHeight` = 676px and `window.innerHeight` = 676px, one viewport, with `scrollY` = 0. **The body does not natively scroll.** Three live canvases: main **2160×1014**, a sound-viz **90×90**, and a third measuring 2163×1017 backing store at **0×0 CSS size**, present but not laid out. Scrolling drives a custom in-engine journey through zones. There is no tall column of prose to go dead.

- **Idle substrate never sleeps.** With zero user input, a `requestAnimationFrame` probe counted **54 ticks in 1.118s = 48.3 ticks/sec** still running. The render loop is welded to time, not to scroll or hover. The single biggest source of mid-page life on the spectacle register: at rest, the canvas is still rendering. A rAF counter measures the tab's compositor cadence, which tops out at refresh rate, so it corroborates the continuous loop rather than isolating the engine's own draw calls.
- **SplitText line/word/char reveals.** The live Lusion DOM carries **557 total spans, 517 single-character spans, 541 no-class spans**, the SplitText signature. The bundle carries `splitText` ×23. Text lands per line and per word on entry.
- **Section transitions as shader seams.** Chromatic aberration, displacement, frost between zones (Igloo, `(shipped)`).
- **Scroll-scrubbed real-time assembly.** The scene builds as the page advances (Igloo, `(shipped)`).

**Index: the middle is a hover-live giant-type index.** Aristide `d.css` / `d.js`, all counts exact:

- **Masked `translate3d` reveals.** `transform:translate3d(0,101%,0)` ×3, `(0,-110%,0)` ×2, `(-110%,0,0)` ×2 on overflow-masked rows; standalone `will-change:transform` exactly **13** times. Digits and index titles slide in and out of masks. The counter boots 0→100, digits exit `translate3d(-110%,0,0)`, then the index title reveals; no marketing prose between.
- **Hover-on-row pseudo-element.** `#n2:hover>div:last-child .n2::after` and `:hover::after` animate a line on the index entry.
- **WebGL imagery behind type plus click-morph route.** Per-project color and letter positioning across 30 entries; clicking morphs the index title and its WebGL image into the case study. The middle is the index, alive because each row hovers and each click transforms.
- **Token census in `d.js` (69,520B):** `raf` 17 + `Raf` 20 = **37**, `cursor` **14**, `mouse` **13**, `split` **9**; `lenis`, `locomotive`, `gsap`, `ScrollTrigger`, `scrub` all **0**. Exactly one `cursor:pointer` rule in `d.css` and no other cursor rule; no custom-cursor CSS at all.

**Research-publication quiet: the middle is real prose, alive typographically.**

Ink & Switch `base.css` + `/index.css` `(winner-verified CSS; site is award-unverified, not an Awwwards submission)`:

```css
margin-left: -1.8em;                              /* hanging marginalia */
right: -15rem;                                    /* figure caption in the right gutter */
margin-top: calc(-24px * var(--move-up) - 13px);  /* sidenote aligned to its referenced line */
.lab-notes-stamp        { rotate: calc(var(--randA) * 5deg - 4deg) }
.lab-notes-stamp:hover  { opacity: calc(var(--randB) * 10% + 90%) }
a:hover, a:focus-visible { color: var(--link-color); background-size: 100% 100px }
.newsletter-form label:hover span { color: black }
```

Per-instance CSS-variable randomness gives the page a hand-placed, non-templated feel at rest. Drop-cap logos hang off the left edge; custom counters and gutter icons ship as masked SVG. `scroll-behavior: smooth` (×1) and `position: sticky` (×2) live in `/index.css`. Motion in the reading column is near zero; aliveness is structural and typographic.

Thesephist `main.css` / `paper.min.css` `(winner-verified CSS; award-unverified)`:

```css
main a       { text-decoration-color: var(--accent); text-decoration-thickness: 2px;
               transition: text-decoration-color .2s }
main a:hover { text-decoration-color: var(--foreground-light) }
```

`main.css` carries 0 `@keyframes`, 0 `animation:`, 0 `scroll-behavior`, and exactly **1** `transition:`, the underline. `paper.min.css` has one hover rule, `.paper.movable:focus,.paper.movable:hover{…}` with `transition:transform .15s,box-shadow .15s`. The hero artifact is a self-built spinning point/ASCII torus referenced as `/js/torus.min.js`, on Linus Lee's own `torus` reactive framework: a hero artifact, not a mid-page effect.

### Hover on text

The tier ships text-hover on **nav labels, buttons, index rows, and links, never on running body prose.** A hard data point: prose-paragraph hover is not a technique at this tier, so dead prose cannot be fixed by adding hover to paragraphs.

- **Letter-clone roll-swap on nav labels.** Lusion `(winner-verified)`. `.header-menu-link` stacks `.header-menu-link-text` + `.header-menu-link-text-clone` + `.header-menu-link-background`, the fill transforming in. Class counts in `about.CNa9RfUh.css`: `.header-menu-link` ×28, `-text` ×4, `-text-clone` ×4, `-background` ×2. The clone stack is pre-built into the markup: `<span class="header-menu-link-text">Home</span> <span class="header-menu-link-text-clone">Home</span>` plus a `-background` div and an SVG. Cloning is **word-level**, not per-character: the doubled labels are "Home Home", "About us About us", "Projects Projects", "Contact Contact". Text and clone spans roll on `transition:.4s color,.4s transform cubic-bezier(.4,0,.1,1)`; the SVG icon rule uses `transition:.4s color,.2s .2s transform cubic-bezier(.4,0,.1,1)`.
- **Index-row `::after` material.** Aristide `(winner-verified)`. A pseudo-element line on the giant index entry, not a color sweep along prose.
- **Link underline-color shift (quiet register).** Thesephist `(winner-verified)`. A 2px accent underline shifting color on hover. Header links draw the underline in on hover.
- **Link highlight-sweep (quiet register).** Ink & Switch `(winner-verified)`. A material highlight grown via `background-size`, plus form-label hover and stamp-opacity hover.

No heading, paragraph, or list-row of body copy carries a hover response anywhere in the read CSS. Weight and optical-size shifts on hovered prose, per-char rises on hovered headings, background highlights on prose: none appear. A text-hover signature belongs on nav labels, index rows, or links, never on the prose column.

### Re-fire behavior

The law holds at this tier, but the mechanism is register-specific and mostly not scroll-coupled.

- **Decor re-plays on time, not scroll (spectacle).** The Lusion render loop runs at 48.3 ticks/sec at idle with no input. This decor never stops and never needs a scroll pass to re-fire; it is a continuous simulation. Shader seams between zones re-fire on every zone crossing (Igloo, `(shipped)`).
- **Content reveals fire once and persist.** SplitText line and word reveals settle on entry; Aristide's masked `translate3d` digits and titles exit into place once per route. No evidence of content re-hiding to re-reveal on scroll-up.
- **The index register does not scroll at all.** Aristide's `d.js` contains no `ScrollTrigger`, `scrub`, `lenis`, or `locomotive` tokens: click-routed, no scroll-jacking. There is no up/down re-fire because there is no scroll spine; the route morph fires per navigation.
- **The quiet register re-fires nothing.** No scroll-linked decor, no re-playing reveals; CSS-native `scroll-behavior:smooth` and static prose.

The re-playing channel here is rarely scroll-driven. The spectacle tier's is a continuously-rendering engine, not a scroll-scrubbed text effect; the index and quiet tiers ship essentially no scroll-replayed decor.

### Smooth scroll

Smoothing is bespoke or native at this tier: Lenis and Locomotive, the corporate/editorial default smoothers, are absent from every readable bundle on this line.

- **Lusion (spectacle).** `window.Lenis`, `LocomotiveScroll`, `ScrollTrigger`, and `gsap` all absent from `window`; `document.documentElement.className` === `"is-desktop is-ready is-white-bg"` exactly. Token census in the 1.25MB `hoisted.CJiXW_YI.js`: `splitText` ×23, `matcap` ×58, `raF` ×28, `requestAnimationFrame` ×3; `lenis`, `Lenis`, `locomotive`, `Locomotive`, `ScrollTrigger`, `scrolltrigger` all **0**. Smoothing is hand-rolled inside the canvas: the wheel feeds an inertial journey rendered in WebGL via the engine's own rAF loop. `(winner-verified)`
- **Aristide (index).** Zero smooth-scroll-library tokens in 69,520B of `d.js`; click-routed. Smoothing is not applicable; there is no long scroll to smooth. `(winner-verified)`
- **Ink & Switch (quiet).** CSS-native `scroll-behavior:smooth` only, no JS inertia. Thesephist: none. `(winner-verified)`

Smoothing on this line is neither near-universal nor library-driven. The spectacle sub-stack rolls its own in-engine inertia, the index sub-stack routes around scroll, the research sub-stack uses native or nothing. A build reaching for Lenis to feel like this tier is copying the wrong layer; the feel comes from the engine, not a wheel smoother.

### Routing the dead middle

The tier has three real answers, and a build should route to one rather than sprinkle text effects on a prose column:

1. **Virtualize the middle into a live substrate:** a canvas or engine that renders at idle. The middle is alive because it is a continuous simulation replaying on time, not because prose has hover.
2. **Convert the prose middle to a hover-live giant-type index:** masked `translate3d` row reveals, `::after` hover material, click-morph route. Click-routed, no smooth-scroll needed.
3. **Commit to the quiet research-publication register:** keep genuine prose and make it live through typographic structure: hanging marginalia, gutter sidenotes aligned to their reference line, randomized hand-stamps, one hero artifact. At this register the tier ships almost no text motion, and scroll-linked text effects would be off-register.

Scroll-replayed text effects are a signature of other archetypes (editorial, bold-maximal), not the experimental >8 tier.

## Refuted

- **"Lusion v3 was a CSSDA Website of the Year 2023 nominee"** — understated: it is the **winner**, 9.27, and Best Agency Site, per the [CSSDA 2023 Website of the Year winners post](https://www.cssdesignawards.com/blog/2023-website-of-the-year-winners/394/) and the [WOTY winners list](https://www.cssdesignawards.com/woty-award-winners); it also holds CSSDA Website of the Month Oct 2023. The same site holds Awwwards Developer Site of the Year 2023 beside its Site of the Year 2023 ([archived Annual Awards 2023](https://web.archive.org/web/20240307133625id_/https://www.awwwards.com/annual-awards-2023/)) and FWA of the Day 21 Sep 2023, FWA of the Month Sep 2023 and FWA of the Year 2023 ([FWA case record](https://thefwa.com/api/cases/lusion-v3)).
- **"Igloo's footer is a generative particle-journey payoff"** — unsupported. The cited Awwwards case study describes no footer particle journey, only a previs animation and the links particle simulation.
- **"Igloo's Shape B skeleton runs three ice-block project zones"** — unsupported. The case study says "each project" generically; no count of three is stated.
- **"`#e { bottom:49px… }` and `#e-s` 14×14 are id selectors"** — false: both are classes in `d.css`, `.e` and `.e-s`, with the reveal on `.e-s div`. The values are right, the selector type wrong.
- **"Aristide's body cursor computes to `default`"** — false: `auto` in the rendered DOM. The load-bearing "no lag-dot" holds.
- **"Lusion's H1 SplitText values are winner behavior (`yPercent 110→0`, ~0.8s, stagger 0.08, `cubic-bezier(0.625,0.05,0,1)`)"** — unsupported: `(technique, single-source)`. The numbers were never verified against Lusion's bundle.
- **"Lusion live DOM has 429 split-text spans"** — false: two stable probes measured **557 total spans / 517 single-character spans**, and the count is view- and zone-dependent rather than fixed. Hundreds of char spans and per-char reveals survive; 429 does not.
- **"PPllaayy" / "RReeeell" as evidence of per-character cloning** — false. Live DOM shows **word-level** cloning on nav words ("Home Home", "About us About us", "Projects Projects", "Contact Contact"). The PLAY button reads plain `"PLAY"` with no clone and no per-char split, and no "Reel" element exists in the DOM. The roll-swap mechanism is independently confirmed from the header innerHTML.
- **"Bruno's 8.04 overall belongs to the 2025 rebuild"** — false: Design 7.94 / Usability 7.55 / Creativity 8.95 / Content 8.13 / Overall 8.04 belong to the **2019 build**, SOTD 11 Nov 2019, Developer Award 8.17. The 2025 rebuild is a separate entry: SOTD 21 Jan 2026, Design 8.05 / Usability 7.83 / Creativity 8.62 / Content 8.18 / Overall 8.11, Developer Award 7.65. Both sit below 8.5, so the ceiling finding is unaffected.
- **"Aristide SOTM Jun 2021, overall ≈8.02"** — false on the score: Portfolio 2021 is SOTD **24 Jun 2021** at overall **8.01**, and its SOTM Jun 2021 is carried by a dedicated Awwwards announcement page (`…aristide-benoist-portfolio-2021-wins-site-of-the-month-june-2021.html`), with 5 SOTM on the profile ([`../winners/studio-unseen-benoist.md`](../winners/studio-unseen-benoist.md)).
- **"On hover all four Lusion nav classes transform with `transition:.4s color,.2s .2s transform cubic-bezier(.4,0,.1,1)`"** — false: that string governs the SVG-icon rule. Text and clone spans use `.4s color,.4s transform` on the same curve.
- **"Aristide ships a filmstrip scrubber"** — false: `d.js` carries zero scroll and scrub tokens, and a scroll-scrubbed filmstrip cannot coexist with a click-routed build.
- **"Lando Norris's Site of the Year 2025 rests on the OFF+BRAND case study alone"** — false: the [Awwwards Annual Awards winners page](https://www.awwwards.com/annual-awards/winners) lists Lando Norris as Site of the Year 2025 (43 votes) and Site of the Year Users' Choice 2025 (596 votes), Messenger as Developer Site of the Year 2025, and Immersive Garden as Agency of the Year.

## Could not verify

- **Aristide's WebP delivery** (Imagery art direction). `window._A.webp:false` in the fetched context; WebP is served on capability detection, with no positive proof read.
- **Lusion's SOTY 2023 peer-vote tally (95/220).** Single-source; the title itself is verified on the Sites-of-the-Year listing and the archived annual page.
- **The Aristide typeface names** (Hero architectures). Timmons NY by Matt Willey and Jon Way Studio are unprovable from the `t.woff2` / `jw.woff2` filenames; weights 400 and 700 are verified.
- **Bruno's landmark list** (Home, Options, Achievements, Circuit, Behind-the-scene, Three.js Journey, Devlogs, Source code, Musics). Carried from secondary sources, not walked in the live world.
