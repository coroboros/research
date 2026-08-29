---
title: "Son Daven — Live CSS and JS Read"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "corporate-luxury", "live-read", "css", "gsap", "webgl", "webflow", "lenis", "preloader", "magnetic-pull"]
sources:
  - "https://www.awwwards.com/sites/son-daven"
  - "https://www.awwwards.com/websites/sites_of_the_month/"
  - "https://sondaven.com/en"
  - "https://assets.slater.app/slater/18883/55210.js"
---

# Son Daven — Live CSS and JS Read

Five global CustomEase curves and three duration constants are the engine behind Son Daven's motion, and the signature interaction is a knob dragged along a curved SVG path that swaps the whole resort between summer and winter. Source-level read of the CSS and the unminified custom bundle behind `sondaven.com/en`, for the [corporate-luxury archetype](../archetypes/corporate-luxury.md). Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

## Awards and stack

Awwwards [Site of the Day, 5 Jun 2026](https://www.awwwards.com/sites/son-daven), overall **7.62** (Design 7.7 / Usability 7.16 / Creativity 8.15 / Content 7.59), Developer Award **8.09** (Responsive 8.40, Animations/Transitions 8.20), credited to The First The Last; [Site of the Month, Jun 2026](https://www.awwwards.com/websites/sites_of_the_month/) on the monthly listing.

**Stack (verified, from HTML):** Webflow + GSAP 3.13 (ScrollTrigger, CustomEase, SplitText) + GSAP 3.14.1 Flip + Lenis smooth scroll + Swiper 11 + Barba.js page transitions. The Lenis patch version is contested: **1.3.15** sits on every script `src` in the 390 KB raw HTML here, while [`../archetypes/corporate-luxury.md`](../archetypes/corporate-luxury.md) finds the string in neither the Slater module nor the page HTML; the Lenis config below is exact either way. Custom code hosted on Slater (`assets.slater.app/slater/18883/55210.js`, 81KB, unminified), fetched 9 Jul 2026. Console credits: designed and developed by **Ivan Chopei**, agency **THEFIRSTTHELAST**.

Evidence tags: `[CSS]` / `[JS]` = read from the shipped stylesheet and the Slater bundle, `[JS, initX]` naming the function; **observed** = structure present, driving code not found.

**The engine** `[JS]`. Five global CustomEase curves drive everything; `Out` is the workhorse behind most reveals and hovers.

| Curve | Value | Where it is named below |
|---|---|---|
| `Out` | `cubic-bezier(0.25, 1, 0.5, 1)` | nav scramble, menu dim, reveals, headline scatter, preloader video |
| `InOut` | `cubic-bezier(0.76, 0, 0.24, 1)` | logo Flip into the header (§5) |
| `In` | `cubic-bezier(0.5, 0, 0.75, 0)` | not named in the read sections |
| `Ease` | `cubic-bezier(0.25, 0.1, 0.25, 1)` | season-knob snap (§6) |
| `Write` | `cubic-bezier(0.333, 0, 0.667, 1)` | highlight text (§3, inferred) |

Duration constants: `durL = 1.2s`, `durM = 0.8s`, `durS = 0.4s`. Reveal base `delayReveal = 0.2s`, `stagger = 0.1`, desktop breakpoint `992px`; most hover and magnetic effects are disabled at ≤991px.

## 1. Hover / micro-interactions

**Nav items: per-character random scramble** `[JS, initNavItemHover]`. Two stacked text copies, both SplitText'd into chars. On enter, the visible chars fly out (`opacity 1→0, yPercent 0→-75, scale 1→0`) while the duplicate flies in (`yPercent 75→0, scale 0→1, opacity 0→1`), both `duration: durM (0.8s)`, `ease: "Out"`, `stagger: { each: 0.025s, from: "random" }`. The random-order char stagger is the nav tell: letters scatter and pop rather than rolling cleanly.

**Menu list (fullscreen): focus-dim** `[JS, initMenuItemHover]`. Hovering one item drops every other to `opacity: 0.2` (`durM`, `Out`); the hovered item stays at 1. Leave restores all to 1 (`durS`).

**Pill CTA `.btn` (e.g. "Consultation"): full-solid fill, not a tint** `[CSS]`. Layered DOM: `.btn_bg` pill = `background-color: base-1000--100`, a **full solid** brand token, `#2c2824` on light sections and `#a89474` on dark, **never a pale or washed tint**. `border-radius` is a full pill, extended `-4px` left and right past the label. `.btn_hover` is a 2px solid outline in `base-0--100`, the section background color. A duplicated label `.btn_label_text.is-2` (absolute, top-left) is staged for a vertical roll-swap. **The hover animation itself is observed structure with no driving code found**: no CSS `:hover` transition exists for buttons, no Webflow IX2 data is present (`data-w-id`/`w-json`/`ix2` all absent), and no JS handler binds the `hover-btn` attribute. The roll scaffolding exists; what plays is unverified. The fill token and geometry are certain.

**Circular "Invest in Son Daven" CTA: magnetic** `[JS]`. Carries `data-magnetic-strength` and is pulled toward the cursor (see §4).

**Text links** `[CSS]`: `.text-link:hover { text-decoration: none }` removes the underline on hover. The expressive link treatment is the nav char-scramble; body links stay minimal.

**Nav bar surface** `[JS + CSS]`. `.header` is `position: fixed; z-index: 889` with a separate `.header_bg` layer whose `background-color: base-0--100`. That background is **held at `opacity: 0` until you scroll past 1000px**, then fades to 1 (`durS`, `Out`). Its surface color is the current section's own background, `#a89474` (tan) over light sections and `#2c2824` (dark brown) over dark ones, because the theme system reassigns the token as you scroll. **No border-bottom of any color. No `backdrop-filter` blur.** The header also hides on scroll-down (`yPercent: -100`, `durM`) and reappears on scroll-up (`yPercent: 0`), ignoring sub-40px jitter and force-showing within 160px of the footer.

## 2. Motion & scroll

- **Smooth scroll** `[JS]`: Lenis, `duration: 1.2`, `easing: 1.001 - 2^(-10·t)` (exponential-out), `smoothWheel`, `touchMultiplier: 2`; nested `[data-lenis-scroll]` panels get their own `duration: 0.6` instance. The GSAP ticker drives Lenis; `lagSmoothing(0)`.
- **Scroll reveals** `[JS, initScrollElementsReveal]`: 135 `[data-scroll-reveal]` elements, each `ScrollTrigger start: "top bottom"`, `once: true`, a single fire on entry from the viewport bottom. Cards get `transformPerspective: 1000` for a 3D-tilt reveal.
- **Parallax** `[JS, initAllParallax]`, all `ease: "none"`, `scrub`: images `yPercent -20→20`; "img-out" `-10→30`; containers `±10`; and **H1 horizontal drift**, child words `xPercent: [5,-1,-5] → [-5,1,5]` (`scrub: 1`), so display headlines shear sideways at different rates while scrolling.
- **Frame-by-frame scroll video** `[JS, initScrollVideo]`: a `<canvas>` scrubbed through a preloaded image-frame array, `snap: "frame"`, `ease: "none"`, `scrub: 0.25`, `start: "top top" → end: "75% bottom"`, desktop only.
- **Marquee** `[JS, initMarquee]`: infinite `xPercent: -100` over `24s` linear, **scroll-velocity-reactive**: `timeScale(1 + 0.01·velocity)` speeds up and reverses with scroll; pauses off-screen.
- Also present `[JS, function names]`: `initSnapSections`, `initSectionTransition`, `initPlayPauseVideoScroll`, Flip-based tab and gallery morphs.

## 3. Text effects

- **Headlines: scatter-in** `[JS, animateTextH]`: SplitText into **words**; each word starts `scale: 0, opacity: 0` at alternating `yPercent: wrap([-150, 75, -75, 150])`, some dropping from above and some rising from below at varied distances, animating to rest over `durL (1.2s)`, `ease: "Out"`, `stagger: { each: 0.025s, from: "random" }`. Words assemble out of scattered scaled-to-zero fragments in random order. The headline signature.
- **Paragraphs: line rise** `[JS, animateTextP]`: SplitText into **lines**, `yPercent: 250 → 0`, `opacity 0→1`, `durL`, `stagger 0.05`, `Out`.
- **Divider lines: clip wipe** `[JS, animateLine]`: `clip-path: inset(0% 100% -1px 0%) → inset(0% 0% -1px 0%)` left to right, `durL`, `Out`.
- **Highlight text** `[JS, function name initHighlightText]` and the `Write` ease imply a scrubbed word-by-word highlight or write-on on a pinned block (inferred).

## 4. Cursor & pointer

**No custom cursor element** `[JS]`: no cursor DOM node and no follower function exists. The pointer stays native, with two intentional overrides: Swiper sliders use `grabCursor` (grab → grabbing on drag), and the season knob sets `cursor: grab/grabbing`. Magnetic pull replaces a cursor gimmick: `[data-magnetic-strength]` elements (default strength 25) translate toward the cursor by `((x−cx)/w − 0.5)·(strength/16)` em on `mousemove` (`ease: "power4.out"`, `duration: 1.6`; inner targets `duration: 2`), and spring back on leave with **`ease: "elastic.out(1, 0.3)"`, `duration: 1.6`**. The springy overshoot release is the magnetic tell.

## 5. Loaders / intros

**Full preloader with a live counter** `[JS, initPreloader]`. First visit (`sessionStorage.hasVisited` unset) runs `animatePreloaederIntro` *(sic)*; returning visitors get a short version. The intro:

- `[data-preloader-percent]` counts **`0% → 100%`** via `Math.round(loaded/total·100)+"%"`, tied to real asset progress: `Promise.all([framesPromise, globalSceneManager.ready(), document.fonts.ready])`, covering WebGL scenes, scroll-video frames, and fonts.
- An intro video (`data-intro="video"`, `preloader_sheep.mp4`, Hutsul shepherd sheep, blended `mix-blend-mode: lighten`) scales `1.5 → 1` over `2·durL (2.4s)`, `ease: "Out"`.
- The logo does a **Flip** from its preloader position into the header slot, `duration: 1.5·durL (1.8s)`, `ease: "InOut"`.
- Scroll is locked until the timeline finishes, then `initPageTransitions()` (Barba) + `unlockScroll()`. Page-to-page navigation animates via `animateTransition` plus a `.transition` overlay.

## 6. Notable signature interactions

**The draggable summer↔winter season slider** `[JS, initSummerWinterSwitcher]`. A knob (`[data-active]` SVG circle) is dragged along a **curved SVG path**; its position maps to progress `0–1` via nearest-point sampling of `getPointAtLength`. Crossing `<0.4` fires `[data-summer-btn].click()`, `>0.5` fires `[data-winter-btn].click()`, swapping the resort's entire imagery and content between seasons. Release snaps to `0` or `1` (`gsap.to progress`, `durM`, `ease: "Ease"`), cursor toggles `grab → grabbing`. It lets you drag the Carpathians from summer to winter.

**Runner-up signature: the dot-grid WebGL shader** `[JS, raw WebGL fragment shader]`. Hand-written WebGL with no Three, OGL, or Pixi: `createProgram`, single-triangle, `precision mediump float`. It renders scene textures as a **grid of variable-width marks and dots**: samples each texture on `u_gridSize` cells, thresholds luminance (`u_gamma`, `u_blackPoint`, `u_whitePoint`, `u_threshold`), and draws marks from `u_minWidth`→`u_maxWidth` in `u_fillColor` over `u_bgColor`, discarding edge cells. Photographic renders resolve through an embroidery-like dot matrix, the connective motif across `initSceneSeasons`, `initSceneHeroBg`, `initSceneProlog`, `initSceneFin` and the preloader, progress-tracked by a `globalSceneManager`.

## Exact tokens

**Colors** `[CSS]`, a **two-tone palette that inverts per section**, with no third accent:

- `#2c2824`: dark warm brown, near-black
- `#a89474`: muted Carpathian gold/tan
- **Light sections** (`:root` / `.theme_on-light`): background `#a89474`, text and links `#2c2824`. **Dark sections** (`.theme_on-dark`): background `#2c2824`, text `#a89474`. Swapped live on scroll by `initThemeChange`: ScrollTrigger toggles `theme_on-dark`/`theme_on-light` at each `[bg]` section's midpoint.
- White scale: `#ffffff` (`white--100`), `#fff9` (60%), `#fff3` (20%), `#0000` (transparent).
- System states: success `#1ba64b`, alert `#ffa800`, error `#e23d3d`.
- **Permanent film-grain overlay** `.noise`: fixed full-screen AVIF noise, `opacity: 0.1`, `mix-blend-mode: soft-light`, `background-size: 10%`, `z-index: 2147483647`. `.blend-diff` uses `mix-blend-mode: difference` for text over image.

**Fonts** `[CSS]`, Kyiv Type Foundry, a Ukrainian foundry matching the Hutsul theme:

- Display: `"KTF Metro Roman"` (serif fallback `"Times New Roman"`): H1 `144rem/14.4` responsive, `line-height: 83.3%`, `letter-spacing: -0.064em`, very tight negative tracking on all headings.
- Body: `"KTF Metro Blueline"` (fallback Arial): paragraphs carry positive `letter-spacing: 0.08em`; small labels (p6, 10px) are `text-transform: uppercase`.
- Fluid type via `--scale-ratio` (14.4 desktop / 3.84 mobile), `body { font-size: 1vw }`.

## Could not verify

- **Pill `.btn` hover animation**: the structure is certain (full-solid theme-inverting pill plus a duplicate label staged for a roll), but no CSS, IX2, or JS was found driving it. What plays on hover is unverified.
- **No live render.** A static fetch returned only the JS-unrendered shell of the Barba SPA, so every behavior above is sourced from the CSS and the readable Slater bundle. Exact per-scene shader parameter values (`u_gridSize` and siblings) are set at runtime and are not statically recoverable.
- **Lenis patch version.** 1.3.15 on the script `src` here, not found in the Slater module by [`../archetypes/corporate-luxury.md`](../archetypes/corporate-luxury.md); both readings stand.
