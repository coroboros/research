---
title: "Brutalist — Effect Palette, Page Recipe, Mid-Page Aliveness"
date: "2026-07-30"
author: "Coroboros"
tags: ["web-design", "awwwards", "cssda", "brutalist", "neo-brutalism", "effect-palette", "page-recipe", "mid-page-aliveness", "motion-design", "gsap", "lenis", "scroll-driven-animation", "webgl", "glitch", "typography"]
sources:
  - "https://www.awwwards.com/sites/flowfest-2025"
  - "https://www.awwwards.com/sites/sui-overflow-2025"
  - "https://www.awwwards.com/sites/naked-city-films"
  - "https://www.awwwards.com/sites/eloyb-design"
  - "https://www.awwwards.com/sites/treize-grammes"
  - "https://www.awwwards.com/sites/amaterasu"
  - "https://www.awwwards.com/sites/design-thinkers-2020"
  - "https://www.flowfest.co.uk/"
  - "https://eloyb.design/"
  - "https://www.nakedcityfilms.com/"
  - "https://overflow.sui.io/"
  - "https://13g.fr"
  - "https://slater.app/14984/39049.js"
  - "https://slater.app/14984/39050.css"
  - "https://cdn.prod.website-files.com/682310547ba9eeb97324a89e/css/flowfest-2025.webflow.shared.d5970e214.css"
  - "https://tympanus.net/codrops/2025/10/15/from-blank-canvas-to-mayhem-eloy-benoffis-brutalist-glitchy-portfolio-built-with-webflow-and-gsap/"
  - "https://tympanus.net/codrops/2026/01/19/naked-city-films-designing-and-building-a-website-that-refuses-to-stand-still/"
  - "https://tympanus.net/codrops/2024/10/10/case-study-treize-grammes-2024/"
  - "https://tympanus.net/codrops/2026/02/18/joffrey-spitzer-portfolio-a-minimalist-astro-gsap-build-with-reveals-flip-transitions-and-subtle-motion/"
---

# Brutalist — Effect Palette, Page Recipe, Mid-Page Aliveness

The brutalist line tops out around 7.5 on the Awwwards jury, and its mid-page stays alive by layering a scrubbed decor texture behind fire-once content reveals. Per-effect recipes read off awarded sites in the brutalist / neo-brutalist line, the ordered page scaffold that carries them, and what the line's highest scorers ship to keep the zone between hero and footer alive. Every recipe cites a named winner with its award, its date, and values read from its live CSS, its shipped JS, or a builder-authored case study. Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md) §1.2.

## Corpus

Award, date, score, credits, register, and how deeply each site was read.

Evidence tags: `(winner-verified)` = read from the awarded site's live CSS, JS, or DOM; `(shipped)` = observed live or in award-page media, implementation not read; `(technique)` = a documented method, typically Codrops; `(design-canonical)` = a documented design system with no verified award; `(single-source)` = one site only; `[CSS]` / `[JS]` = quoted from shipped code; **verified** / **stated** / **observed** = measured in source / claimed by the builder / seen but not read; `(stated, unconfirmed)` = a builder claim the source read could not confirm; `(inferred)` = derived from indirect evidence.

