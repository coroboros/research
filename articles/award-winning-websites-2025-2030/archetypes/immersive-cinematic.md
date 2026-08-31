---
title: "Immersive Cinematic — Effect Palette, Page Recipe, Mid-Page Aliveness"
date: "2026-07-30"
author: "Coroboros"
tags: ["web-design", "awwwards", "immersive-cinematic", "webgl", "gsap", "scroll-driven-animation", "rive", "effect-palette", "page-recipe"]
sources:
  - "https://www.awwwards.com/sites/lando-norris"
  - "https://www.awwwards.com/sites/siena-film-foundation"
  - "https://www.awwwards.com/sites/lusion-v3"
  - "https://www.awwwards.com/sites/messenger"
  - "https://www.awwwards.com/sites/into-the-storm"
  - "https://www.awwwards.com/sites/typography-principles"
  - "https://www.awwwards.com/sites/shopify-editions-summer-24"
  - "https://www.awwwards.com/sites/obys-2"
  - "https://www.awwwards.com/sites/terminal-industries"
  - "https://www.awwwards.com/sites/cartier-watches-wonders-2025"
  - "https://www.awwwards.com/annual-awards/winners"
  - "https://web.archive.org/web/20240307133625id_/https://www.awwwards.com/annual-awards-2023/"
  - "https://www.awwwards.com/websites/sites_of_the_year/"
  - "https://www.awwwards.com/websites/sites_of_the_month/"
  - "https://www.awwwards.com/awwwards/collections/loading-page/"
  - "https://www.awwwards.com/siena-film-foundation-case-study.html"
  - "https://www.cssdesignawards.com/woty-award-winners"
  - "https://www.cssdesignawards.com/wotm/lusion-v3/44311/"
  - "https://www.cssdesignawards.com/sites/cartier-watches-and-wonders-2025/47763"
  - "https://www.cssdesignawards.com/sites/terminal-industries/47847/"
  - "https://thefwa.com/cases/lusion-v3"
  - "https://landonorris.com/"
  - "https://www.siena.film/"
  - "https://lusion.co/"
  - "https://messenger.abeto.co/"
  - "https://activetheory.net/"
  - "https://www.itsoffbrand.com/our-work/lando-norris"
  - "https://www.webgpu.com/showcase/mclaren-f1-driver-lando-norris-official-website/"
  - "https://www.webgpu.com/showcase/cartier-watches-and-wonders-immersive-garden/"
  - "https://www.nocodesupply.co/item/lando-norris"
  - "https://tympanus.net/codrops/2025/11/19/how-to-build-cinematic-3d-scroll-experiences-with-gsap/"
  - "https://tympanus.net/codrops/2026/04/13/lusion-where-digital-craft-meets-ambitious-experimentation/"
  - "https://tympanus.net/codrops/2026/05/27/whooshes-snaps-and-shaders-adrien-vanderpotte-and-the-feeling-of-the-interface/"
  - "https://tympanus.net/codrops/2020/08/05/magnetic-buttons/"
  - "https://github.com/Cuberto/mouse-follower"
  - "https://cuberto.com/tutorials/27/"
  - "https://metabole.studio/en/blog/immersive-website-examples"
  - "https://www.utsubo.com/blog/best-threejs-websites-2026"
---

# Immersive Cinematic — Effect Palette, Page Recipe, Mid-Page Aliveness

Overall jury scores on the immersive/cinematic line run 7.9–8.25, capped by a standing Usability tax on heavy WebGL, and the winners barely ship prose mid-page: the zone between hero and footer is interactive indexes, scrubbed media, and never-idle canvas. The line's per-element effect repertoire read off live winner stylesheets, the page shapes and hero architectures read off live DOM, and the mid-page channels that keep that zone from going dead. Every value here is committable by name. Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

## Corpus

Evidence tags: `(winner-verified)` = read from the awarded site's live CSS, JS, or DOM; `(shipped)` = observed live or in award-page media, implementation not read; `(technique)` = a documented method, typically Codrops; `(design-canonical)` = a documented design system with no verified award; `(single-source)` = one site only; `[CSS]` / `[JS]` = quoted from shipped code; **verified** / **stated** / **observed** = measured in source / claimed by the builder / seen but not read; `(stated, unconfirmed)` = a builder claim the source read could not confirm; `(inferred)` = derived from indirect evidence.

Each site with its award, its jury numbers where Awwwards publishes them, and how deep the evidence goes.

| Site | URL | Award + date | Overall (Design / Usability / Creativity / Content) | Evidence depth | Stack |
|---|---|---|---|---|---|
| **Lando Norris** | `landonorris.com` | Awwwards Site of the Day (SOTD) 17 Nov 2025 (8.18) + Site of the Year (SOTY) 2025 and Site of the Year Users' Choice 2025 (Annual Awards winners page) + Developer Award 7.58 (Animations/Transitions 8.60); OFF+BRAND | **8.18** (8.12 / 7.9 / 8.71 / 8.18) | CSS + JS bundle + rendered DOM + screenshots | Webflow + GSAP + Lenis + Rive |
| **Siena Film Foundation** | `siena.film` | Awwwards SOTD 18 Mar 2025 + **Site of the Month (SOTM) Mar 2025** + Developer Award 7.51 (Animations/Transitions 8.60); Niccolò Miranda (design and technical direction) with G-NS Studio (production) and Federico Valla (development), per the award page's credit block | **7.9** (7.99 / 7.61 / 8.13 / 8.00) | CSS + JS bundle + rendered DOM + screenshots | Webflow shell + Vercel/Next overlay, Lenis, GSAP SplitText |
| **Lusion v3** | `lusion.co` | Awwwards SOTD 2 Oct 2023 + Developer Award **8.41** (Animations/Transitions **10.0**) + Site of the Year 2023 + Developer Site of the Year 2023 (archived Annual Awards 2023 page); CSSDA Website of the Year 2023 (9.27, winner listing) + Website of the Month Oct 2023; FWA of the Year 2023 + FWA of the Month Sep 2023 + FWA of the Day 21 Sep 2023 | **8.25** (8.26 / 7.95 / 8.65 / 8.26) | CSS + JS bundle + rendered DOM | Astro + WebGL (OGL inferred) + custom lerp |
| **Messenger** | `messenger.abeto.co` | Awwwards SOTD 10 Nov 2025 + Developer Award **8.21** + Developer Site of the Year 2025 (Annual Awards winners page); abeto | **7.92** (8.04 / 7.46 / 8.23 / 8.15) | award page, media-only | Three.js / WebGL / WebSockets |
| **Active Theory** | `activetheory.net` | V6 SOTD; Google I/O Adventure SOTD; current-iteration award unverified | — | rendered DOM (display copy is canvas-rendered) | proprietary Hydra/Aura WebGL |
| _Into the Storm_ | `airforce.com/intothestorm` | Awwwards SOTD 23 Mar 2021, out of window | **8.15** (8.24 / 7.73 / **8.5** / 8.35) | score only | — |

