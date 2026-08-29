---
title: "Depo Luxe — Live CSS and JS Read"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "corporate-luxury", "live-read", "css", "gsap", "webgl", "custom-cursor", "clip-path", "eleventy", "splittext"]
sources:
  - "https://www.awwwards.com/sites/depo-luxe"
  - "https://depoluxe.xyz"
---

# Depo Luxe — Live CSS and JS Read

Depo Luxe ships no filled CTA button anywhere in its chrome (the site's single fill-and-invert hover rule sits quarantined inside the cookie consent manager) and runs a full-screen Three.js shader plane over a monochrome DOM set in one typeface. Source-level read of the CSS and JS behind `depoluxe.xyz`, for the cinematic end of the [corporate-luxury archetype](../archetypes/corporate-luxury.md). Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

## Awards and stack

Awwwards [Site of the Day, 7 Jul 2026](https://www.awwwards.com/sites/depo-luxe), overall **7.62** (Design 7.81 / Usability 7.16 / Creativity 7.8 / Content 7.84), Developer Award **7.53** (Animations/Transitions 8.40, WPO 7.80, Responsive 7.60, Markup 7.40, Semantics/SEO 7.00, Accessibility 6.80), credited to Cuchillo; the page records a two-color `#fff` / `#000` palette and tags Film & TV, Luxury, Animation, Clean, Navigation Menu, Photo & Video, Microinteractions, 11ty. The Developer Award is consistent with the heavy WebGL.

**Stack (verified):** 11ty static · GSAP + ScrollTrigger · GSAP **SplitText** · **Three.js/WebGL** full-screen shader plane (OrthographicCamera + PlaneGeometry, 46 fragment/vertex shaders, 16 ShaderMaterial, 44 WebGLRenderer, 32 `gl_FragColor`) · Cuchillo's own framework for custom smooth-scroll and cursor. Project videos are Vimeo-hosted 1080p MP4 loops.

Evidence tags: `[CSS]` / `[JS]` / `[HTML]` = read from the site's own source, fetched 9 Jul 2026; **observed** = runtime-only, collected under Could not verify.

## 1. Hover / micro-interactions

- **Text links, the site's primary CTA pattern** `[CSS]`: `.link-underline`, a `:before` underline (`background:currentColor; height:.5px; bottom:.8em; width:100%`) whose **opacity fades 0→1** on hover, `transition:.1s`/`.2s`. The underline draws in via opacity, with no fill and no color inversion. Body links (`.body a`, `.widget-bio a`) invert the logic (`--opacity-hover:0`, `--opacity-hide:1`): underline shown at rest, **fading out** on hover. `[aria-current=page]`/`.--active` lock the underline on.
- **Buttons that fill or invert** `[CSS]`: **only the cookie banner.** The site has **no traditional filled CTA buttons.** The single fill/invert rule is `#CMP .btn` in the consent manager: rest = transparent bg + border + `backdrop-filter:blur(40px)`; hover **inverts**, `:not(.--full):hover{background-color:var(--color);color:var(--bg)}` and `.--full:hover{background-color:var(--bg);color:var(--color)}`, `transition:background-color .3s ease-out`. The invert-on-hover instinct exists, quarantined to the cookie UI and kept out of the site chrome.
- **Selected works, the signature content hover** `[CSS]`: hovering one work sets `--opacity-figure:.3` to dim that thumbnail, and `.--hover .block-selected-works{--opacity:.2}` **dims all sibling items to 20%** for a spotlight. Metadata swaps: `.client` + `.counter` fade out (opacity→0, `.4s var(--ease-out-quad)`) while `.title` fades in (`opacity .4s var(--ease-in-quad)`) and `.client2`/`.director` fade in (`.2s var(--ease-in-quad) .05s`). At rest a row reads client plus roman counter; on hover it reads the film title plus director.
- **Nav bar surface** `[CSS]`: `#Header`: `position:fixed`, `z-index:5`, `transform:translateZ(5px)` (it sits inside a 3D perspective scene), `pointer-events:none`. A **separate blur layer `#Header__blur`** carries `backdrop-filter:blur(40px)` and a background that is a **5%-opacity tint** flipping with the section palette, `rgba(0,0,0,.05)` on dark sections and `rgba(255,255,255,.05)` on light, `transition:background-color .2s ease-out`. **No border-bottom on the nav**; border-bottom appears only on `abbr` and the video progress track. The centered logo (`#Header .logo-depo`) is an SVG-masked **frosted box**: `backdrop-filter:blur(1rem)`, `background:#ffffff1a`, mask `/assets/svg/depo-luxe-box.svg`.

## 2. Motion & scroll

- **Custom smooth scroll** `[JS]`: the Cuchillo `Scroll` class, wheel-driven (`wheel` ×56), lerp-interpolated (`cr.lerp(p0,-p1,t)`; `lerp(t,e,i)=t*(1-i)+e*i`), default `goto(t,e=2,…)`. Neither Lenis nor Locomotive.
- **Scroll displacement and parallax** `[CSS + HTML]`: `[data-scroll-displace]` on **16 elements**; the container is `overflow:hidden` and the inner `div`/`img` is transformed from `center center`, JS-driven. A sibling `[data-scroll-scale]` handles scroll scale.
- **Clip-path mask reveal, the signature** `[CSS]`: `[data-has-mask] [data-mask-child]` animates a `clip-path:polygon(...)` from four CSS vars (`--mask-inside-top/right/bottom/left`) plus an `--inside-x/y` offset, giving an inset wipe for images and media on enter.
- **Line reveal** `[CSS]`: `.line-parent{overflow:hidden}` with SplitText lines translating up under the clip.
- **Background video reacts to scroll** `[CSS]`: `#BGVideo` is fixed full-screen at `opacity:.5`, driven by `--grayscale`, `--blur`, `--scale` (`scale3d`) vars that JS animates for desaturate, blur, and scale. The `.visor-videos` viewport has `--overlay:.24`.
- **Durations and easings** `[CSS]`: dominant `.2s` (14×), then `.1s`, `.4s`; longest `.5s`. Reveals use `--ease-out-quad` (`cubic-bezier(.25,.46,.45,.94)`); fades use `--ease-in-quad` (`cubic-bezier(.55,.085,.68,.53)`).

## 3. Text effects

- **Hero headline** `[CSS + HTML]`: `<h1 class="claim __claim">` reads "A strategic and cinematic approach to contemporary luxury", rendered **italic serif** (`font-style:italic`, EB Garamond italic), inside the fixed `#Header` holder (`translateY(var(--y))` for scroll drift).
- **Split reveals** `[JS]`: GSAP **SplitText** (it guards `"SplitText called before fonts loaded"`), feeding the `.line-parent` overflow-clip line reveals. Char and word granularity exist in the split system; per-line is the confirmed on-screen unit.
- **Roman numeral counters** `[CSS]`: content is indexed via CSS `counter(roman-counter, upper-roman)` (`.block-text .counter:after`), reinforcing the editorial film-credit tone.

## 4. Cursor & pointer

- **Custom Cuchillo cursor** `[JS]`: adds the body class `__cursor`; the element is `position:fixed; z-index:10000; opacity:0.9`. Attribute-driven modes: `data-cursor-magnetic`, `data-cursor-drag` (+`data-cursor-axis` x/y), `data-cursor-follow`, `data-cursor-follow-fixed`, `data-cursor-image`, `data-cursor-icon`, `data-cursor-text`, `data-cursor-color`, `data-cursor-rotation`. The cursor is magnetic, draggable, and can carry a text label, icon, or image. Disabled on touch (`xr.isTouch`). Which specific elements opt in is **observed** only: the data-cursor attributes are applied at runtime, not in the static HTML.
- **Native cursor hidden in video takeover** `[CSS]`: `.plaver-video-full, .plaver-video-full *{cursor:none}` and `.__cursor-default-hide *{cursor:none}`.

## 5. Loaders / intros

**Video preloader plus SVG logo** `[CSS + JS]`: `#Preloader`: white bg, black text, full-screen, `z-index:14`, `text-transform:uppercase`, serif. It contains an SVG logo (`--size-logo:10rem` desktop / `5.625rem` mobile) whose `path{opacity:0}` reveal in as loading progresses, plus a `<video class="video-preloader">`. The JS asset loader `Pr` tracks `progress` 0→1 (`itemsTotal`/`itemsLoaded`/`onComplete`), gating `.show()` on the video `play()` resolving. **No numeric percent counter element was found**; progress reads out through the logo path reveal rather than a counting number. A genuine gated intro, not an instant paint.

## 6. Notable signature interactions

1. **WebGL video/image transition layer** `[JS]`: a body-level full-screen `<canvas>` running the Three.js shader plane over the monochrome DOM. The animations-8.4 and Developer Award centerpiece.
2. **Fullscreen video-navigation takeover** `[CSS]`: `.plaver-video-full`: `background:#000`, `100vh`, giant scrubbing timer (`--font-size-timer:20.5vw`), `cursor:none`, dashed progress track (`border-top/bottom:1px dashed`), controls at `60px`/`120px` widths, a cinematic full-bleed player mode for selected works.
3. **Section palette inversion** `[CSS]`: `palette-primary`↔`palette-secondary` flip the entire black/white scheme, and the nav's 5% blur tint with it, as you scroll between sections.

## Exact tokens

- **Colors** `[CSS]`, from `:root`: `--white:#fff` `--black:#000` `--grey:#999`; accents defined but reserved: `--blue`/`--yellow` both `#0000fe`, `--red:#ff4f23`, `--assertive`/`--focus:#f0f`. `--primary:var(--black)` `--secondary:var(--white)`; sections carry `palette-primary`/`palette-secondary` classes that swap `--bg`/`--color` for a scroll-driven black↔white inversion. Nav tint `rgba(0,0,0,.05)` / `rgba(255,255,255,.05)`; logo box `#ffffff1a`.
- **Type** `[CSS]`: one typeface only, **EB Garamond serif, regular and italic**, at every size including display; `letter-spacing:-.01em`, `line-height:1.375`; hero H1 italic; timer `--font-size-timer:20.5vw`.
- **Motion** `[CSS + JS]`: a full cubic-bezier easing palette is declared, `--ease-out-quad` (`cubic-bezier(.25,.46,.45,.94)`) through `--ease-in-quad` (`cubic-bezier(.55,.085,.68,.53)`) to `--ease-in-out-expo`; durations `.1s` / `.2s` (dominant) / `.4s` / `.5s`; Cuchillo `Scroll` lerp `lerp(t,e,i)=t*(1-i)+e*i`, `goto(t,e=2,…)`.

## Could not verify

- Which elements opt into the custom cursor: the `data-cursor-*` attributes are applied at runtime, not in the static HTML (**observed**).
- The per-scroll displace magnitudes on the 16 `[data-scroll-displace]` elements: JS-driven (**observed**).
- No JS was executed, so corroboration beyond the source reaches only the static structure and the Awwwards metadata above.