| Site | URL | Award and date | Jury | Credits | Register | Evidence read |
|---|---|---|---|---|---|---|
| **FlowFest 2025** | `https://www.flowfest.co.uk/` | Awwwards Site of the Day (SOTD) 29 Jul 2025 + GSAP Site of the Week + Developer Award | **7.36** | Dennis Snellenberg, Osmo, Ilja van Eck, Isabel Edwards | warm-illustrated: butter / pink / orange (Webflow `:root` tokens below), round buttons, chunky type | live CSS + 982KB raw HTML + the full Slater bundle (`https://slater.app/14984/39049.js`, 31.6KB raw JS; `https://slater.app/14984/39050.css`) + `flowfest-2025.webflow.shared.d5970e214.css` |
| **Eloy Benoffi** | `https://eloyb.design/` | Awwwards Honorable Mention (HM) 4 Jul 2025 + GSAP Site of the Day + CSSDA Best UI / Best UX / Best Innovation | HM, no jury number published | — | glitch / terminal: charcoal `#2B2C27`, Px437 VGA bitmap font | live CSS + 1.46MB raw HTML with inline GSAP + `eloyb-design.webflow.shared.min.css` (58KB) + Codrops case study, 15 Oct 2025 |
| **Sui Overflow 2025** | `https://overflow.sui.io/` | Awwwards SOTD 15 Apr 2025 | **7.48** | HOLOGRAPHIK + Ilja van Eck | saturated / structural: 2px hard borders, 0-radius controls, Sui-blue accent | live CSS (2025 tokens) + 451KB raw HTML of the 2026 successor edition now served at the URL; structure and copy below are the successor's |
| **Naked City Films** | `https://www.nakedcityfilms.com/` | Awwwards SOTD 23 Jan 2026; Awwwards tags WebGL + GSAP | **7.34** | SavoirFaire / Tomas Kmet | industrial / editorial: off-white on black, Haas Grotesk, WebGL scene | live CSS (the origin now returns `403`) + Codrops case study, 19 Jan 2026 |
| **Treize Grammes** | `https://13g.fr` | Awwwards Honorable Mention 11 Oct 2024 | HM | Thomas Carré / 13G | activation-concept brutalism: the fake-button-to-video morph | 423KB raw HTML (strings, computed hexes, script srcs) + `13g.webflow.shared.min.css` + the production bundles `main.js` (10.7KB) and `loader.js` (1.7KB) + Codrops case study, 10 Oct 2024 |
| **Joffrey Spitzer** | — | Awwwards nominee | — | — | minimalist with a brutalist edge, Astro + GSAP + Swup; borderline archetype, carried as **single-source / supporting** for its stepped preloader, Flip handoffs, and mask reveals | Codrops case study only, 18 Feb 2026 |
| **DesignThinkers 2020** | `https://www.awwwards.com/sites/design-thinkers-2020` | Awwwards Honorable Mention | HM | — | inverted-color hover brutalism; **pre-window (2020), supporting** only | award page |
| **Amaterasu** | `https://www.awwwards.com/sites/amaterasu` | Awwwards SOTD 14 Nov 2024; Awwwards tags Technology / 3D / Storytelling | **7.54** | — | not brutalist ("organic" is a reader's label, not an Awwwards tag); cited only to fix the archetype ceiling | award page |

Amaterasu is carried for its score alone; its WebGL point-cloud is not a brutalist build reference. Rogier de Boevé is dystopian 3D, outside the line. Cuberto and Lando Norris are the smooth premium-agency register, named below only to fix the AI-default clichés and never as brutalist evidence.

**FlowFest palette.** The shipped Webflow stylesheet (`https://cdn.prod.website-files.com/682310547ba9eeb97324a89e/css/flowfest-2025.webflow.shared.d5970e214.css`) declares `--color-light: #f3ecd2`, `--color-dark: #121212`, `--color-pink: #f489a3`, `--color-light-plus: #fffefb`, `--color-mango: #f3a20f`, `--color-orange: #f97028`, `--color-yellow: #f0bb0d`. The served HTML's inline SVGs (rainbow arches, illustrations) use `#F3A20F` ×16, `#F97028` ×10, `#F0BB0D` ×10 and `#F489A3` ×6 as strokes and fills, while `#121212` ×226 and `#FFFEFB` ×70 carry ink, borders, and button fills. The Awwwards entry lists the palette as `#F3A20F` / `#F97028`: that pair is the illustration and rainbow palette, and the pink / off-white / off-black trio is the button and ink palette.

**Evidence base.** Live CSS, raw HTML, and shipped JS bundles read via `curl` from each site's own origin and CDN, 9–13 Jul 2026.

### The score reality

The brutalist archetype tops out around **7.5** on Awwwards in the 2023–2026 window. Every truly-brutalist SOTD verified scored **7.34–7.48**, and the single highest-craft brutalist build (Eloy Benoffi) took an Honorable Mention rather than a SOTD. The archetype's rejection of polish caps the jury Design score, so the "top tier" of this line is the 7.3–7.5 band: the ceiling to match, not a bar these sites cleared. Ceiling context: Amaterasu at **7.54** (SOTD 14 Nov 2024) is the nearest higher scorer and is not brutalist.

## Effect palette

### Cross-site headline

The winners share no single hover trick and no single nav treatment. Each element class earns a different response, and the whole system holds one voice. The pale fill-sweep and the filled scrolled-nav-bar that a lazy build ships appear in zero of the sites examined.

### Hover and micro-interactions

**AI-default cliché.** One `:hover` rule reused on every button: a pale wash of the accent (`background: color-mix(accent 12%, white)`) sweeping in over `0.3s ease`, the same treatment copied onto links, cards, and nav. A soft frosted nav bar that fades to a translucent white and grows a 1px border-bottom on scroll.

**What the winners show.** Every element class gets a distinct response, and when a fill happens it is a **full saturated token, never a pale tint**. Across the four sites read live, the nav bar at rest is transparent, borderless, and un-blurred every time.

#### 1a. Button press-down (hard-shadow collapse)

The button sits on a hard offset shadow at rest; on hover it translates *into* the shadow and the shadow flattens to zero. No color change, no fill.

- FlowFest `.btn`: rest `box-shadow: 0 4px 0 rgba(0,0,0,0.15)`; hover `transform: translateY(0.25em); box-shadow: 0 0 0 0 rgba(0,0,0,0.5)`. Transition `0.25s cubic-bezier(0.625, 0.05, 0, 1)`, a custom Osmo expo-out. Button fill stays pink `#F489A3` or off-white `#FFFEFB`; 2px off-black border `#121212`; pill radius 160px.
- **Where it fits.** Warm-illustrated and saturated stacks where the button reads as a physical object. The canonical brutalist button move.
- FlowFest (verified, live CSS). Single-source for the exact mechanic; the offset-shadow-plus-press is archetype-standard.

#### 1b. Full-accent structural fill

A bordered, zero-radius control fills with the **full brand accent** on hover or activation; label color holds. The closest any winner comes to a "fill", and it is saturated, not washed.

- Sui Overflow `.nav-link`: `border: 2px solid #000F1D`, `border-radius: 0`, rest `background: #F7F7F7`; active/current `background: #4DA2FF` (Sui blue). Transition `background-color 0.3s`. Label stays off-black `#000F1D`.
- Token names from the shipped stylesheet: `--color--blue-900: #000f1d` (the 2px border on controls), `--color--blue-700: #4da2ff` (the `.button-icon__wrap` background fill), `--color--light: #f7f7f7`; radius `0` by absence of any radius declaration.
- **Where it fits.** Saturated / industrial-monochrome stacks; nav pills, filter chips, segmented toggles, anything that reads as a switch. The measured fill is the full accent (`#4da2ff`), the border a strong 2px ink (`#000f1d`), the radius `0`.
- Sui Overflow (winner-verified, first-party from the shipped stylesheet). Against 1a, the pair gives the line both a "press" and a "fill" button rather than one default.

#### 1c. Underline draw from the leading edge

A pseudo-element rule, 2px, `currentColor`, scaled from 0 → 1 on the x-axis with `transform-origin: left`. Text color unchanged.

- FlowFest `.underline-link::before { content:""; position:absolute; bottom:0em; left:0; width:100%; height:0.125em; background-color: var(--…) }`: rest `scaleX(0)` with `transform-origin: right`, hover `.underline-link:hover::before { transform-origin: left; transform: scaleX(1) rotate(0.001deg) }`. The `rotate(0.001deg)` forces crisp GPU rasterization. The origin flip between states is the detail a copy misses.
- Sui Overflow `[data-underline]::after { height: 2px; width: 100%; background: currentColor; transform: scale(0,1); transform-origin: left }` → hover `scale(1,1)`, gated behind `@media (hover: hover) and (prefers-reduced-motion: no-preference)`.
- **Where it fits.** Text links and inline nav in every stack. The default link treatment; two independent SOTD sites converge on it.
- FlowFest + Sui Overflow (verified, live CSS). **≥2 sites.**

#### 1d. Link color dim / shift (no underline)

Text link shifts color on hover with a short color-only transition: dim toward gray, or up toward the accent. Restraint over decoration.

- Naked City `.director-link:hover { color: var(--grey-dark) }`, `transition: color 0.35s`; raw un-styled anchors elsewhere sit at the browser default blue `rgb(0,0,238)` on purpose.
- Sui Overflow `.faq-rich a:hover { color: var(--color--gray-700) }`, the same move in the structural stack.
- **Where it fits.** Industrial/editorial stacks with dense text menus (director lists, indexes) where underlines would clutter. Both sites resolve the hover to a muted grey (`--grey-dark`, `--color--gray-700`), never to the accent.
- Naked City + Sui Overflow (verified, live CSS).

#### 1e. Card / sticker rotate-tilt

Cards and pinned "sticker" elements rotate a few degrees on hover, alternating direction by DOM parity so a grid tilts like scattered paper.

- FlowFest `.community-card:hover { transform: rotate(3deg) }`; odd children `rotate(-3deg)`. Expect-cards reveal at `rotate(-5deg) scale(1)` / even `rotate(5deg)`.
- **Where it fits.** Warm-illustrated / zine stacks; image cards, tags, stickers. Amplitude runs 3–5°, with the sign alternating per `nth-child`.
- FlowFest (verified, live CSS). Single-source; signature of the warm-illustrated stack.

#### 1f. Image RGB channel-split / CRT dissolve

Image hover dissolves the still into offset RGB channels via a shader, then a video autoplays underneath once buffered. Brand-tinted, not literal red/green/blue.

- Naked City: a CRT-inspired GLSL shader "dissolves the image into RGB-like channels", the palette shifted from pure R/G/B toward the brand tones; it runs in a Three.js scene inside the site's own Canvas3 Nuxt module, not in CSS. The shader is a reused component across every image reveal. Video-after-shader sequencing is case-study-stated, not read from source.
- **Where it fits.** Industrial/terminal stacks with a WebGL layer already present; hero and portfolio thumbnails. Its CSS-only cousin is a cheap `filter: invert()` (1g), the same intent without the shader budget.
- Naked City (author-stated; implementation is WebGL, not CSS-inspectable). Single-source.

#### 1g. Image invert-on-hover

Hover inverts the image to a hard negative: no transition, or a fast one. The cheap, honest cousin of 1f.

- DesignThinkers 2020: inverted-color hover across the grid (observed, **pre-window**).
- **Where it fits.** Any stack where a WebGL shader is overkill; `filter: invert(100%)`, optionally `grayscale(100%)`. Instant or ≤0.2s is what separates the brutalist read from a smooth one.
- DesignThinkers (single-source).

#### 1h. Nav bar surface — transparent and borderless at rest, on all four

At rest, all four live-read winners run the **same** nav: `position: fixed`, `background: transparent`, `border-bottom: none`, `backdrop-filter: none`, text painted in the page's off-black or off-white token.

- FlowFest `nav`: transparent, color `#121212`, no border.
- eloyb.design `.navbar`: transparent, color `#2B2C27`, no border.
- Naked City `.navigation-bar`: transparent, color `#FFF`, no border.
- Sui Overflow `header`: transparent, color `#000F1D`, no border.

**No winner hangs a different-colored border-bottom under the nav, and none takes a solid surface color at rest.** The type and the fixed corner placement carry it. Scrolled-state surface change was not captured; "gains a bar on scroll" stays unverified, while the rest-state convergence is 4/4.

FlowFest + eloyb + Naked City + Sui Overflow (verified, live CSS). **4 sites.**

### Motion and scroll

**AI-default cliché.** One global `fade-up 0.6s ease-out` on every section via a scroll library's default; a `translateY` parallax on the hero image at `speed=-2`; the same reveal on headings, images, and cards alike.

**What the winners show.** Reveal choreography is *smooth* GSAP (expo, power, bounce eases), varied per content type, while the jarring/step register is reserved for hero text and toggles (§3). Scrub-linked reveals over passive fades.

#### 2a. Staged multi-step scale-in

An element overshoots and settles across chained tweens with tightening durations and rotating eases: mechanical assembly, not a soft fade.

- Treize Grammes work cards: scale `1.75 → 1.5 → 1.25 → 1` across three tweens: `0.25s power3.in` (stagger 0.2) → `0.2s power3.inOut` (0.15) → `0.15s power3.out` (0.1); random `transform-origin` per card.
- Eloy ships the same cascade in source, in `tlWorkCardReveal`; the per-step values from its inline JS are in "## Mid-page aliveness".
- **Where it fits.** Feature/work grids in any stack; the brutalist alternative to a uniform fade-up.
- Treize Grammes (author-stated params). *Single-source*; the Eloy read carries the identical numbers, so the two are one recipe with an unresolved site attribution, not two corroborating sites. The source read is on Eloy.

#### 2b. Scrub-pinned stacked-copy scroll

A masked row holds 3+ stacked copies of a word; scroll drives `yPercent 0 → -300` under `scrub`, so the label ratchets through its duplicates as the section moves.

- Treize "Selected Work" title: `ScrollTrigger { start: 'top bottom', end: 'bottom-=60% top', scrub: 0.6 }`, `yPercent 0 → -300`, eases `power3.in / power2.in / power1.in`, stagger `amount: 2`.
- Eloy `tlWorkScroll`: same device, `scrub: 0.6`, `.work-header … .title-txt` rows `fromTo(yPercent: 0 → -300)`, `ease: "power1.in"`, `stagger: { amount: 2 }`, `duration: 2` (source-verified).
- **Where it fits.** Section headers and dividers; it pairs with marquee bands.
- Treize Grammes (author-stated); the Eloy `tlWorkScroll` values are identical and "Selected Work" is Eloy's `.work-header … .title-txt` (attribution note under 2a).

#### 2c. Scrub-driven scale slider

Scroll position, not time, drives a GSAP timeline scaling the active item up and its neighbors down; ease `none`, because scroll is the clock.

- Joffrey Spitzer vertical slider: `ScrollTrigger`-driven, `force3D: true`, expand `0.8s` / contract `1.5s`, `0.3s` gap, ease `none`.
- **Where it fits.** Editorial work indexes; the brutalist take on a carousel: no auto-advance, scroll is the control.
- Joffrey Spitzer (author-stated, supporting). Single-source.

#### 2d. Scrub dissolve with heavy lag

A hero graphic dissolves as the page scrolls with a high `scrub` value, so the motion trails the scroll for a deliberate, physical drag.

- Treize hero SVG: `ScrollTrigger { scrub: 8 }`, per-path stagger from random positions, `opacity 0`, `2s`, ease `bounce.inOut`.
- Eloy `tlHeroSVG` runs `scrub: 8` on its flower paths with the same `bounce.inOut` fade (source-verified).
- **Where it fits.** Hero exit as the page leaves the fold; the high scrub is the signature; the common range elsewhere is 0.5–1.
- Treize Grammes (author-stated); the Eloy `tlHeroSVG` values are identical and the flower paths are Eloy's (attribution note under 2a).

#### 2e. Marquee band at section breaks

A horizontal text band translates `-100%` on loop between sections, the brutalist section divider.

- FlowFest keyframes: `@keyframes translateX { to { transform: translateX(-100%) } }` plus a `rotateSun` decorative spin (`rotate(9deg)`). The JS marquee runs at `pixelsPerSecond = 75` (`initCSSMarquee`, clones `[data-css-marquee-list]`).
- FlowFest (verified, live CSS keyframes + Slater JS). Pairs with 2b.

**Layer split.** Reveals are smooth and eased (`Expo.easeOut`, `power3`, `bounce.inOut`); the jarring/step register lives in hero text and micro-toggles, not in scroll reveals. The split runs by layer, not as an archetype-wide "never smooth".

### Text effects

**AI-default cliché.** SplitText per-char fade-up on every heading with identical `stagger 0.03, ease power2.out`, the same reveal minimalist, editorial, and brutalist builds all ship.

**What the winners show.** The signature brutalist text move is scramble / glitch / diff, not fade; smooth mask reveals are supporting, reserved for body and secondary titles.

#### 3a. Scramble / character-diff swap (signature)

Text mutates character-by-character between two strings on hover or in place: decode/glitch, not crossfade.

- Eloy Benoffi location tag: hover swaps "Madrid" ↔ "Mar del Plata" via GSAP TextPlugin `type: "diff"`, `0.3s`, `preserveSpaces` / `padSpace: true`; Codrops adds `speed: 1`. `ScrambleTextPlugin.min.js` is loaded on the page; the scramble read is inferred from the loaded plugin, not named by the case study.
- The live scramble mechanic is hand-rolled JS, not the plugin: any `[scrambleText]` element re-randomizes its characters on hover over charset `'*&@#%$-_:/;'`, `setInterval(…, 100)` on `mouseover`, `clearInterval` + `innerText = originalText` on `mouseout`.
- **Where it fits.** Terminal/glitch stacks; location tags, status strings, section labels, hero sub-lines. The brutalist counter to a fade.
- Eloy Benoffi (winner-verified, inline JS + DOM). Single-source, and definitive of the glitch stack.

#### 3b. RGB split / glitch on hero type (signature)

Hero display type splits into offset color channels: the `rgb-split` keyframe, corroborated by the corpus's glitch and CRT work (Eloy's whole system, Naked City's channel dissolve).

- **Where it fits.** The hero headline, one moment per page, held in the hero, never scattered across body copy.
- Eloy Benoffi + Naked City (author-stated). **≥2 sites** carry channel-split as a core device.

#### 3c. Masked per-char / per-line reveal (supporting)

Lines and characters rise out of an `overflow: hidden` mask on scroll: the smooth supporting reveal, not the brutalist signature.

- Joffrey Spitzer: titles `SplitText` chars `yPercent -120, scale 1.2, stagger 0.01, expo.out, 1s`; paragraphs per-line `yPercent 105, stagger 0.04, expo.out, 0.9s`, mask per line. Eloy also loads `SplitText`; on FlowFest it ships in a script tag but is never registered. Treize ships none; its script-tag census (below) carries only ScrollTrigger, three.js r128 and Swiper 11 alongside GSAP.
- **Where it fits.** Body copy and secondary titles anywhere; it runs *under* a scramble/glitch hero, never instead of one.
- Joffrey Spitzer (verified params) + Eloy (SplitText present). **≥2 sites**, shared across archetypes, supporting.

### Cursor and pointer

**AI-default cliché.** A smooth lerped follower-blob (the premium-agency mouse-follower) bolted onto a brutalist skin: a circle trailing the pointer with `mix-blend-mode: difference`. It reads as generic-premium, the opposite of brutalist honesty.

**What the winners show.** Either a hard *swapped* cursor (a bitmap/SVG image replacing the arrow) or the deliberate default.

#### 4a. Swapped bitmap / pixel cursor

The system arrow is replaced by a custom pixel/SVG cursor image with an explicit hotspot: instantaneous, no lerp.

- eloyb.design `body { cursor: url(".../cursor-default_dark.svg") 2 0, auto }`, matched to the Px437 VGA bitmap type.
- **Where it fits.** Terminal/glitch stacks, where the whole page commits to a pixel cursor for a DOS/CRT read. `cursor: url()` carries zero runtime and no lag, unlike a JS follower.
- eloyb.design (verified, live CSS). Single-source.

#### 4b. Deliberate default / raw pointer

The OS cursor stays and unstyled anchors keep the browser default blue. Honesty as a stance.

- Naked City: default-blue router anchors `rgb(0,0,238)` left raw; no custom follower on links.
- **Where it fits.** Industrial-monochrome stacks carrying the "this is a document, not an experience" read.
- Naked City (verified, live CSS). Single-source.

A custom-cursor element was present on Sui Overflow and eloyb (`hasCustomCursor`), but the smooth-follower blob was absent from every brutalist winner; it belongs to the smooth-agency archetype, not this one.

### Loader effects

**AI-default cliché.** A centered percentage counter easing `0 → 100` over a smooth `power2.out`, then a fade-to-content, the same preloader on every site regardless of archetype.

**What the winners show.** Every winner in the line front-loads an intro beat; the brutalist tell is its *character*, not its presence. At effect level the signal is `steps()` easing on the counter: Joffrey Spitzer ratchets `0 → 100` in 14 chunky steps over `3s` against a parallel `clip-path` wipe. The stepped easing is the whole signal; a smooth counter reads generic.

Per-winner loader beats and handoffs are in "## Page recipe" → Loader and intro.

### Composition

Two SOTD sites, both read live end-to-end, each varying interaction by element class while holding one voice. Coherence comes from a *single physical metaphor*, not a single effect.

#### 6a. FlowFest 2025 — voice: "physical objects on a table"

Everything responds the way a printed, tactile object would; the differentiation is by affordance.

- **Button** → presses down into its hard shadow (`translateY(0.25em)`, shadow collapses to 0). *Affordance: a thing you push.*
- **Text link** → underline draws from the left (`::before scaleX 0→1`). *Affordance: a thing you trace.*
- **Card** → tilts `±3°`, alternating by grid parity. *Affordance: paper you nudge.*
- **Sticker / expect-card** → peels in at `±5°` with scale. *Affordance: a decal.*
- **Nav** → transparent, no border, off-black `#121212` text, fixed. *Affordance: none; it stays out of the way.*
- One easing family binds them: `0.25s cubic-bezier(0.625,0.05,0,1)`. Different transforms, one clock, one metaphor: variety that reads as one hand.

#### 6b. Sui Overflow 2025 — voice: "hard-edged controls that snap state"

Everything reads as a switch or toggle; differentiation is by control type, unified by the 2px / 0-radius / off-black system.

- **Nav pill / button** → fills with full accent `#4DA2FF` inside a 2px `#000F1D` border, radius 0 (`background-color 0.3s`). *Control: a segment that activates.*
- **Text link** → 2px `currentColor` underline scales `0→1` from the left. *Control: an inline toggle.*
- **FAQ toggle** → the plus rotates `90°`; on open, the two dots spread `±500%`. *Control: an expander.*
- **Key / chip** → `.key:hover { transform: translate(7%, 18%) }`, a keyboard-key micro-press. *Control: a physical key.*
- **Nav** → transparent, no border, off-black text, fixed. Same restraint as FlowFest.
- Unifiers: every control shares the 2px off-black border, 0 radius, off-black-on-off-white base (`#000F1D` on `#F7F7F7`), and a `0.3s` linear-ish switch timing. Different controls, one build system: coherent variety.

**The transferable rule.** Each site holds one physical metaphor (object / control / terminal / print sheet), gives every element class the interaction its *affordance* implies under that metaphor, and runs all of them on one easing family and one border/shadow/radius system. Variety across classes plus unity of metaphor and values is what these two SOTD winners do that a single repeated hover cannot.

### Anti-signals — absent from every winner examined

- **Pale / washed-out tint fill on button hover.** Zero occurrences. When a fill happens it is the full saturated accent (Sui `#4DA2FF`); otherwise the button presses (FlowFest) or the link shifts color (Naked City). A `color-mix(accent, white)` wash appears nowhere.
- **One hover rule reused across element classes.** Every winner differentiates button vs link vs card vs nav. The universal single-trick is the tell.
- **Scrolled nav that grows a solid surface + a different-colored border-bottom.** All four live-read navs stay transparent, borderless, un-blurred at rest, painting only token-colored text.
- **`backdrop-filter: blur()` frosted nav.** `none` on all four.
- **Smooth lerped follower-blob cursor** with `mix-blend-mode: difference`. Brutalist winners swap the cursor bitmap (eloyb) or keep the default (Naked City).
- **Pure `#000` / `#fff`.** Even Sui Overflow, whose Awwwards swatch reads `#000000 / #ffffff`, ships `#000F1D` on `#F7F7F7` in the actual CSS; the off-black/off-white floor holds in a real SOTD winner.
- **Uniform `fade-up 0.6s` on every section.** Reveals are staged and varied per content type (scale assembly, scrub sliders, stacked-copy ratchets), not one global fade.
- **Rounded, soft-shadow cards.** Radius is 0 in the structural stack (Sui) or a committed pill (FlowFest 160px), never the default 8–12px; shadows are hard offset (`0 4px 0`), never blurred.

## Page recipe

The ordered scroll anatomy, hero skeletons, loader handoffs, route transitions, verbatim copy voice, imagery formula, footer construction, and the replayable spectacle. The element-level grammar those pages carry is "## Effect palette" above.

### Named page shapes

Three page shapes recur. Each is grounded in ≥1 winner; single-source shapes are flagged.

#### Shape A — The Community Scroll

**Fingerprint.** The event / festival / hackathon long-scroll. A warm or playful loader hands off to a type-as-image hero carrying a date/location line and a single ticket/register CTA; then a linear funnel walks the reader from "what is this" → proof (lineup / tracks / prizes) → "what to expect" feature strip → social proof (testimonials, "two years of…") → FAQ accordion → an oversized invitation close that reprises the CTA. Density oscillates hard: tight lineup/FAQ clusters against a vast hero and close. FlowFest's live HTML carries **9 `<section>` elements** (`class="section"` ×0) across roughly 8–14 viewport-heights; the "18–24 sections" figure counts finer scroll beats and is observed, not verified. Climax sits at the lineup/tracks reveal (~40% down); the rest beat is the FAQ before the close. Fits conferences, festivals, hackathons, community events, launch microsites.

**Skeleton.** loader → type-as-image hero + date/location + CTA → "What is X?" understanding block → lineup/tracks proof grid → "what to expect" feature strip (4–6 tiles) → community / social-proof band (testimonials) → FAQ accordion → oversized "see you there" close + CTA reprise + contact.

**Grounding.** FlowFest (funnel order from the rendered heading sequence: What is X? → lineup → what-to-expect → community → FAQ → close); Sui Overflow 7-block scroll (live successor).

#### Shape B — The Studio Index

**Fingerprint.** The portfolio / agency / production-company page where the loader morphs into the navbar, the hero is an identity statement (a location toggle, a manifesto line, a cycling brand promise) rather than a headline, and the body is a single hover-charged work index. The close is the finale, not an epilogue: it carries the loudest interaction and the contact CTA. Few named sections (4–8), ~5–8 viewport-heights. Climax = the work-index hover/scale spectacle; the emotional peak is deliberately near the bottom. Fits creative portfolios, agencies with attitude, production companies, studios.

**Skeleton.** loader-into-navbar → identity hero (tag / manifesto, no CTA in fold) → "who / about" band → hover-charged work index (drag slider or CRT-dissolve grid) → contact/connect close.

**Grounding.** Eloy Benoffi (Who / Work / Labs / Connect, clone-field about-section; live + Codrops); Naked City Films (directors nav + CRT thumbnail grid; Codrops); Treize Grammes (promise hero + service index + "book a partner" footer; live).

#### Shape C — The Stepped Reel

*(single-source)*

**Fingerprint.** The showreel-first minimal-brutalist folio. A mechanical stepped-counter loader with a clip-path curtain hands its first video frame directly into a full-bleed showreel hero via a Flip morph; the body is a brutalist vertical case slider where the active case scales up to take the spotlight; multi-page, with Swup + Flip route transitions that rhyme with the loader. Minimalist surface with a raw, direct edge. 4–6 sections. Fits solo directors, motion designers, reel-first portfolios.

**Skeleton.** stepped-counter loader + clip-path curtain → showreel-video hero (Flip handoff from loader frame) → brutalist vertical case slider → about (Flip link→title morph) → contact.

**Grounding.** Joffrey Spitzer only (Codrops, technique, single-source; "vertical case slider" is Codrops-only).

### Hero architectures

#### Hero 1 — Type-as-image slab

*(FlowFest, live-verified)*

The H1 is not text; it is drawn. FlowFest renders **"Webflow chat, festival vibes, good times."** as inline `<svg><path>` inside `.welcome__h1` (`.welcome__h1 > span > svg > path` in the raw HTML; the phrase, trailing period included, exists only as JS-injected accessible text, absent from the server HTML, which is what proves it SVG-drawn). Above it sits the tagline **"FlowFest is back."**, a chat-cloud mascot centered, a shuffle photo carousel, and the date/location line **"Friday 8th August, Manchester, UK"**. The only CTA in the fold is the "Buy Tickets" pill in the fixed nav; the hero itself carries no button.

Entrance choreography, from `initLoader` post-loader handoff:

| Order | Element | Transform | Duration | Easing |
|---|---|---|---|---|
| 1 | `.welcome-sun__transform` (mascot) | `y` → `0` from centered | (tweened, timeline anchor `"< -1"`) | `cubic-default` |
| 2 | `.nav-bar` | `yPercent -102 → 0` (drops in) | timeline `"<"` | (default) |
| 3 | `.welcome__row-cards` | `y "3em" → 0`, `autoAlpha 0 → 1`, `stagger -0.025` | 1s | `Expo.easeOut` |
| 4 | `.welcome__h1 > span`, `.welcome__h2-box-wrap` | `yPercent 100 → 0`, `autoAlpha 0 → 1`, `stagger -0.025` | 1s | `Expo.easeOut` |
| 5 | `.rainbow-sides__right`, then `__left` (4 arches each) | DrawSVG stroke from the edges | 2s each, delays 0.5s / 1s | `animateRainbow`, stagger 0.075 |

All five rows read from the raw Slater bundle (`https://slater.app/14984/39049.js`). Rows 1–4: `-102`, `Expo.easeOut`, `stagger: -0.025`, `duration: 1`. Row 5: `animateRainbow(selector, mode, count, duration = 4, delay = 0, stagger = 0.075, …)` draws `count` path pairs (`paths[i]` with `paths[i + count]`) with DrawSVGPlugin on `Power2.easeInOut`, and the loader calls it as `animateRainbow('.rainbow-sides__right', 'fromStart', 4, 2, 0.5, 0.075)` then `animateRainbow('.rainbow-sides__left', 'fromEnd', 4, 2, 1, 0.075)`: four arches per side over 2s, delayed 0.5s and 1s, so the side rainbows complete in roughly 2.7–3.2s. The vertical rainbows are a separate scroll-scrubbed draw (Mid-page aliveness below).

#### Hero 2 — Identity-tag terminal hero

*(Eloy, live-verified)*

No headline sells; the fold is an identity terminal. Corner-anchored status tags carry the message: bottom-left **`>>>based in madrid, spain`** / **`[timezone:gmt+2]`** / **`40.416775 // -3.703790`**, which diff-swap to **`>>>born in mar del plata, arg`** on interaction (GSAP TextPlugin `type: "diff", preserveSpaces: true, padSpace: true`, read live; Codrops adds `speed: 1`). A drawn eye-flower SVG plus ASCII decorations sit center. The nav is a forced-open menu (Who / Work / Labs / Connect / `socials ⇢`). No CTA in the fold; the CTA is at the bottom. Entrance: the loader container expands and resolves into the hero, the loading bar becoming the navbar.

#### Hero 3 — Showreel-curtain hero

*(Joffrey, single-source)*

Full-bleed autoplay showreel video, no verbatim H1. The hero is revealed by the loader's clip-path curtain retracting, and the loader's first video frame is Flip-morphed (`Flip.getState` / `Flip.from`, `1s expo.inOut`) into the showreel's final size and position: the loader *is* the hero's entrance.

### Loader and intro

**No brutalist intro read here is an instant paint.** Four roster sites have their intro documented, and each runs a deliberate one: a chat loader (FlowFest), a stepped counter (Joffrey), a loader-to-navbar expansion (Eloy), a scroll-driven welcome transition (Naked City). Sui Overflow is the open case: no intro surfaces in its shipped CSS, raw HTML or script stack, and a secondary source records it as near-instant with no ceremony ([`../surfaces/preloaders.md`](../surfaces/preloaders.md)). The claim below is scoped to the four verified intros.

#### FlowFest — chat-cloud typing loader

*(live-verified, from `initLoader`)*

The loader is an in-character chat conversation, on-brand for "Webflow chat". Beats:

1. `main` set `overflow: clip`, `height: 100svh`; mascot `.welcome-sun__transform` positioned to viewport center; its `.chat-cloud__p` set to `"..."`.
2. `.loading-screen` → `{ autoAlpha: 0, duration: 0.3, ease: "none", delay: 0.1 }`.
3. Chat cloud types (all `ease none`, TextPlugin): `"..."` → **`"Hi Friends!"`** (0.4s, delay 0.2) → `"..."` (0.25s, delay 1) → **`"We are back..."`** (0.5s) → `"..."` (0.25s, delay 1) → back to the hero's resident text `sunTransformText` (0.5s).
4. Handoff (overlapping): mascot slides `y → 0`, nav-bar drops from `yPercent -102`, welcome cards and H1 spans stagger in (Hero 1 table), rainbow arches draw from the sides.
5. `lenis.stop()` during (`tl.call(() => lenis.stop())` in source), then `pageTransitionOut()` + `lenis.start()` + `main` `clearProps: all` at timeline `3`.

Globals read live: `staggerDefault 0.07`, `durationDefault 1.47`, `transitionOffset = 25; /* ms */`, `CustomEase.create("cubic-default", "0.625, 0.05, 0, 1")`.

#### Joffrey — stepped counter + clip-path + Flip

*(technique, exact params)*

- Counter: `gsap.to(progressVal, { duration: 3, ease: 'steps(14)', value: 100 })`: 0→100 in 14 chunky steps; the `steps()` is the brutalist tell.
- Curtain (parallel): `clip-path` `inset(2.5rem 2.5rem 2.5rem 2.5rem)` → `inset(100% 0rem 0rem 0rem)`, **`duration: 1, ease: "expo.inOut"`**.
- Handoff: `Flip.getState()` / `Flip.from()` morphs the preloader's first video frame into the showreel's size and position, **1s `expo.inOut`**.

#### Eloy — loader-into-navbar expansion

*(technique)*

Starts as a stripped-down version of the hero visuals; a loading bar grows while the section scales down; the loader container becomes the navbar. Codrops section title: "Wow at First Sight: The Loading Animation into the Hero Section".

#### Naked City — scroll-driven welcome transition

*(technique)*

No isolated preloader documented; the initial load and a scroll-driven welcome transition are the first two stages of a unified transition system running in "a single `requestAnimationFrame` loop within the Canvas3 module".

**Absence is data, within scope.** Across the four sites whose intros were read, a zero-ceremony instant paint was not observed once; Sui Overflow's entry is unread on this axis. The brutalist tell is the character of the intro (typed chat, `steps()` counter, container expansion), not its presence.

### Route transitions

*(multi-page winners)*

- **Joffrey Spitzer: Swup + GSAP Flip.** A menu link is captured (`Flip.getState(link)`), scaled and repositioned to become the destination page title, matching `fontSize` / `lineHeight` / `letterSpacing`: `Flip.from(state, { duration: 0.9, ease: "expo.inOut" … })`, reversed on exit; the work-list→detail navigation uses the same approach. The transition language **rhymes with the loader**: both are Flip + `expo.inOut` + clip-path (technique, single-source).
- **FlowFest: Barba.js `@barba/core@2.10.3`** (CDN script tag, `data-barba="wrapper"` in the raw HTML). First load runs the full chat loader (`initLoader`); internal Barba navigations run `initLoaderShort` (a `.loading-screen` `autoAlpha` fade plus a rainbow re-init and `pageTransitionOut()`, no chat replay) with `pageTransitionIn/Out` stopping and starting Lenis and a `transitionOffset` of 25ms. The internal transition is a shortened echo of the loader (live-verified).
- **Naked City.** "Navigation feels more like moving between scenes than loading new pages." and "Transitions feel closer to editorial cuts than traditional fades.", two separate case-study sentences. One system covers initial load, welcome transition, directors-nav interactions, and full page transitions (technique).

Pattern: where a route transition exists, it is a **shared-element morph or an editorial cut**, and it deliberately rhymes with the loader, never a generic cross-fade.

### Copy voice

Two dialects share one refusal: no corporate hedging, no marketing gloss.

#### Dialect 1 — Warm-communal *(FlowFest, Sui, Treize-activation)*

First-person-plural, exclamatory, imperative invitations; short lines.

- FlowFest hero H1 (verbatim, live): **"Webflow chat, festival vibes, good times."** · tagline **"FlowFest is back."**
- FlowFest loader chat (verbatim, live JS): **"Hi Friends!"** → **"We are back..."**
- FlowFest sections (verbatim, live DOM): **"What is FlowFest?"**, **"The No.1 Fest for:"** with a boxed **"Web Designers & Devs"** (the colon is present in the body heading; the ampersand ships as `&amp;`), **"An Event Ran by The Community, For The Community"** (span-split), **"Get Your Ticket for the Community-Led Event of the Year"**
- FlowFest close (verbatim, live DOM): H2 **"See you there!"** · **"Reach out to Isabel at isabel@designsie.co.uk if you have any questions."** · CTA **"Buy Tickets"**
- Sui (verbatim, 2026 successor): H1 **"Sui Overflow 2026"** / **"May - August, 2026"**; **"Build alongside high-signal teams from around the world"**; CTAs **"Register"**, **"View Projects"**, **"Become a sponsor"**, **"Follow on X"**. The prize line ships in two variants: the `sr-only` span reads **"$500K+ in total prizes across core and sponsored tracks"**, the on-screen display copy reads **"$500K+ in total prizes and rewards across core and specialized tracks"**.
- Treize (verbatim, live DOM, French): H1 **"Réveillez votre croissance"** (br-split); triad **"Be true"** / **"Be strong"** / **"Be bold"**; H2 **"On transforme les ambitions en marques"** (br-split); footer CTA **"Prenez rendez-vous avec l'un de nos associés"**; the DOM apostrophe is the curly **`’`** in `l’un`. **"Activez votre marque !"** ships as a button, not an H1 alternate; the "cycling H1" framing is observed, not DOM-proven.

#### Dialect 2 — Terminal-ironic *(Eloy, live)*

Lowercase, `>>>` terminal prefixes, self-deprecating identity tags, ALL-CAPS action verbs.

- Location tags (verbatim, live DOM): **`>>>based in madrid, spain`** · **`[timezone:gmt+2]`** · **`40.416775 // -3.703790`** · diff target **`>>>born in mar del plata, arg`** (the DOM encodes `&gt;&gt;&gt;`).
- CTA (verbatim, live DOM): **`CLICK TO CONNECT`** · **`##########COPY EMAIL##`**, ASCII-framed **`COPY EMAIL`**.
- Nav (verbatim, live DOM): **Who** · **Work** · **Labs** · **Connect** · **`socials ⇢`**, the arrow inside `fmenu-socials`.

**Voice formula.** Person: 1st-plural (communal) or 2nd-person imperative; Eloy drops to lowercase-first-person-ironic. Sentence length: short, often fragment. Verb temperature: hot imperatives ("Register", "Réveillez", "CLICK TO CONNECT", "Build"). Punctuation signature: exclamation plus trailing dots ("Hi Friends!", "We are back...") in the warm dialect; `>>>`, `//`, `[...]`, `#` fences in the terminal dialect. **What the voice refuses:** third-person corporate distance, feature-benefit hedging, "solutions" / "empower" / "seamless" vocabulary, and quiet neutral CTAs; the button is always a verb.

### Imagery art direction

Imagery register is a stack choice, with one through-line: **assets are drawn/typographic primitives or degraded media, never stock gloss.**

- **FlowFest (warm illustrated).** Candid event photography (a 5-image shuffle carousel) subordinate to the SVG headline; decorative marks are drawn SVG (rainbow arches, a sun/chat mascot), never emoji glyphs.
- **Eloy (terminal).** No photography. ASCII art plus a hand-drawn eye-flower SVG carry the surface; `mix-blend-mode: difference` on overlapping clones, declared twice in the shipped stylesheet and applied to runtime-injected clones.
- **Naked City (industrial/cinematic).** Film stills and video graded toward the brand register: a CRT-inspired GLSL shader dissolves each thumbnail into RGB-like channels adapted from pure R/G/B into the brand's electric-blue tones; video autoplays under the dissolve on hover. Awwwards palette widget, "palette of 2 colors": electric blue **`#0004EB`** on gray **`#979797`**.
- **Treize (industrial monochrome).** Brand-case imagery in a Swiper carousel plus Lottie popups over a near-black / off-white base. Computed hex counts across the page: **`#E0E055`** ×63 (most frequent, so the dominant chartreuse accent), **`#EEEEEE`** ×40, **`#131313`** ×16.

**Formula.** One treatment holds page-wide: illustrated-drawn (FlowFest), ASCII/vector-only (Eloy), or degraded-media-shader (Naked City). The crop is full-bleed or hard-framed to the grid; the grade is either flat-saturated (warm stacks) or high-contrast-limited-palette (industrial stacks).

### Footer

The brutalist close is a **designed finale, never functional chrome.** Three recipes:

- **Oversized invitation close** *(FlowFest, live DOM).* `.footer__h2` **"See you there!"** at display scale + `.footer__p` contact line + a newsletter form + a reprised **"Buy Tickets"** CTA + two oversized flanking illustrations. Two-column structure (title/contact | form), illustrations bleeding the edges.
- **Contact-first activation close** *(Treize, live DOM).* Animated close carrying the partner-booking CTA **"Prenez rendez-vous avec l'un de nos associés"** in `cta-prefooter__wrapper`, contact as the terminal action.
- **ASCII contact block** *(Eloy, live DOM).* `##########COPY EMAIL##` + `CLICK TO CONNECT`. The page's loudest interaction, the clone field, sits one section earlier on `.about-section` (Spectacle menu below); the emotional peak is near the bottom, not literally in the footer.

CSS-level: the close reprises the primary CTA or the contact action, sets the wordmark or headline at the page's largest type, and hosts at least one motion or interaction moment. No winner ships a link-list-columns chrome footer.

### Spectacle menu

The one passage a judge replays, per winner:

- **Eloy: the clone field** *(the strongest replay).* Trigger: mouse movement over `.about-section`, under the inline comment `/*CONNECT POPUPS*/`. Mechanics read from source: `const TRIGGER_DISTANCE = 200; const COPIES_PER_TRIGGER = 2;`: a `mousemove` handler calls `createCopies(2)` each time cumulative pointer travel reaches 200px, with **no maximum-copy cap**; each copy carries `mix-blend-mode: difference`; on the section's `mouseleave` the `.generated-copy` clones exit via `gsap.to(generatedCopies, { opacity: 0, scale: 0.6, duration: 0.2, ease: "back.in(1.7)" })`. Codrops files it under the heading "Ending with a Critical Error". Payoff: a chaotic difference-blend interference field of overlapping "CLICK TO CONNECT" ghosts. Replayable because it is pointer-driven and unbounded; every mouse path draws a different mess.
- **FlowFest: the chat-cloud reveal.** Trigger: page load. Beats: the mascot types "…" → "Hi Friends!" → "We are back..." then slides to rest as the nav drops, cards stagger, and the rainbow arches draw from the edges. Payoff: a conversation that becomes the hero. Replayable as a reload; the typing carries personality no static hero could.
- **Joffrey: counter into showreel.** Trigger: load. Beats: a `steps(14)` counter ratchets 0→100 over 3s while a clip-path curtain retracts (`inset(2.5rem…)` → `inset(100% 0 0 0)`, 1s `expo.inOut`), then the loader's first frame Flip-morphs into the full showreel. Payoff: the mechanical count resolves into cinematic motion.
- **Naked City: CRT thumbnail dissolve.** Trigger: hover a film thumbnail. Beats: a GLSL CRT shader dissolves the still into brand-tinted RGB channels while the underlying video buffers, then autoplays. Payoff: an editorial cut from stillness to motion, in-shader.
- **Sui (2025): full-accent structural fill.** A bordered zero-radius control takes the full saturated accent on activation (§1b).

### Page-level anti-signals

- **No winner opens on a card/bento grid.** The fold is a type-as-image slab (FlowFest), an identity terminal (Eloy), a promise line (Treize), or a showreel curtain (Joffrey), never a grid of tiles.
- **No winner leads attention with a product-shot carousel.** FlowFest's carousel is candid community photography, secondary to the drawn SVG headline; it is never the primary attention device.
- **No winner ships a functional link-list footer.** The close is an oversized invitation, a contact-first activation, or an ASCII contact block, always a designed finale.
- **No winner whose intro was read ships true instant paint.** FlowFest, Joffrey, Eloy and Naked City each front-load a loader or a welcome transition; Sui Overflow was not read on this axis and a secondary source calls it near-instant ([`../surfaces/preloaders.md`](../surfaces/preloaders.md)).
- **No winner's route transition is a generic cross-fade.** Where a transition exists it is a shared-element Flip morph (Joffrey) or an editorial cut (Naked City), rhyming with the loader.

The element-level absences (uniform `fade-up`, solid or blurred nav at rest, pale tint fills, one reused hover rule) are in "## Effect palette" → Anti-signals.

## Mid-page aliveness

What the line's highest scorers ship to keep the prose/content zone between hero and footer alive, the exact zone where the merely-good 7.2–7.4 build reads dead.

### Library and asset census

| Site | Smooth scroll | GSAP | Plugins / extras | Read from |
|---|---|---|---|---|
| FlowFest | `lenis@1.3.1` | `gsap@3.13.0` | ScrollTrigger, CustomEase, DrawSVGPlugin, TextPlugin, Draggable registered in the Slater bundle (`slater.app/14984/39049.js`); SplitText + InertiaPlugin loaded but never registered. `@barba/core@2.10.3`, Slater bundle | `<script src>` + `slater.app/14984/39049.js` |
| Eloy | `lenis@1.3.3` | `gsap@3.15.0` | ScrollTrigger, SplitText, Draggable, InertiaPlugin, Observer, ScrambleTextPlugin, TextPlugin, EasePack, ScrollToPlugin — all 9 present | `<script src>` + inline JS |
| Sui Overflow | `lenis@1.1.14` (11 references) | `gsap@3.12.7` | ScrollTrigger, SplitText, `lottie-web@5.12.2` + named JSON decor | `<script src>` |
| Treize | `lenis@1.1.13` | `gsap@3.12.5` | ScrollTrigger, `three.min.js` r128, `swiper-bundle.min.js` @11 | CDN `<script>` tags + `main.js` / `loader.js` |
| Naked City | custom Canvas3 module | GSAP inside Canvas3 | Three.js + smooth scroll + scroll-speed directives fused in one rAF loop | Codrops (technique) |

### The mid-page inventory

**FlowFest 2025** (7.36), the warm-loud register. Between hero and footer the life is:

- **Prose-tile rotation welded to scroll.** The "What is FlowFest?" `.about__tile` runs a `.rotate-circle__list` from `rotate: +15` to `rotate: -15` (`rotateMin = -15`, `rtatePlus = 15` in source), `scrub: 0`, `start: "0% 100%"`, `end: "100% 0%"`. The circular image element rotates continuously as the prose block passes.
- **Rainbow arches drawn on scroll.** `rainbowsScrolltrigger()` re-runs `animateRainbow` under `scrub: 0`: `('.rainbow-vertical__1', 'fromStart', 9, 0.5, 0, 0.0375, null, { trigger: '.welcome', endTrigger: '.about__tile', … })`, `('.rainbow-vertical__3', 'fromStart', 9, 0.5, 0, 0.075, null, { trigger: '.about__bottom', start: 'top 100%', end: 'bottom 50%', … })`, and the side rainbows at count 4 / duration 0.75 against `.stacked-cards__collection`. Each vertical rainbow SVG carries 9 `stroke="black"` and 9 colored paths, so DrawSVG strokes 9 path pairs in on `Power1.easeOut` as the mid-page prose scrolls under them.
- **Idle mascot follows the cursor.** `initSunnyFollowMouse`: every `[data-sunny-face]` tracks the pointer via `gsap.quickTo(this, 'xPercent', { duration: 0.4, ease: 'power3' })` (and `yPercent`) on a `window` `mousemove` listener. Runs the whole page, mid-sections included.
- **Mascot speaks on hover.** `.sun-chat-combo` `mouseenter` → `showText`: chat cloud `autoAlpha 1` over 0.2s, then `text: sunTransformText` via TextPlugin, `duration: 0.5, ease: "none", delay: 0.3`; `mouseleave` → `hideText` types back to `"..."`. A per-section in-character hover payload.
- **CSS marquee band.** `initCSSMarquee` clones `[data-css-marquee-list]` and runs at `pixelsPerSecond = 75`, an infinite loop at section breaks.
- **Draggable photo deck.** `.stacked-cards__collection`: `flick(dir, skipHome, releaseX)` + `restack()` (rewrites z-index and transform) + `resetCycle()`, a throwable card carousel the reader deals through mid-page. The engine is `Draggable.create(firstEl, { type: 'x', … })` with a hand-rolled `onDragEnd` handing off between two cards; the release throw is `gsap.to(el, { x, rotation: 0, duration: 1, ease: 'elastic.out(1,0.75)' })` inside `flick()`.

**Eloy Benoffi** (HM), the glitch-loud register, the densest mid-page in the corpus. Its inline GSAP holds named timelines, one per content zone:

- **Prose assembles from a hash field.** `tlAboutReveal` on `.about-section [type-txt] .char`, `scrub: false`: `.from(…, { stagger: { each: 0.05, from: "random", ease: "none", grid: "auto" }, text: { value: "#", speed: 1 }, duration: 0.05, ease: "power4.out" })`. Every character starts as `#` and resolves to its real glyph in random order; the mid-page paragraph types itself out of noise.
- **Section title ratchets on scroll.** `tlWorkScroll` (`scrub: 0.6`): `.work-header … .title-txt` rows `fromTo(yPercent: 0 → -300, ease: "power1.in", stagger: { amount: 2 }, duration: 2)`: stacked copies of "Selected Work" climb through an `overflow: hidden` window as the page scrolls.
- **Work cards scale-cascade in.** `tlWorkCardReveal` (`scrub: false`, `from: "random"`) fires once per card as three chained `fromTo` calls, all source-verified: `scale 1.75 → 1.5` (`duration 0.25`, ease `power3.in`, `stagger { amount: 0.2, from: "random", ease: "power1.out" }`) → `1.5 → 1.25` (`0.2`, `power3.inOut`, `stagger { amount: 0.15, …, power1.inOut }`) → `1.25 → 1` (`0.15`, `power3.out`, `stagger { amount: 0.1, … }`).
- **Decor pixel-fields scrubbed under the content.** `tlHeroSVG` (`scrub: 8`, flower paths fade on `bounce.inOut`), `tlAboutZoom` (`scrub: 6`, `.about-bg_pixels`), `tlFullScroll` (`scrub: 0.5`, `.nav-deco_reel` across the whole page), `tlWorkReveal` (`scrub: 1`, `.pixel-on [pixel-bg]`), plus `tlHeroScroll` (`scrub: 1.8`) and `tlAbouScrollUI` (`scrub: 1`) on the UI layer. A continuous scroll-linked texture behind the prose.
- **Clone field on the about/connect section.** The pointer-travel clone spawner; constants and exit tween under Spectacle menu.

**Sui Overflow** (7.48), the quiet/industrial register. **Lottie JSON** decor placed mid-page, three assets resolved on the CDN and named exactly: `Header - Pointer - V03`, `Header - Code and Mail - V05`, `Awards - University - V01`. Structural fill on controls: `2px solid #000F1D`, radius 0, full-accent `background: #4DA2FF` over `background-color 0.3s`. The mid-page life is Lottie loops plus scroll-triggered SplitText, not glitch.

**Treize Grammes** (HM), warm-minimal brutalist. Mid-page carries a Three.js "Be true / Be strong / Be bold" video triptych and a Swiper carousel. Even the quiet agency register ships a WebGL layer and an inertial carousel between hero and footer.

**Naked City Films** (7.34), degraded-media register. The custom Canvas3 Nuxt module fuses smooth scroll, Three.js, scroll-speed directives, and GSAP in one `requestAnimationFrame` loop. Image hover runs the GLSL CRT shader (RGB-channel dissolve) reused across every image reveal; the buffered video autoplays after the shader transition. Hover states are hand-built reusable components, "fast, purposeful, restrained."

**Synthesis.** Mid-page life at this tier is layered, not single-channel: a scrubbed decor texture (rainbows / pixel-fields / Lottie) running behind the prose, a content reveal that fires once as each block enters, one idle loop in character (mascot-follow, marquee, clone field), and one draggable or WebGL spectacle the reader operates. The dead 7.2–7.4 build ships the hero reveal and the image reveal, then leaves the prose with no scrubbed layer, no idle loop, and no per-block entrance.

### Hover on text

The tier ships almost **no CSS hover response on non-link text**: headings, prose, list rows, numbers. This holds across all four live-read sites.

- **FlowFest.** No prose or heading hover. Links only (§1c); `.btn:hover { text-decoration: none }` strips decoration and nothing else. `ff_wf.css` carries zero heading/prose hovers.
- **Eloy.** Exactly one CSS text-hover in the whole 58KB bundle: `.floating-foot_copy:hover { color: var(--color--secondary) }`. The one genuine non-link text-hover is JS: `[scrambleText]` re-randomizes characters on `mouseover` (§3a). That scramble is the register's text-hover signature, applied to labeled elements only, never blanket.
- **Sui.** Two text-hovers in 108KB: `.faq-rich a:hover { color: var(--color--gray-700) }` (link color-dim) and `.key:hover { transform: translate(7%, 18%) }` (a keyboard-key press micro-toggle, not prose). No heading or body hover.
- **Treize.** Three hover rules in the entire stylesheet: `a:hover { outline: 0 }` and two lightbox `opacity` toggles. None touches text, color, or border; its hover life is GSAP / magnetic-button driven.

Forms observed, ranked by frequency: link underline-draw from the leading edge (`scaleX`, origin left) → link color-dim → JS character-scramble on labeled non-link text (glitch register only) → key/chip micro-press. Absent everywhere: per-char rise on prose hover, weight or optical-size shift on headings, background-highlight sweep, color sweep along heading text. A build that adds heading or prose hover is inventing above the tier; the tier puts that budget into scroll-linked reveals and idle loops instead.

### Re-fire behavior

The line splits the same way every time, and the mechanism is legible in source.

- **FlowFest.** Scrub census across the Slater bundle: `scrub: 0` ×13, `scrub: true` ×1; the only `toggleActions` value anywhere is `'play none none reverse'`, appearing ×8. Content entrances ride the **loader timeline**: `tl.from('.welcome__row-cards', { y: '3em', autoAlpha: 0, ease: 'Expo.easeOut' })` and `tl.from('.welcome__h1 > span, .welcome__h2-box-wrap', { yPercent: 100, autoAlpha: 0, ease: 'Expo.easeOut' })`, with no ScrollTrigger attached, so they persist. Decor (the rainbow arches, the `.rotate-circle` in the about tile) is welded to scroll via `scrub: 0` or reverses via `play none none reverse`, replaying forward on scroll-down and rewinding on scroll-up.
- **Eloy.** The split is explicit in the timeline flags. Content reveals carry `scrub: false` and fire once: `tlAboutReveal` (the prose hash-resolve), `tlWorkCardReveal` (the card scale-cascade). Decor carries a scrub number and re-fires every pass: `tlHeroSVG` 8, `tlAboutZoom` 6, `tlFullScroll` 0.5, `tlWorkReveal` 1, `tlWorkScroll` 0.6, `tlHeroScroll` 1.8, `tlAbouScrollUI` 1. The directional callbacks run only on decor and UI timelines (`onEnterBack: playCloseAnimation` on `tlHeroScroll`; `onEnter` / `onLeaveBack: toggleMenu` on `tlAbouScrollUI`; `tlPageLoad` `onStart`) and never touch `tlAboutReveal` or `tlWorkCardReveal`.

**The shape of the split.** A content reveal is a fire-once `.from()` with no `scrub`, or a loader-timeline entrance; a decor channel is a `scrub`-numbered ScrollTrigger or a `toggleActions: play none none reverse`. Driving the page up and down, the prose stays assembled while the texture layer breathes with the scrollbar. A 7.2–7.4 build reads dead when it has neither: the prose fades up once with nothing scrubbed behind it, so a second pass is inert.

### Smooth scroll

Near-universal at this tier, loud and quiet registers alike: all four live-read sites load Lenis (versions in the census table), and Naked City replaces it with the custom Canvas3 module providing equivalent inertial smoothing in the same rAF loop as its WebGL.

The scrubbed decor depends on this. Lenis maps wheel delta to an eased scroll position, and the `scrub`-numbered timelines lerp against that eased value, which is what makes the mid-page texture feel driven rather than stepped. Smoothing is not a register choice at this tier; it is the substrate the aliveness rides on.

### Mid-page anti-signals

Beyond the element-level absences already listed, three are specific to the mid-page zone:

- **No hover response on prose or headings.** Heading and body text is inert to the pointer; the budget goes to scroll-linked reveals and idle loops. A per-char rise or a color sweep on a paragraph is above-tier invention.
- **No fire-once-only mid-page.** The tier never leaves the prose zone with only entrance reveals and nothing scrubbed; there is always a texture layer welded to scroll and one idle loop. This is the exact gap in the dead 7.2–7.4 build.
- **No drifting parallax.** The scroll layer is a mechanism the scrollbar drives (rotate, ratchet, pixel-zoom, shader-scrub), not a background floating at a fraction of scroll speed. Where reveals are typed to content (hash-resolve on prose, scale-cascade on cards, `yPercent` ratchet on titles), no blanket transform is left to carry a section.

## Refuted

- **FlowFest "24-section scroll (live-verified)"** is false: the live HTML carries **9 `<section>` elements** and `class="section"` ×0. The 18–24 figure counts finer scroll beats, not sections; the funnel order survives, the count is observed.
- **FlowFest "near-instant first paint / no preloader ceremony"** is false, per its own `initLoader`: a full chat-cloud typing loader runs on first load, and no zero-intro winner exists in the line.
- **FlowFest stacked-card deck runs on InertiaPlugin** is false: the deck runs `Draggable.create(firstEl, { type: 'x', … })` with a hand-rolled `onDragEnd`, and the release throw is `gsap.to(…, { ease: 'elastic.out(1,0.75)' })`. InertiaPlugin ships in a script tag but is never registered; the Slater bundle registers ScrollTrigger, CustomEase, DrawSVGPlugin, TextPlugin, Draggable only.
- **Eloy `tlWorkCardReveal` stagger `{ each: 0.15, from: "random", ease: "power2.in" }`** is false: no such stagger exists in the card reveal. The three chained `fromTo` calls use `stagger amount 0.2 / 0.15 / 0.1` with stagger eases `power1.out` / `power1.inOut`, under main eases `power3.in` / `power3.inOut` / `power3.out`.
- **Eloy's clone-storm lives in the footer** is false: it is bound to `.about-section` under the inline comment `/*CONNECT POPUPS*/`, and the copies exit on that section's `mouseleave`. The word "footer" appears once in the entire HTML, unrelated to the clones.
- **Eloy's clone-storm duplicates one CTA up to a maximum of 200 copies** is false: the shipped constants (Spectacle menu) spawn two copies per 200px of pointer travel with no cap; the 200 is a pixel step on `mousemove`, not a copy limit.
- **Treize Grammes jury score 8.69** is false: an Awwwards Honorable Mention page carries only community votes ("Votes 15/27"), no aggregate, no `aggregateRating` / `ratingValue`; every "8.69" in the HTML is a CSS `clamp()` or an SVG path coordinate. The 15 visible votes averaged ~8.77 on 9–13 Jul 2026, and "jury" mislabels an HM.
- **Sui Overflow ships `lenis@1.1.13`** is false: the script tag reads `lenis@1.1.14`, with 11 references in the bundle.
- **Treize loads Barba** is false: no script tag, and Barba is absent from both production bundles (`main.js` 10.7KB imports only `loader.js`; `loader.js` 1.7KB references only gsap, so neither can contain Barba core). Only vestigial `data-barba="wrapper|container|link"` and `data-barba-namespace="home"` attributes remain, alongside stale `localhost:3000` dev module tags.
- **Sui's "$500K+ in total prizes across core and sponsored tracks" is the on-screen copy** is false: that string is the `sr-only` span. The visible display copy reads "$500K+ in total prizes **and rewards** across core and **specialized** tracks"; the quoted string is the accessibility variant.
- **FlowFest 2025's live CSS carries neither `#F3A20F` nor `#F97028`** is false: both are `:root` tokens in the shipped Webflow stylesheet (Corpus, FlowFest palette). The parent article's "flat `#F3A20F` / `#F97028` palette" ([`../award-winning-websites-2025-2030.md`](../award-winning-websites-2025-2030.md)) is incomplete rather than wrong.

## Could not verify

- Treize Grammes's rainbow-arch parameters are author-stated and identical to the Eloy Benoffi read; which site the recipe originates from is unresolved.
- Sui Overflow's intro was not read; the instant-paint negative covers the four sites whose intros were read.