Behavioral and named-case evidence, no live CSS read: **Oryzo** (Lusion), Awwwards SOTM Apr 2026 + Developer Award, camera-through-Z-depth scroll. **Bruno Simon portfolio**, Awwwards SOTM Jan 2026, drivable 3D world (Three.js + Cannon.js). **Cartier Watches & Wonders 2025** (Immersive Garden), Awwwards SOTD 18 Aug 2025 (7.64) + SOTM Aug 2025 (listing, [`corporate-luxury.md`](./corporate-luxury.md#corpus)) and CSSDA Website of the Day 16 Jul 2025 (8.39): six 3D rooms `(stated, webgpu.com)`, Web Audio score, GSAP + Lenis. **Hubtown** (Unseen Studio), Awwwards SOTD Jun 2026, cursor-reveal of geometry and lighting. **Telescope / Silent House / Sandy Shore** (Adrien Vanderpotte), Awwwards SOTD, focal-zoom scroll and continuous scene transitions. **Obys Agency** (`obys.agency`: Awwwards SOTD 4 May 2026, 7.46, + Developer Award 7.98; the studio is Awwwards Studio of the Year 2023) and its **Typography Principles** (Awwwards SOTD), kinetic type. **Shopify Editions**, Awwwards SOTD, scroll-staged particle-dispersing type. **Explore Primland**, scroll-driven terrain flythrough. **Terminal Industries** (Awwwards SOTD 3 Sep 2025, 7.68, + SOTM Sep 2025; CSSDA Website of the Day 4 Aug 2025, 8.42), scroll shifts 3D visuals into wireframe.

Parameter references (technique, not a site): Codrops "Cinematic 3D Scroll with GSAP" (Nov 2025); Cuberto `mouse-follower`; Codrops "Magnetic Buttons".

Live asset paths read: Lando CSS `cdn.prod.website-files.com/67b5a02dc5d338960b17a7e9/css/lando-offbrand.shared.{043b62fef,4f53262f0}.css` (two near-duplicate variants, ~366KB combined) and JS `lando.itsoffbrand.io/dev-js/lando.OFF+BRAND.js` + `assets.itsoffbrand.io/lando/dev-js/lando-by-OFF+BRAND.js`; the JS hosts require a `landonorris.com` referer, and a bare fetch returns 403. Siena CSS `siena-film-foundation.vercel.app/styles/main.css`, JS `siena-film-foundation.vercel.app/app.js`. Lusion CSS `lusion.co/_astro/about.CNa9RfUh.css`, JS `lusion.co/_astro/hoisted.CJiXW_YI.js`.

**Evidence base.** Awwwards jury pages read directly, CSS and JS bundles downloaded and grepped verbatim, DOM read behind a `location.hostname` guard, 9–13 Jul 2026; award titles read on the Awwwards Annual Awards winners page and the sites-of-the-month listing on 29 Aug 2026.

### The score reality

**Overall jury scores on this line run 7.9–8.25.** Jury averaging compresses the overall, and the archetype pays a standing Usability tax: heavy WebGL and scroll-hijack cost the Usability sub-score, which caps the overall in the low 8s. The Usability column across the five scored rows reads 7.95 / 7.9 / 7.46 / 7.61 / 7.73, a range of **7.46–7.95**, and nobody in the line buys the WebGL cost back. The 8.5+ numbers that exist are Creativity sub-scores: _Into the Storm_ carries Creativity **8.5** against an overall of 8.15, and Lando carries Creativity **8.71** against 8.18. The real ceiling to build against is **≈8.25 overall / ≈8.7 creativity**, not an 8.5 overall band the jury does not award here.

Design-token evidence read from the two deepest sites. Lando: lime `#D2FF00`, lime-off `#B2C73A`, lime-zero `#D2FF0000`, dark-green `#282C20`, black `#111112`, cream `#F4F4ED`; 176 elements on the page use the lime. Siena easing tokens: `--easeOutQuint: cubic-bezier(.23,1,.32,1)` (the workhorse), `--customEase: cubic-bezier(.19,1,.22,1)`, `--easeOut: cubic-bezier(.77,0,.175,1)`, `--panels-duration: .9s`, `--slider-dur: .8s`. Lando's own default easing is not in the external bundle at all; it sits in the inline HTML `<style>`: `:root{--cubic-default:cubic-bezier(0.65, 0.05, 0, 1);--duration-default:0.75s}`. A "verbatim" easing sourced from external CSS alone will miss the site default.

## Effect palette

Two findings overturn the common defaults up front, and the sections below carry their evidence: **winners do not wash buttons with a pale tint**, and **the nav bar stays transparent**.

### Hover and micro-interactions

**AI-default cliché.** Every button gets the same `:hover` fading in a pale, low-opacity tint of the accent (`background: rgba(accent, .1)`); every link gets a generic underline; the nav gains a frosted `backdrop-filter: blur()` plus a solid or tinted background and a border-bottom on scroll. One trick, applied everywhere.

#### Buttons and CTAs

- **Full-token flood + text inversion**: on hover the control's background jumps to a solid, full-saturation token and the text or icon flips to the contrast token. The flood color is chosen per context, not globally. *Verified:* Lando `.f1-highlight-grid:hover{background-color:var(--color--lime);color:var(--color--black)}` (CSS line 5569) and the schedule variant `.f1-highlight-grid.is-schedule:hover{background-color:var(--color--dark-green);color:var(--color--lime)}` (line 5594); Siena `.all-work-cta-w:hover{background-color:#000;color:#fff}` at `.5s var(--easeOutQuint)`, with the nested `.down-arrow-btn.black{transition:…5s var(--easeOutQuint);bg:#fff;color:#000}` inverting the arrow; `[data-btn=explore]:hover` floods the background SVG to `#fff` and strokes the line `#000`. Two sites, so this is the archetype's real button-hover grammar, with one disclosure that applies wherever the Lando + Siena pair is the base: Siena is also the parent reference's canonical Editorial exemplar, so the two-site foundation overlaps that archetype. **Where it fits.** Controls sitting on a photographic or dark canvas, where one decisive state change carries the interaction.
- **Already-solid CTA, motion-only hover**: the primary CTA ships filled with the accent at rest, no color on hover. *Verified:* Lando `.btn-w` is solid `#D2FF00` background, `#282C20` text, 1px lime border, `.54rem` radius at rest, and carries **no `:hover` rule** in CSS; the hover is a JS/Webflow transform (press, scale, icon nudge; exact transform unverified). **Where it fits.** Builds where the accent is the brand signature and the button reads as a lit object rather than a state machine. It is the strongest counter to the pale-tint reflex: the button is already the loudest thing on the page, so hover only nudges.
- **Doubled-label roll**: the label is duplicated in two stacked or side-by-side copies inside an `overflow:clip` box; hover translates the pair so a fresh copy slides in. *Verified:* Lando `.nav-menu-link-w { overflow:clip }` with doubled DOM text ("HomeHome", "On TrackOn Track") and `.nav-menu-link-w:hover{color:var(--color--lime-off)}` (line 6177); Siena `[data-btn=explore]:hover [data-after]{ transform: translateY(-150%) }` plus `[data-x]{ transform: translate(100%) }` at `.8s` easeOutQuint, staggered `.1s`. `overflow:clip` appears **23 times** in Lando's CSS and once in Siena's. **Where it fits.** Nav items and text CTAs, where the motion does not change layout.
- **Magnetic pull**: the button follows the cursor a fraction of the offset while the pointer is inside its bounds, snapping back on an elastic or expo ease on leave. *Reference:* Cuberto `mouse-follower` (`stickDelta: 0.15`) and Codrops "Magnetic Buttons"; per-build strength and duration live in the source, not the article. **Where it fits.** A single hero CTA: one magnet per view, never a page of them.

#### Text links

- **Adopt-the-accent recolor**: on hover the element takes the site's one saturated accent, the color otherwise reserved for the CTA. *Verified, two sites:* Lando nav-link → lime-off `#B2C73A`, `.helmet-grid-extender-img` → lime; Siena `.review-he` → red, `.menu-film-direct-link svg path` → `#fff`/`#000`. **Where it fits.** Text links and metadata rows. The accent is scarce, and recolor is how a link comes alive precisely because that color means "active" everywhere else.
- **Plain underline, supporting rather than signature**: animated underline-draw is largely absent from these two cinematic winners. Lando rich-text links use a bare `text-decoration: underline`; Siena footer links reveal via `opacity` plus an arrow rotate `-135deg`, with no draw. The kinetic underline belongs to the editorial archetype. **Where it fits.** Sparingly, and only inside long-form body copy.

#### Images and cards

- **Inner scale 1.1**: the image scales to `1.1` inside a fixed frame that clips the overflow. *Verified, two sites:* Lando `.helmet-grid-item-w:hover .helmet-grid-item-img-helmet { transform: scale(1.1) }`; Siena `.previousnext-item:hover .full-img-w { transform: scale(1.1) }`. The amplitude is **10%, not 3%**. A `1.03` scale is imperceptible and reads as dead; a grep for `scale(1.02)` and `scale(1.03)` returns **zero hits** on both bundles. **Where it fits.** The default media hover.
- **Clip-path ellipse uncover**: the media is revealed or hidden by a top-anchored elliptical mask that grows. *Verified, Lando-signature:* `[data-helmet-item]:hover .reveal-img { clip-path: ellipse(100% 120% at 50% 0%) }`; `.part-i-video-w:hover { clip-path: ellipse(80% 50% at 50% 50%) }` (single-source for this hover trigger). The `ellipse(100% 120% at 50% 0)` → `ellipse(100% 0% at 50% 0)` pair recurs across Lando's scroll reveals, so the top-anchored form is the whole-site motif rather than a one-off, and the `50% 50%` hover anchor sits outside that family (Mid-page aliveness, Channel C). **Where it fits.** Reveals carrying brand shape themselves: a visor curve, a lens.
- **Edge-anchored panel wipe**: a solid pseudo-element grows via `transform: scaleY(0→1)` from an edge. Fill done right: a real color panel wipes in, it does not fade. *Verified, single-source:* Siena `[data-hover=bggrow]:hover:before { transform: scaleY(1) }`. This is the honest version of the cliché: targeted to specific elements, full-opacity, directional. **Where it fits.** Cards taking a fill where a full recolor would be too heavy.

#### The nav bar

- **Transparent, adaptive, chrome-free**: the nav is `position: fixed`, `background: transparent`, no `backdrop-filter`, `border-bottom: 0 none`. Its text and icon color transitions (Lando: `color .75s cubic-bezier(0.65,0.05,0,1)`, the site's `--cubic-default`/`--duration-default` pair) to stay legible over whatever section scrolls under it. *Verified, two sites:* Lando `.css-nav` (transparent, no backdrop, no border, cream text adapting to dark and light sections); Siena `.nav-w` (fixed, transparent, no backdrop, no border). A grep returns `backdrop-filter` = **0** and nav `border-bottom` = **0** on both bundles. **Where it fits.** The archetype's default nav; a solid nav bar belongs to the corporate/SaaS archetypes.

### Motion and scroll

**AI-default cliché.** Every section fades up 20px on a 0.6s ease-out `IntersectionObserver`, uniform for the whole page; "parallax" is a background image translating at 0.5×; scroll is untouched, so nothing feels choreographed.

- **Scrub-linked master timeline, pinned**: a single ScrollTrigger with `scrub: 1` (or `0.8`) pins a section and drives a timeline whose segments carry their own durations and eases; scroll position *is* the playhead. *Reference params (Codrops cinematic tutorial):* `scrub: 1`, `pin: true`, camera segments of `duration: 1 / 2 / 3.5`, ScrollSmoother `smooth: 4`. *Winner mechanic:* Lando scrubs a `<video>` `currentTime` to scroll and scrubs the hero-next-race clip-path open and closed. **Where it fits.** The page's one signature sequence, the moment that carries memory weight.
- **A named cinematic easing family, reused everywhere**: winners define two to four custom cubic-beziers and route nearly every transition through them, which is what makes variety cohere (see Composition). *Verified (Siena):* `easeOutQuint (.23,1,.32,1)` on almost every hover and slider transition, `customEase (.19,1,.22,1)`, `easeOut (.77,0,.175,1)`. *Verified (Lando):* `cubic-bezier(0.65,0.05,0,1)` at `0.75s` for nav and hamburger, declared as `--cubic-default` / `--duration-default` in the inline `<style>`. *Verified (Lusion):* `cubic-bezier(.4,0,.1,1)` ×32 and `cubic-bezier(.35,0,0,1)` ×32 dominate, with `cubic-bezier(.1,0,.1,1)` ×3 and `cubic-bezier(.16,1,.3,1)` ×2 trailing, at `.3–.5s` on transform and color. *Reference (Codrops):* cinematicSilk `.45,.05,.55,.95`, cinematicSmooth `.25,.1,.25,1`, cinematicFlow `.33,0,.2,1`. **Where it fits.** A named set of 2–3 curves per site, with no ad-hoc eases alongside them.
- **Camera through Z-depth, not layer parallax**: scroll moves a real camera forward through a 3D scene with true depth and physics-weighted inertia instead of sliding 2D layers. *Sites:* Oryzo/Lusion (camera through true Z-axis depth), Explore Primland (scroll-driven terrain flythrough), Cartier (scroll moves the visitor between 3D rooms). **Where it fits.** WebGL media carrying a spatial story.
- **Staged scroll beats (entrance, hold, exit)**: each section is a discrete narrative beat rather than a continuous reveal: content enters, holds while a sub-action plays, then exits. *Verified param (Codrops text choreography):* fade-in `duration .2` → hold `.6` → fade-out `.2` at `scrub 0.8`. *Sites:* Shopify Editions (scroll position as narrative beats), Terminal Industries (scroll shifts 3D visuals into wireframe). **Where it fits.** Product and story pages with a fixed number of moments.
- **Full-bleed page-transition wipe**: a top-layer overlay covers the viewport during route change, a cinematic cut rather than a white flash. *Verified:* Lando `.transition-w` (`z-index: 9999`, full-viewport); Siena `--panels-duration: .9s` panel system. **Where it fits.** Multi-page immersive sites, where navigation reads as a scene change.

### Text effects

**AI-default cliché.** The SplitText per-character fade-up at `stagger: 0.05`, applied identically to every heading on the page, so no headline is more important than another.

- **Variable-font axis animation**: display type animates `font-variation-settings` (weight, width) rather than opacity or position, so letters thicken and widen in place. *Verified (Lando, single-source but a strong signature):* `.text-nav-link { font-variation-settings: "wght" 660, "wdth" 93; text-shadow: 0 5.25rem; transition-property: color; transition-duration: .6s; transition-timing-function: cubic-bezier(.19,1,.22,1) }` at CSS lines 6187–6195, with `font-size: 5.25rem` on the same rule outside that quoted range; the `text-shadow` doubles the glyphs exactly one line-height down for the roll, only `color` transitions in CSS, and the axis move itself is JS. **Where it fits.** The hero's one signature type move; it reads as bespoke because almost nobody ships it.
- **Masked line or word reveal**: lines sit in `overflow: clip` boxes and translate in from below with a hard mask edge and no fade. *Verified, two sites:* Lando nav links on `cubic-bezier(.65,.05,0,1)`; Siena explore-CTA label swap. *Reference stagger:* Codrops per-char `stagger: 0.02`, char reveal `0.2–0.25s`. **Where it fits.** The default headline entrance, cleaner than a fade.
- **Kinetic type as image**: letters scale, split, and morph during scroll; type *is* the hero, not a caption over one. *Sites:* Obys "Typography Principles" (letters scale, split, morph on scroll), Shopify Editions (particle-dispersing type). **Where it fits.** Pages with no photographic hero, where the wordmark or headline carries the whole frame. The archetype's strongest beat-SOTD text move.
- **Full-height marquee**: a running text band at `100svh`. *Verified, single-source:* Lando `.c.is-marquee { height: 100svh }`. **Where it fits.** Sparingly, as a section-scale transition rather than decoration.

Signature versus supporting: variable-font axis and kinetic-type-as-image are signatures, one per page. Masked line reveal is supporting, the reliable everyday entrance. Per-char fade is the cliché; the masked reveal is what these winners ship instead.

### Cursor and pointer

**AI-default cliché.** A small circle `div` lagging the pointer with `cursor: none` on the body, applied to every page regardless of whether it earns its keep, often hurting the Usability axis (30% of the Awwwards score) on mobile and for precision targets.

- **Deliberate default cursor**: the winner move here. The top two sites keep the OS cursor. *Verified:* Lando `getComputedStyle(body).cursor === "auto"` with no follower element; Siena `main.css` carries no `cursor: none` and no follower rule. Two of the highest-decorated sites in the line choose not to hijack the cursor. **Where it fits.** The line's default; a custom cursor appears only where a specific mechanic justifies it, never reflexively.
- **State-morphing follower, when justified**: a follower lags the pointer and changes shape or label per element class: a dot over blank space, a ring over links, a "View" label over media, an arrow over sliders. *Verified library defaults (Cuberto `mouse-follower`):* `speed: 0.55`, `ease: "expo.out"`, velocity skew `skewingText/Icon/Media: 2` with `skewingDeltaMax: 0.15`, magnetic `stickDelta: 0.15`, `hideTimeout: 300`; states `-hidden / -pointer / -text / -icon / -active / -media`. **Where it fits.** Cursors carrying information the layout cannot ("drag", "view", "play") with distinct states per element class, which is itself a composition tool (see Composition).
- **Cursor-driven scene reveal**: the pointer uncovers detail in a WebGL scene (geometry, lighting, focus) rather than decorating the pointer itself. *Sites:* Hubtown/Unseen (cursor uncovers geometry and lighting), Telescope/Vanderpotte (cursor drives a focal zoom via overlapping masks). **Where it fits.** Heroes that are live canvases, where the pointer reads as lighting the scene.

### Loader effects

**AI-default cliché.** A centered spinner, or a bare `0–100%` counter on a blank screen, hard-cutting to the page the instant it hits 100, with no continuity between the loader and the first frame.

This is the archetype where the intro is load-bearing: the heavy WebGL and video payload needs a covering sequence, so winners choreograph the wait into the first act.

- **Brand-object assembly → reveal wipe**: the preloader builds the site's signature object (helmet, wordmark, logo) while assets stream, then wipes or clip-paths open into the live hero so there is no cut. *Sites:* Lando (Rive-powered intro + GSAP, the brand object assembling before the hero; documented by the studio and GSAP, frame timing observed). The top-anchored `ellipse(… at 50% 0)` geometry that recurs across Lando's scroll is the hand-off mask. **Where it fits.** Brands with one iconic object.
- **Progress-as-narrative**: the load percentage drives a real visual (a value counting, a scene lightening, a camera pulling back) so the counter is diegetic rather than a UI widget. *Sites:* Active Theory boots into a full-screen WebGL intro that transitions fluidly into navigation; the Awwwards "Loading" collection catalogs the pattern. Numeric choreography observed. **Where it fits.** Shader-heavy sites where the wait is unavoidable, and the wait becomes the opening shot.
- **Panel/curtain hand-off**: full-viewport panels cover the boot, then slide or scale away to expose the hero, sharing machinery with the page-transition wipe under Motion and scroll. *Verified adjacent:* Siena `--panels-duration: .9s`; Lando `.transition-w` overlay. **Where it fits.** Sites already carrying a page-transition system, reused for the intro so entry and navigation share one grammar.

### Composition

The two deepest-evidence sites solve the same problem (every element class must feel distinct yet part of one voice) in opposite ways. The shared lesson: **cohesion comes from constants (one easing family, one scarce accent, one grammar), and variety comes from a different mechanic per element class.** Never one mechanic everywhere; never a different easing per element.

**Lando Norris: cohesion by scarce accent + shared geometry, no custom cursor.** Mapped by element class, all verified from CSS:

| Element class | Hover mechanic |
|---|---|
| Primary CTA (`.btn-w`) | ships solid lime with dark-green text, a lit object; hover is motion-only |
| Card / schedule grid (`.f1-highlight-grid`) | full flood + inversion; flood color varies (lime with black text, or dark-green with lime text) |
| Image / media (`.helmet-grid-item`, `.part-i-video-w`) | clip-path ellipse uncover + inner `scale(1.1)` + accent recolor to lime |
| Nav link (`.nav-menu-link-w`) | masked vertical swap under `overflow:clip` + color → lime-off |
| Text link | color → lime, bare underline |
| Nav bar | transparent, text color adapts per section, no backdrop, no border |
| Cursor | OS default |

What makes it one voice: the single lime accent (`#D2FF00`, plus muted `#B2C73A` for hover) is the only saturated color and it means "active" on every class; the top-anchored ellipse (`… at 50% 0`) is the reveal shape for hero, cards, video and the intro hand-off; one timing DNA (`cubic-bezier(0.65,0.05,0,1)` at `0.75s`) governs the chrome. Five mechanics, one accent, one shape, one ease. Lando's CSS declares only **26** `:hover` rules in total (13 in each of the two near-duplicate files); the variety is not in hover-rule count.

**Siena Film Foundation: cohesion by one easing family + inversion grammar.** Mapped by element class, all verified from CSS:

| Element class | Hover mechanic |
|---|---|
| Explore CTA (`[data-btn=explore]`) | background floods `#fff`, line and icon invert to `#000`, label swaps (`translateY(-150%)` + `translate(100%)`), `.8s` |
| Work CTA (`.all-work-cta-w`) | full black flood + white text, `.5s` |
| Footage menu (`[data-footagemenu]`) | color → `#fff`, background SVG → `#000`, `.6s` |
| Menu film item | reveals the arrow link (`opacity 1` + `scale 1`) while the leading dot collapses (`scale 0`) |
| Slider / review | accent red recolor + svg `scale .95` + a hidden CTA height-reveals (`grid-template-rows: 0→1fr`) |
| Footer link | `opacity` reveal + arrow rotate `-135deg` |
| bggrow elements | `scaleY(0→1)` panel wipe |
| Nav bar | transparent, no backdrop, no border |
| Cursor | OS default |

What makes it one voice: one easing family, `easeOutQuint (.23,1,.32,1)`, runs through nearly every transition regardless of element; one grammar, inversion and reveal-from-edge (fill flips to a solid, text flips to contrast, hidden things grow into view), repeats while the mechanic differs per class (flood versus swap versus scale versus height-reveal versus rotate); one scarce accent, red, held back for the live slider state only. Siena's CSS also ships a declarative stagger ladder, `[data-delay=".1"]{transition-delay:.1s}` through `[data-delay="2"]{transition-delay:2s}`, with rungs at .1 / .2 / .3 / .4 / .5 / .6 / .8 / 1 / 1.2 / 1.4 / 1.6 / 1.8 / 2 and no .7, so delay is authored in markup, not scattered through JS.

**Lusion v3** sits at the opposite density: **71** `:hover` rules in `about.css` against Lando's 26, routed through two dominant beziers. High hover count with a two-bezier constant is the same trick from the other end.

**The transferable rule.** For a build to compose instead of repeat: pick one accent (used only for "active"), one easing family (2–3 named beziers), and one grammar (inversion, or reveal-from-edge). Then give each element class its own mechanic: button floods, image scales `1.1`, link swaps under a mask, card inverts, slider recolors, media uncovers via clip-path. Variety lives in the mechanics; unity lives in the constants. A custom cursor, if present, is itself an element-class dimension (its `-text`/`-media`/`-pointer` states differentiate what it hovers), but two of the top winners prove it is optional.

### Anti-signals — absent from every winner examined

- **Pale, low-opacity tint fill on buttons** (`background: rgba(accent, .1)`). Winners flood full-token and invert, or ship the CTA already solid. Zero pale tints found.
- **Frosted-glass nav on scroll**: `backdrop-filter: blur()` plus a solid or tinted background appearing on scroll. `backdrop-filter` greps to 0 on both bundles.
- **A border-bottom under the nav bar**, matched or contrasting. `border-bottom: 0 none` verified on both.
- **One universal hover for all element classes.** Every winner differentiates button ≠ card ≠ image ≠ link ≠ nav.
- **Reflexive custom cursor** with `cursor: none`. The two top sites keep the OS cursor.
- **Imperceptible hover amplitude** (`scale(1.02)`, `scale(1.03)`): 0 grep hits; winners use `1.1` or a full flood.
- **Bare spinner or naked % counter with a hard cut.** Winners choreograph the load into the opening shot.
- **Animated underline-draw as a primary link treatment** in this archetype: it belongs to editorial; here links recolor to the scarce accent or reveal an arrow.
- **A different easing per element.** Winners route everything through 2–3 named beziers.

## Page recipe

### Named page shapes

Section count and length split hard by expression. The personality/product page runs long: Lando, 12 sections, ~16.5 viewport-heights, `scrollHeight` **10369px** at `innerHeight` **630** (10369/630 = 16.46). The studio and catalog pages run as custom-scrolled or single-scene experiences whose `scrollHeight` stays pinned at ~1vh with transform-driven motion: Siena 630/630 = 1.0, Lusion 630/630 = 1.0, Active Theory 630/630 = 1.0, all winner-verified. The `630` is the viewport height these figures were measured at; Siena's same 1.0 equality holds at `676` ([`editorial.md`](./editorial.md)). Four named shapes cover the line.

#### Shape A — The Portrait Procession (Lando Norris)

(winner-verified section order; the pinned horizontal track is shipped / observed)

**Fingerprint.** A corner-locked wordmark over a full-bleed frontal portrait on a light canvas, then a long vertical procession of full-viewport chapters, each a facet of the person (on-track, off-track, honors, partners, socials), with one horizontal-scroll pinned interlude, closing on a dark inverted portrait footer carrying an oversized split-color valediction. The palette flips light→dark exactly once, at the close, bookending the hero. Rest beats are short bridge sections between the full-height chapters. For athlete, personality, and founder portfolios with many facets and one face.

**Ordered skeleton**: class names and heights read element-by-element from the DOM. Intensity `n/10` is a comparative 1–10 estimate of attention load (defined in [Composition Chains](../winners/composition-chains.md)):

1. `s home-hero` (630px): frontal portrait photo on cream + topo-line silhouette · attention · 9/10 · seam: marquee slides under
2. `s home-marquee` (630px, absolute overlay): scrolling word strip · rhythm · 4/10
3. `s` (857px bridge): transition breath · rest · 2/10
4. `s is-horizontal-track` (2154px ≈ 3.4vh): pinned horizontal "ON TRACK" gallery · proof · 8/10 · seam: pin release → vertical resume
5. `s is-otot-home`: "ON / OFF TRACK" split · understanding · 6/10
6. `s is-otot-end`: split closer · understanding · 4/10
7. `s home-helmets` (1414px ≈ 2.24vh): "Helmets" 3D rotating gallery · proof/spectacle · 9/10 (climax candidate) · seam: clip reveal
8. `s` (397px bridge) · rest · 2/10
9. `s is-lando-exe`: "World Drivers' Champion" honor · proof · 7/10
10. `s is-home-collabs`: "partners" / "&campaigns" · proof · 5/10
11. `s is-callout-socials`: "what's up On Socials" · engagement · 5/10
12. `s is-footer` (computed `background: rgb(244,244,237)` = `#F4F4ED`): "Always bringing the fight." full-bleed helmet portrait + split headline · close (climax) · 9/10

Climax is doubled: the "Helmets" gallery mid-page and the footer valediction at the base. Seams are clip-path masked cross-fades (`ellipse(100% 120% at 50% 0%)` recurs site-wide), never hard cuts.

#### Shape B — The Gated Index (Siena Film Foundation)

(winner-verified)

**Fingerprint.** A branded splash gate in a metaphor costume (a cinema ticket, "ADMIT ONE", ticket number "004") that must be dismissed by clicking ENTER, opening into a custom-scrolled index of self-contained project cards. Each card is a film-still or trailer surface with a masked-reveal title and one CTA. The footer is functional but still costumed. For film, production, and catalog brands with discrete named works.

**Ordered skeleton:**

1. Splash gate: "SIENA" vintage-serif wordmark, "FILM FOUNDATION" letterspaced, ticket-stub "ENTER →" · attention/threshold · 8/10 · seam: gate dismiss
2–9. Eight film-project cards, one register each (Savoy · Moon in the 12th House · Taboo · Kafka's Last Trial · My Project X · Ana Maxim · Outsider Freud · By Any Means), each with a masked-reveal title plus an `EXPLORE` CTA · proof · 7/10 each. Two scoping notes from the live read ([`editorial.md`](./editorial.md)): the visible label is `EXPLORE` (`[data-btn=explore]`), while `SEE CASE` ships ×8 in the raw HTML and never surfaces in the rendered DOM; and only `SAVOY` is DOM-confirmed; the other seven titles render inside the WebGL canvas and come from the source HTML
10. Footer: "©2024. SIENA FILM FOUNDATION." + legal + "EMAIL US" · close · 3/10

Media: **3** `<video>` elements + **1** WebGL canvas (winner-verified counts). The DOM stores each card title as two overlaid copies (`h2[0]` reads literally `"SSaavvooyy"`, interleaved duplicates), the fingerprint of the doubled-label roll.

#### Shape C — The Studio Manifesto → Project Reel (Lusion v3)

(winner-verified)

**Fingerprint.** A declarative first-person-plural statement hero set over a live 3D scene, a one-line manifesto section, then a scrolling reel of 3D project cards each tagged by discipline, closing contact-first with a real physical address. The claim and its proof, the canvas, share every fold. For agencies, studios, and multidisciplinary makers.

**Ordered skeleton:**

1. Hero: "We create 3D visual storytelling and interactive web experiences that help brands stand out" over a 3D canvas, "SCROLL TO EXPLORE" cue (uppercase in the DOM) · attention · 8/10
2. Manifesto: "Bold Ideas, Brought to Life" + "We combine design, motion, 3D, and development…" · understanding · 6/10
3–N. Project reel (**OryzoAI** · OffTheOak · DevinAI · Porsche: DreamMachine · SyntheticHuman · Meta: SpatialFusion · **Spaace-NFTMarketplace** · **DDD2024** · **ChooChooWorld** · SodaExperience), each a 3D card prefixed with a discipline list ("concept • web • design • development • 3d • animation") · proof · 7/10 each
4. "See all projects" → contact-first footer (address, socials, newsletter) · close · 6/10

WebGL throughout: **3** canvases, **0** videos. The DOM stores project titles quadrupled (`"OOOOrrrryyyyzzzzoooo"` = "Oryzo"), a layered split-letter reveal, and the quadrupling is what makes the reel names easy to mis-transcribe: the four bolded names above decode the multiplication (12 D's ÷ 4 = "DDD"; 8 o's ÷ 4 = "oo").

#### Shape D — The Single-Scene World (Messenger, Active Theory)

(technique / observed)

**Fingerprint.** No scroll narrative: one continuous WebGL scene *is* the site. Navigation and content live inside the 3D world; a loader boots directly into the scene; sound is a first-class layer. Messenger: a tiny GPU-rendered planet where the visitor pilots deliveries, console-game physics in a browser tab, built on Three.js / WebGL / WebSockets (tech tags confirmed on the Awwwards entry). Active Theory: a canvas portfolio fronted by an audio toggle and a capability-filter menu, all display copy canvas-rendered; the DOM headings are empty and the nav reads "Toggle Audio / Work / Contact / -> games / -> multiplayer / -> XR / VR / AI / -> installations / -> websites" (winner-verified verbatim). For experiential, game-adjacent, and virtuoso-developer brands. The shape presupposes a WebGL build budget.

### Hero architectures

#### H1 — Corner-lockup portrait (Lando Norris)

(winner-verified structure, shipped composition)

The wordmark sits in a corner, not centered-giant: `<h1>` "Lando Norris" top-left as a two-line heavy-grotesque lockup ("LANDO / NORRIS"), `<h2>` subhead below it. The face fills the fold; type steps aside.

- H1 text "Lando Norris"; subhead H2 raw `textContent` **"2025 Mclaren Formula 1 Driver"**, with a lowercase "c", while `document.title` separately reads "2025 McLaren Formula 1 Driver — Lando Norris". Both strings are verbatim from the DOM.
- Type: `font-family: "Mona Sans Variable", Arial, sans-serif` (winner-verified computed).
- `<body>` computes `background: rgb(40,44,32)` = `#282C20` with `color: rgb(244,244,237)` = `#F4F4ED`. The page is predominantly dark; the `#F5F2EC`–`#FAF7F0` cream register lives inside the hero canvas and returns at the footer.
- Media: full-bleed frontal portrait photograph, subject centered and symmetric, high-key even studio light, near-shadowless, neutral-warm grade on near-white cream; faint gray topographic contour lines behind form a ghosted helmet-visor silhouette (shipped, screenshot). **21 canvases** page-wide plus a Rive node count that depends on the selector: 35 Rive-matched nodes by DOM match, 17 `data-rive-artboard` mount points (3 matching the literal `canvas[data-rive]` selector, 5 unique `.riv` files); cite as ≥N ranges on an actively patched build. The hero is a Rive/WebGL composite, not a flat image.
- Nav interplay: fixed transparent nav; "L7" monogram top-center; lime "STORE" pill plus a menu-toggle icon top-right; a "NEXT RACE / SPA GP / MCLAREN F1 SINCE 2019" status card bottom-left (shipped; this copy string is committable but not independently verified).
- CTA: two, lime "STORE" in the nav and a primary "Load Norris" button (winner-verified DOM label; a pun on the loading state).

Entrance beat table, reconstructed from winner-verified easing and mechanic constants plus observed choreography, since the intro overlay unmounts on load and per-element durations are not a live scrub:

| # | Element | Transform | Duration | Easing |
|---|---|---|---|---|
| 1 | Rive brand-object (helmet/wordmark) assembly while assets stream | build in place | tied to load (observed) | Rive/GSAP (observed, unverified) |
| 2 | Reveal wipe into live hero | clip-path `ellipse(100% 120% at 50% 0%)` grows from top | ~0.8–1.2s (observed) | `cubic-bezier(.65,.05,0,1)` (winner-verified, inline `<style>`) |
| 3 | Headline lines (`overflow:clip` boxes) | `translateY` up, hard mask edge, no fade | staggered (technique) | `cubic-bezier(.65,.05,0,1)` (winner-verified) |
| 4 | Nav text/icon color settle | `color` transition to stay legible over the fold | `.75s` (winner-verified `--duration-default`) | `cubic-bezier(.65,.05,0,1)` (winner-verified) |

#### H2 — Statement-over-canvas (Lusion v3, Active Theory)

(winner-verified copy)

A first-person-plural declarative sentence over a live 3D/WebGL scene, with a "scroll to explore" cue at the base and minimal chrome. The claim and the proof share the fold.

- Lusion H1: "We create 3D visual storytelling and interactive web experiences that help brands stand out" (DOM stores it as line-split spans); microcopy "SCROLL TO EXPLORE", uppercase in the DOM. Type `font-family: Aeonik` (winner-verified computed); nav Home / About us / Projects / Contact / Labs plus a "Let's talk" CTA. The body computes `rgb(255,255,255)`: this is a **light-key** studio environment, not a dark canvas.
- Active Theory: no DOM headline; the statement is inside the canvas; the fold's only affordances are "Toggle Audio", "Work", "Contact". Sound-first: an audio player ("<< Song--Artist >>", prev/next, Toggle Audio) is part of the hero chrome. Body computes `rgb(0,0,0)`.

#### H3 — Costumed splash gate (Siena Film Foundation)

(winner-verified copy, shipped composition)

The gate *is* the hero: an oversized "SIENA" vintage high-contrast serif wordmark centered on pure black, "FILM FOUNDATION" letterspaced beneath, and a single ticket-stub "ENTER →" affordance with a perforated dashed divider (shipped, screenshot). It is its own fixed panel rather than a scrim over the reel: `.preloader-w{position:fixed; inset:0; z-index:99999999; background-color:var(--black); display:none}` with `.show{display:flex}`, carrying a `.preloader-video{height:50svh}` (`100svh` on mobile) and a `.preloader-btn{transform:translateY(200%); font-family:Neue Brucke}` that slides up into place ([`../surfaces/preloaders.md`](../surfaces/preloaders.md)). `<body>` computes `background: rgb(0,0,0)`, `color: rgb(250,247,239)` = `#FAF7EF`, `font-family: "NB International", Arial, sans-serif`; the display wordmark is a vintage serif. The gate node's isolated `textContent`, excluding style and script children, is exactly `"SIENAADMIT ONE004"`, and **not** doubled, unlike the film titles.

### Loader and intro

Two hand-off families, plus one absence pattern.

- **Auto-retracting object-assembly curtain (Lando).** A Rive/GSAP preloader builds the signature object while assets stream, then opens into the live hero via the top-anchored `ellipse(… at 50% 0)` hand-off mask so there is no cut (observed). The "Load Norris" pun labels the wait. Verified negative: no `[class*=load]`, `[class*=preload]`, or `[class*=curtain]` node survives post-load; the curtain unmounts rather than hiding. The negative does **not** extend to `[class*="intro"]`, which still matches surviving content nodes (`text-cta-short-intro`, `callout-socials-intro-w`).
- **Held, clickable costumed gate (Siena, Active Theory).** Not an auto-dismissing loader but a threshold the user must act on. Siena's is a cinema ticket ("ADMIT ONE / 004", ENTER stub; winner-verified DOM plus shipped visual); Active Theory's is an audio consent ("Toggle Audio", winner-verified). The gate is the brand's first gesture, and it doubles as the sound-autoplay unlock the archetype needs (the sound-unlock role is inferential; 3 `<video>` elements are present on Siena).
- **Absence as data (Lusion).** Near-instant paint; the intro is the "SCROLL TO EXPLORE" cue and the 3D scene settling: no curtain, no counter, no loader node in the DOM. A verified pattern, not an omission.

Synthesis: the intro either retracts on its own after composing the object (Lando) or waits for one deliberate click that is itself in-character (Siena ticket, Active Theory audio). A bare spinner or naked % counter that hard-cuts to the page is absent from every winner examined.

### Route transitions

The line is dominated by single-scene and anchored-scroll pages, so true multi-route transitions are secondary, but where routes exist, the transition rhymes with the loader.

- **Lando**: single page with anchored full-height sections; sub-routes (On Track, Off Track, Store) exist; `view-transition-name` for thumbnail→hero morphs (observed, unverified).
- **Siena**: film card → case study via "SEE CASE STUDY"; the Webflow shell plus Vercel/Next overlay implies a cover/curtain into the detail surface echoing the ticket cut (single-source, observed; the detail transition was never driven).
- **Lusion**: project card → project page, multi-page; the transition is a WebGL cover/morph consistent with the reel (observed). A `back` link is present in the DOM (winner-verified) but not on the homepage, so where it lives is unresolved.
- **Messenger / Active Theory**: no routes; movement is camera and scene motion inside one continuous canvas (observed).

### Copy voice

Verbatim per winner, all read from live DOM unless tagged:

- **Lando Norris.** H1 "Lando Norris"; subhead "2025 Mclaren Formula 1 Driver"; sections "Helmets", "World Drivers' Champion", "Always bringing the fight."; nav "On Track" / "Off Track" / "Partnerships" / "Calendar" / "Store"; primary CTA "Load Norris"; footer "© 2026 Lando Norris. All rights reserved". Voice: third-person-brand, ultra-terse; sections are noun-labels, not sentences; verbs are idioms or imperatives ("Load Norris", "bringing the fight"); the one full stop is emphatic on a fragment ("Always bringing the fight."). Refuses explanatory body copy, "welcome to", adjectives, any sell.
- **Lusion v3.** H1 "We create 3D visual storytelling and interactive web experiences that help brands stand out"; manifesto "We combine design, motion, 3D, and development to create digital experiences that feel visually striking and technically seamless. From campaign launches to immersive brand worlds, we build work that captures attention and invites interaction."; section "Bold Ideas, Brought to Life"; microcopy "SCROLL TO EXPLORE"; footer address **"Suite 2, 9 Marsh Street, Bristol, BS1 4AA, United Kingdom"**; the DOM leaf-node chain reads `["Suite","2","9","Marsh","Street","Bristol,","BS1","4AA","United","Kingdom"]`, with `footer-address-line` #1 carrying "Suite" + "2" and the next line carrying "9 Marsh Street". Voice: first-person-plural, one long confident declarative, warm-technical verbs (create, combine, build, capture, invite), Title-Case headers; refuses empty hype by naming disciplines.
- **Siena Film Foundation.** Film titles "Savoy", "Moon in the 12th House", "Kafka's Last Trial", "By Any Means"; splash "SIENA" / "ADMIT ONE" / "004"; CTAs "SEE CASE STUDY", "EXPLORE", "EMAIL US", "ENTER"; nav "WORK" / "About" / "Contact"; footer "©2024. SIENA FILM FOUNDATION." (shipped, via fetch); a recurring film descriptor "A film based on a true Story" (shipped, via fetch). Voice: caps-locked institutional terseness in a cinema lexicon (ADMIT ONE, EXPLORE, WORK); refuses first-person and adjectives; the copy is a marquee, not prose.

**Voice formula.** Person tracks the subject: third-person for the personality/product (Lando), first-person-plural for the studio (Lusion), no-person institutional caps for the catalog (Siena). Sentence length is label-length (1–4 words) by default; only the studio spends one long declarative. Verb temperature runs idiomatic-warm ("bringing the fight", "brought to life") over corporate. The punctuation signature is the emphatic terminal period on a fragment. What the voice refuses across all three: explanatory paragraphs, feature bullets, exclamation marks, and hype adjectives; the visual persuades, copy only labels and punctuates.

### Imagery art direction

- **Lando: editorial photographic, one treatment page-wide, palette-flipped at the close.** Subject: the person, and the object, the helmet. Crop: tight head-and-shoulders, centered, symmetric. Light: high-key even studio, near-shadowless. Grade: neutral-warm on cream in the hero; the footer inverts the same subject (helmet portrait) on dark olive `#282C20`. Treatment: subject isolated and composited onto a brand field of gray topographic contour lines, a repeating motif. The whole page is portrait-on-field; the register flips light→dark once.
- **Siena: cinematic-poster film stills.** Subject: film frames and trailers on a `#000` body, 3 `<video>` elements. Grade: dark, high-contrast, poster-like, vintage serif overlaid. One dark treatment page-wide.
- **Lusion / Messenger / Active Theory: no photography.** The image is live-rendered 3D: physical materials, HDRI or single-source light, fog and bloom. The art direction is shader and material choice, not a photo grade. The dark-canvas grade holds for **Active Theory** (`#000`) and **Messenger** only; Lusion's body computes `rgb(255,255,255)` and the v3 hero is a light-key studio environment.

Formula: **either one editorial photographic treatment applied page-wide (subject isolated on a brand field, high-key or cinematic-dark) or no photography at all, where the render is the image.** A mixed stock-photo grid appears in no winner examined.

### Footer

Two footer modes; neither is bare functional chrome.

- **The oversized valediction fold (Lando): designed close, bookends the hero.** A full-bleed dark-olive fold: a real photograph of Lando in his lime race helmet bleeding off the bottom, an oversized split-color headline "ALWAYS BRINGING THE FIGHT." (white + lime, layered), his handwritten signature in lime above it; two nav columns ("PAGES": Home / On Track / Off Track / Calendar / Store; "FOLLOW ON": Tiktok / Instagram / Youtube / Twitch); a sponsor-logo marquee strip (Quadrant, Bell Helmets, Tumi, Pure Electric, Android, PAP, Monster Energy, L7); a centered lime "BUSINESS ENQUIRIES ↗" pill; a lime full-width baseline strip carrying "© 2026 Lando Norris. All rights reserved" left and "PRIVACY POLICY / TERMS" right. CSS: `s is-footer` computes `background: rgb(244,244,237)` = `#F4F4ED` under a `rgb(40,44,32)` dark overlay, with the lime baseline strip at `rgb(210,255,0)` = `#D2FF00` (winner-verified; 176 elements page-wide use the lime). It inverts the hero's palette and swaps the bare face for the helmet, a closing bookend. The sponsor names and the nav-column labels are committable copy, not independently verified.
- **The contact-first grounding block (Lusion): functional-plus.** "Let's talk" CTA, a real physical address ("Suite 2, 9 Marsh Street, Bristol, BS1 4AA, United Kingdom"), socials (Twitter / X, Instagram, Linkedin), "Subscribe to our newsletter". Grounded in a place, not a spectacle.
- **Siena** costumes even its minimal footer ("©2024. SIENA FILM FOUNDATION." + COOKIE / TERMS / PRIVACY + "EMAIL US"); the gallery is the spectacle, so the footer stays a thin credits line, still in-lexicon.

Synthesis: the personality/product brand closes cinematic with a valediction fold that recontextualizes the hero; the studio closes contactable. No winner ships a plain functional footer as the only close.

### Spectacle menu

The one passage a judge replays:

- **Lando: the footer valediction.** Trigger: scrolling to the base. Beats: the split-color "ALWAYS BRINGING THE FIGHT." resolves over the helmet portrait as the signature draws in lime and the palette flips cream→dark-olive. Payoff: the emotional bookend; the bare hero face returns helmeted, ready. Replayable because it recontextualizes the opening rather than merely animating. (shipped; palette-flip mechanics verified in CSS)
- **Siena: the ticket admission.** Trigger: clicking "ENTER" on the "ADMIT ONE / 004" stub. Beats: the ticket dismisses and the film index assembles behind it. Payoff: entry becomes a ritual in-costume. (winner-verified gate + shipped transition)
- **Lusion: a project card's 3D morph.** Trigger: hover or scroll on a reel card. Beats: the discipline-tag letters split and the 3D object morphs. Payoff: the medium demonstrates itself. (observed)
- **Messenger: the delivery loop.** Trigger: piloting the tiny planet. Beats: GPU physics, lighting, and animation drive a console-game delivery run in a browser tab; multiplayer. Payoff: agency; the visitor operates the world. The whole site is the replay. (technique / shipped, via awwwards media, 80.lv, HN, webgpu.com)

Synthesis: the replay moment is a palette-inverting valediction that recontextualizes the hero (Lando), a costumed threshold ritual (Siena), or an interactive world the visitor operates (Messenger). Replayability rests on emotional recontextualization or agency, not motion polish.

### Page-level anti-signals

- **No winner opens on a card grid or a feature-bento.** The fold is a single full-bleed subject: a portrait (Lando), a costumed wordmark gate (Siena), or a live scene (Lusion, Active Theory, Messenger).
- **No hero carousel or slider, no "hero + three feature columns."** One subject, one fold.
- **No stock-photo mosaic.** Imagery is one editorial treatment page-wide or fully rendered.
- **No functional-only footer as the sole close.** The close is designed (valediction) or contactable (address block); even the thin credits line stays in-costume.
- **No visible chrome scrollbar and no boxed max-width hero container.** Full-viewport bleed; custom or transform scroll keeps `scrollHeight ≈ vh` on 3 of 5 (Siena, Lusion, Active Theory all measured at 630/630 = 1.0; Lando is the long-scroll exception at 16.5vh; Messenger is media-only).
- **No explanatory hero paragraph.** Copy is labels plus, at most, one studio manifesto line.
- **No frosted-glass nav and no nav `border-bottom`.** Nav is fixed, transparent, color-transitioning over whatever scrolls under it.
- **No long-form reading section.** Body copy never competes with the visual; there is no article body anywhere in the line.
- **No auto-playing unmuted sound without a gate.** Sound, when present, is unlocked by the costumed gate (Siena ticket, Active Theory audio toggle).

## Mid-page aliveness

What keeps the middle alive at the top of this line, where 7.2–7.4 immersive builds land their heroes and image reveals and then read dead in the sections between.

The single most important finding: **the top tier barely ships prose mid-page.** The archetype's DNA is sparse body copy. Between hero and footer the winners run interactive *indexes* (schedule tables, film cards, award rows), *scrubbed media*, and *never-idle canvas*, not walls of copy. A build whose middle is prose paragraphs is fighting the archetype. The catalog below is what fills that zone instead.

### The five live channels

**Channel A: the always-running idle layer** (the deepest register here)

- **Lando: a Rive idle layer that never freezes.** The runtime is confirmed (`riveAllLoaded` ×11, the constructor instantiated through a minified alias, `new i({src…,enableRiveAssetCDN…})`, inside `lando-by.js`) across the 17 `data-rive-artboard` mount points and 21 page-wide canvases counted under Hero architectures. Ambient audio plus a live status card layer over them. These counts drift with an actively patched build, so they are **lower bounds rather than fixed integers**.
- **Messenger: a live Three.js miniature planet** with GPU-physics courier runs; the middle *is* a running simulation. (shipped, media-only)
- This is the mid-page channel that carries the most weight in the line, and the one merely-good builds omit: **something is always moving even when the user is neither scrolling nor hovering.**

**Channel B: interactive content-row indexes with per-row hover** (the prose replacement)

- **Lando race-schedule table** (`.f1-highlight-grid`): each schedule row is a hover target: hovering floods the row with the lime accent and inverts the text to black; the schedule variant floods dark-green with lime text. The mid-page "content section" is a data table the visitor can touch, not a paragraph. (winner-verified CSS, lines 5569 and 5594)
- **Siena film index** (`.menu-film-item`): hovering a film row hides its bullet (`.dot{transform:scale(0)}`) and fades in a direct-link affordance (`opacity:1;transform:scale(1)` at `.2s ease-out`); the row's SVG arrow swaps fill. Titles are DOM-doubled for the roll swap. (winner-verified CSS)
- **Lusion award list** (`.about-award-item-container`): hovering an award row slides its text `translate3d(1.3em,0,0)` to reveal the arrow/SVG. (winner-verified CSS)
- Pattern: **the middle is a list of rows, and every row answers the cursor.** That is where the missing aliveness lives: in interactive indexes, not animated prose.

**Channel C: scrubbed media welded to scroll** (reversible decor)

- **Lando: 29 concurrent `scrub:` ScrollTrigger channels** (`scrub:!0` ×26 plus `scrub:0`, `scrub:0.5` and `scrub:1`) running parallax, camera moves, and clip reveals all scrubbed to scroll position, so driving up and down re-plays them every pass. (winner-verified)
- **Lando clip-path ellipse uncover**: images rest at `clip-path: ellipse(100% 0% at 50% 0%)`, a 0%-height ellipse, so hidden, with a `scale(1.05)` pre-zoom inside `.helmet-grid-item-reveal-img`, and the mask grows to `ellipse(100% 120% at 50% 0%)`. **Every member of the verified end-state family recurring page-wide is anchored at `50% 0` or `50% 20%`** (the five end-states are listed under Refuted). One brand shape carries the eye across every section seam.
- **Siena mouse-drag video scrubber** (`[data-videoplayer='scrub']`): `onmousemove` maps cursor x → `video.currentTime`, verbatim `(clientX-rect.left)/rect.width; this.video.currentTime=l*this.video.duration` inside `this.scrub.onmousemove`. The film still is scrubbable by hand. A second mode, `[data-videoplayer='mask']`, is also present. (winner-verified JS)
- **Lando: a pinned horizontal-track interlude** that locks the viewport and pans sideways under vertical scroll (shipped / observed: `horizontal` ×21, `xPercent` ×12 and every `pin`/`pinSpacing`/`pinType` token in the bundle resolve to GSAP ScrollTrigger's own internals rather than an isolable site-level section, so the static bundle cannot confirm it).

**Channel D: fire-once masked reveals on the sparse headings**

- **Siena `split-line-move`** (GSAP SplitText `type:"lines"`): headings and standfirsts split into lines that translate in from an `overflow:clip` box, staggered per line via `:nth-child` translate offsets. Verified counts: `linesClass:"split-line-move"` ×1 plus a `-case` variant, `type:"lines"` ×2; the CSS carries `.split-line-move:nth-child(2){transform:translate(20%)}` with a family of offsets including `-15%`, `10%`, and `0`. Cleaner than a per-char fade. (winner-verified CSS + JS)
- **Lando masked line entrance**: lines `translateY` in inside `overflow:clip` (×23 in the CSS), no fade, on `cubic-bezier(.65,.05,0,1)`, the site default declared in the inline HTML `<style>` as `--cubic-default`, paired with `--duration-default: 0.75s`. (winner-verified)
- These are content reveals: **fire once and persist** (see Re-fire behavior below).

**Channel E: section-transition seams**

- The `ellipse(… at 50% 0)` mask reused at section hand-offs (Lando) so the boundary between two sections is itself a branded reveal, not a hard cut. (winner-verified; the ellipse-mask family recurs page-wide)
- Siena routes card → case study through an overlay stack that rhymes with the intro gate. (shipped)

**Net:** five live channels fill the immersive middle, and only one of them (D) is text. The other four are idle canvas, interactive rows, scrubbed media, and shaped seams. A dead-prose middle is a symptom of building the middle out of prose at all.

### Hover on text

The tier does ship hover on non-link text, but sparingly and always as the site's one accent doing the reading, never a generic effect on every block.

- **Semantic accent recolor on a heading**: Siena `.review-slide-cont:hover` recolors the review heading and eyebrow to the site's one accent:
  ```css
  .review-slide-cont:hover .review-he,
  .review-slide-cont:hover .roll-cont-eyeb { color: red; transition: color var(--slider-dur) var(--easeOutQuint); }
  ```
  with `--slider-dur: .8s` and `--easeOutQuint: cubic-bezier(.23,1,.32,1)`: a heading answering the cursor with the brand accent. Siena's CSS ships nested; the scoped form above is what the stylesheet declares. (winner-verified)
- **Per-char rollover**: Siena splits copy with `charsClass:"split-rollover"` (SplitText `type:"chars"`), verified at `charsClass:"split-rollover"` ×3 and `type:"chars"` ×3, a per-character hover play kept distinct from its line-reveal split. (winner-verified JS)
- **Content-row text inversion**: Lando schedule rows flip text color as the row floods (`.f1-highlight-grid:hover{ color: var(--color--black) }` under the lime flood; the schedule variant goes to lime text). The text recolors because the row it sits in became active. (winner-verified)
- **Sibling-dim on a menu group**: Siena uses `:has()` so hovering one menu link dims the *others* to 70%: `[data-hover=mainlinkgroup]:has([data-hover=mainlink]:hover) [data-hover=mainlink]{opacity:70%}`, with `transition:opacity .2s`. Hovering text changes the unhovered text. (winner-verified)
- **Prose-link underline draw**: Lusion draws link underlines in prose via a `::after` `transform: scaleX(0→1)`: `#project-details-desc a:hover:after, #project-details-side-list a:hover:after{ transform: scaleX(1) }`. Its description prose is split for animation via `this.domDescription._splitText()` (×23 in the bundle, with `domDescription._splitted.revert()`), gated `if(properties.viewportWidth>=812)` against `MOBILE_WIDTH=812`, desktop only. (winner-verified)

**What the tier does not ship on text:** a scroll-linked emphasis-fill on prose, the dim→bright, per-word accent sweep that carries a wall of editorial copy. That mechanic is an editorial/minimalist signature; the immersive winners do not run it because they have almost no prose to run it on. The hero variable-font move (Lando `.text-nav-link`, under Text effects) is the one bespoke type effect, and it is a hero move, not a mid-page one. A build that needs prose alive in this archetype gets the two hover forms above (accent recolor plus per-char rollover) and a fire-once line reveal on entry, not a scrubbed emphasis fill.

### Re-fire behavior

Two independent bundles behave the same way, and the exceptions sharpen the rule rather than break it.

- **Fire-once content**: both Lando and Siena configure content reveals with GSAP `toggleActions: "play"`. Lando declares it as a shared default config object, `R6={toggleActions:"play"}`; Siena carries `toggleActions:"play"` ×1 as the only value in its bundle, with `onEnter` ×15 exactly. `"play"` means play on enter, and the omitted `onLeave`/`onEnterBack`/`onLeaveBack` slots mean no reverse: the reveal fires once on the first pass and persists. Driving back up does not un-reveal the copy or the images. (winner-verified JS, both sites; Siena's bundle does contain `onLeave`/`onLeaveBack`/`reverse` tokens elsewhere, in timeline and decor code, so the no-reverse finding is scoped to content-reveal `toggleActions`.)
- **Reversible decor**: Lando's 29 `scrub:` channels (Channel C) plus `IntersectionObserver` ×4 re-play on every pass, forward and back, because they are scrubbed to the scrollbar rather than triggered. Siena's `[data-videoplayer='scrub']` is the hand-driven version of the same principle.
- **The decor exception proves the rule.** Lando ships exactly 2 `toggleActions:"play none none reverse"` triggers, and both sit on WebGL decor: `uCursorIntensity` and a wireframe `uOpacity` driven through `[data-gl-track="head"]`. Reversal is reserved for shader uniforms, never for copy or gallery images.
- On a repeated up/down drive: headings and gallery images stay revealed, while the parallax, the ellipse masks, the pinned horizontal pan, and the video scrub all move continuously with the scroll. **Content persists; decor reverses.**

The Lenis and lerp inertia below is what makes the scrub channels read as continuous camera motion rather than jitter; re-fire decor and smooth scroll are one system.

### Smooth scroll

All three deep-read sites smooth the wheel; smoothing is near-universal at this tier and the library tracks the stack.

- **Lando Norris: Lenis.** 75 case-insensitive `lenis` hits in the bundle, with the full class family `.lenis`, `lenis-locked`, `lenis-prevent`, `lenis-scrolling`, `lenis-smooth`, `lenis-stopped`. Webflow + GSAP stack. (winner-verified)
- **Siena Film Foundation: Lenis.** The constructor is bundled verbatim: `smoothWheel:i=!0,syncTouch:r=!1,syncTouchLerp:n=.075,touchInertiaMultiplier:o=35,easing:u=…,lerp:c=.1`, with `html.lenis` / `lenis-smooth` / `lenis-stopped` classes in CSS. The `.075` and `35` are the Lenis library's **destructuring defaults in the constructor signature**, not Siena's passed config; they confirm the library, not the tuning. (winner-verified)
- **Lusion v3: custom lerp-based smooth scroll, not Lenis.** `lerp(` ×38 exactly, `scrollManager` ×121 (plus `ScrollManager` ×2), `addEventListener("wheel")` ×5, `requestAnimationFrame` ×3, and `new Lenis` / `locomotive` = 0. The hardcore WebGL studio rolls its own so the scroll value can drive the scene directly. (winner-verified)

Read: **Webflow/GSAP immersive builds reach for Lenis; bespoke-WebGL studios write their own lerp.** Either way the wheel is smoothed; an un-smoothed wheel is itself an anti-signal in this line, because every scrubbed decor channel depends on a continuous scroll value.

Lusion's renderer is WebGL with an OGL-shaped API surface; the counts and the failed `ogl` citation are under Refuted.

### Mid-page anti-signals

- **No walls of prose.** The middle is indexes, scenes, and scrubbed media. A prose section that reads dead is usually a section that should not be prose.
- **No scroll-linked emphasis-fill on copy.** Absent across all three deep reads, an editorial move; here there is no copy to carry.
- **Almost no CSS transitions.** Each of Lando's two near-duplicate CSS files declares exactly one `transition-property:color` and one `transition-property:height` (2 unique rules, 4 declarations across both files, in ~366KB) alongside just 3 `transition:` shorthands (`transition:unset`, a `background-color/color .1s`, and an `all .3s`). The `.f1-highlight-grid` base rule carries **no** transition at all: the lime flood is instant, driven by JS. Mid-page motion is GSAP/Rive/lerp-driven; the CSS holds resting and target states and JS interpolates. A build that leans on CSS `:hover transition` for its aliveness is a tell.
- **No frozen middle.** The idle layer (Rive, canvas, WebGL) never stops; a section that goes static between inputs breaks the fiction.
- **No reversing content reveals.** `toggleActions:"play"` on copy and gallery images; the only `"play none none reverse"` triggers are on shader uniforms.
- The element-level anti-signals under Effect palette hold mid-page too, confirmed by grep on both live bundles.

## Refuted

- **"Messenger — Awwwards Developer Site of the Year 2025 at `messenger.network`"** is half false: the title is real (Annual Awards winners page), but the entry is **SOTD 10 Nov 2025 + Developer Award 8.21** at `messenger.abeto.co`; `messenger.network` 301-redirects to `genzee.io`.
- **"Lando's first fold is a 3D helmet on cream"** is false: the fold is a full-bleed frontal portrait photograph with the helmet as a ghosted contour-line silhouette behind the face (Hero architectures), plus a later "Helmets" gallery and the footer portrait; `<body>` computes `#282C20` / `#F4F4ED`, so the page is predominantly dark and the cream register is hero-and-footer only.
- **"Lusion reel names Oryzo / Space-NFTMarketplace / DD2024 / ChoChoWorld"** is false: decoding the quadrupled DOM `textContent` gives **OryzoAI**, **Spaace-NFTMarketplace**, **DDD2024** and **ChooChooWorld** (Page recipe, Shape C). The other six reel names hold.
- **"Lusion footer address: Suite 29 Marsh Street"** is false, a line-fusion misread; the DOM leaf-node chain (Copy voice) gives **"Suite 2, 9 Marsh Street, Bristol, BS1 4AA, United Kingdom"**.
- **"Lando's preloader unmounts — no `[class*=load/preload/intro]` node survives"** is false as a blanket negative: `[class*="intro"]` still matches surviving content nodes (Loader and intro); the negative narrows to load / preload / curtain.
- **"Lusion / Messenger / Active Theory render on dark canvases"** is false for **Lusion**, whose body computes `rgb(255,255,255)` (Imagery art direction); the dark-canvas grade holds for Active Theory and Messenger only.
- **"Lando's ellipse family includes `110% 110% at 50% 0%` and an `… at 50% 100%` end-state"** is false: both grep to **0 hits**. The verified family is `100% 0% at 50% 0`, `100% 120% at 50% 0`, `120% 100% at 50% 20%`, `120% 120% at 50% 0`, `70% 100% at 50% 0`, every member anchored at `50% 0` or `50% 20%`. The mechanic holds; the enumerated end-states were partly wrong.
- **"Lando ships 44 `data-rive` canvases and instantiates `new Rive` ×8+"** is false: the live build carries **17** `data-rive-artboard` mount points (3 literal `<canvas data-rive>`, 5 unique `.riv` files), and the only literal `new Rive` sits inside the Rive library's own deprecation-warning string; the site instantiates through a minified alias. `riveAllLoaded` ×11 confirms the runtime; the counts drift with an actively patched build and should be cited as ≥N ranges.
- **"`toggleActions:"play"`, never `"play reverse"`"** is false as an absolute: Lando ships 2 × `toggleActions:"play none none reverse"`, both on WebGL decor (Re-fire behavior). The rule holds for content reveals, and the exception reinforces "content persists, decor reverses".
- **"Lusion runs WebGL via OGL — 2 refs in the HTML"** is false as cited: both hits are the substring `ogl` inside *Google* and *googletagmanager*, and genuine `ogl`/`oframe` tokens are zero (the `oFrame` ×7 are substrings of `requestVideoFrameCallback`). WebGL stands (`WebGLRenderingContext` ×3, `createProgram`); the OGL identity rests on the API surface (`Mesh` ×49, `Texture` ×39, `Program` ×2, `RenderTarget` ×2) and the studio's known stack, not on the cited proof.
- **"Siena's Lenis is configured `syncTouchLerp:.075`, `touchInertiaMultiplier:35`"** is unsupported: those values are the Lenis constructor's destructuring defaults (Smooth scroll), not proof of Siena's passed config; Lenis identity stands via the constructor and the `html.lenis` class family.
- **"Siena — Awwwards Site of the Month April 2025"** is false: **March 2025** ([`editorial.md`](./editorial.md#refuted)).

## Could not verify

- **Lando's pinned horizontal-track interlude** `(shipped)`: `horizontal` ×21 and `xPercent` ×12 in the bundle resolve to GSAP ScrollTrigger internals (Channel C); confirming it requires driving the live site.
- **Three committable Lando copy strings**, flagged, not cut: the hero status card ("NEXT RACE / SPA GP / MCLAREN F1 SINCE 2019"), the footer sponsor names (Quadrant, Bell Helmets, Tumi, Pure Electric, Android, PAP, Monster Energy, L7), and the footer nav-column labels (PAGES, FOLLOW ON).
