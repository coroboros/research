---
title: "Brunello Cucinelli — Live CSS and JS Read"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "corporate-luxury", "live-read", "css", "gsap", "backdrop-filter", "custom-cursor", "lenis", "ai-interface"]
sources:
  - "https://www.awwwards.com/sites/brunello-cucinelli-ai-e-com"
  - "https://shop.brunellocucinelli.com/en-gb/ai"
  - "https://brunellocucinelli.ai"
  - "https://www.makemepulse.com/case-study/brunello-cucinelli-ai-shopping-experience"
  - "https://www.makemepulse.com/news/makemepulse-reimagines-a-e-commerce-platform-with-callimacus-technology"
---

# Brunello Cucinelli — Live CSS and JS Read

Line-draw rather than fill is the luxury signature of the sibling build read here: the CTA never takes a color on hover; it draws a stroke SVG ring and rotates it, over a frosted-glass menu system and a warm off-white ground. Source-level read of the CSS and JS behind the makemepulse-built Brunello Cucinelli AI experience, for the [corporate-luxury archetype](../archetypes/corporate-luxury.md). The awarded shop page is bot-blocked, so every value comes from the sibling `brunellocucinelli.ai` build by the same studio. Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

## Awards and stack

Awwwards [Site of the Day, 9 Jul 2026](https://www.awwwards.com/sites/brunello-cucinelli-ai-e-com), overall **7.19** (Design 7.27 / Usability 7.02 / Creativity 7.2 / Content 7.33), Developer Award **7.01**, credited to makemepulse; tags E-Commerce, Fashion, Luxury, Clean, Unusual Navigation, Interaction Design, HTML5. Studio material: the [makemepulse case study](https://www.makemepulse.com/case-study/brunello-cucinelli-ai-shopping-experience) and the [Callimacus news post](https://www.makemepulse.com/news/makemepulse-reimagines-a-e-commerce-platform-with-callimacus-technology).

**The awarded page is bot-blocked.** The Site of the Day (SOTD) page itself, **`shop.brunellocucinelli.com/en-gb/ai`**, sits behind **Akamai bot manager** and returns **HTTP 403 "Access Denied" (edgesuite.net)** to fetches under any user agent and to automation-controlled Chrome, which it fingerprints through `navigator.webdriver`. **That page's own CSS and JS could not be extracted.**

Every `[CSS]` value below comes from the **sibling makemepulse-built experience `brunellocucinelli.ai`** ("the AI-powered website of Brunello Cucinelli… explore the life of Brunello, the philosophy"), which shares the same studio, the same **Solomei AI / Callimacus** integration (`art.solomei.ai/webxp-integration.min.js`), and the same design-system tokens, fonts, and frosted-glass language. It carries the same `.product-card-*`, `.c-prompt-*` (AI prompt bar) and `.ep-banner-*` (WebGL hero) surfaces. The shop e-com very likely shares this system, **but its exact hexes and durations cannot be proven identical.** Concept-level AI behavior comes from the makemepulse case study (**observed**).

Stack of the sibling build `[JS]`, from `index-RpG0soLF.js`, fetched 9 Jul 2026: **React SPA** on Vite, **GSAP 58 refs + ScrollTrigger 24** for scroll animation, **Lenis 39** for smooth scroll, **Fancybox v5 46** for image lightbox and zoom, **IntersectionObserver** for reveals, one `THREE` ref. `art.solomei.ai/webxp-integration.min.js` loads the AI "webxp" layer.

**Two sizes are on record for that one file.** The bundle measures **510 KB** here; [`../archetypes/corporate-luxury.md`](../archetypes/corporate-luxury.md) logs **1,559,314 B** (≈1.49 MB) for the same `brunellocucinelli.ai/assets/index-RpG0soLF.js`. The ratio is ≈3:1 (3.06 reading KB as 1000 B, 2.99 as 1024 B), consistent with a compressed transfer size measured against the decompressed resource size, the usual Brotli ratio for a minified JS bundle. Both figures stand as measured; response headers were not read, so which reading is the transfer size is unconfirmed.

Evidence tags: `[CSS]` / `[JS]` = read from the sibling build's shipped stylesheet and bundle; **observed** = from the case study or implied by structure, not read in code.

## 1. Hover / micro-interactions

- **Buttons and CTAs are not a color fill.** `[CSS]` The primary controls are circular and pill icon-buttons: `.o-button{--btn-bg:var(--color-white);border-radius:100%}`, expanded variant `border-radius:40px;padding:0 20px`. The hover micro-interaction is a **stroke-drawn SVG circle** that completes and rotates:
  `.can-hover a:hover .o-icon--circle{--speed:10ms;opacity:.3;stroke-dashoffset:0;transform:rotate(180deg)}`
  The CTA never fills with charcoal, never inverts, and never washes to a pale tint. It draws a ring outline (`stroke-dashoffset → 0`), rotates 180°, and drops icon opacity to `.3`. The luxury signature is line-draw rather than fill.
- **AI prompt submit button** `[CSS]`: `.c-prompt-wrapper .o-button{--btn-bg:#e9e9e9…transform:translateY(-50%)}` with icon `transform:rotate(180deg)`, a **pale-gray `#e9e9e9`** circular submit affordance pinned right-center of the prompt bar.
- **Images and cards** `[CSS]`: `.product-card-container:hover .product-card-img{transform:scale(1.05)}`, guarded by `@media (hover:hover) and (pointer:fine)`, plus a slower editorial variant `.can-hover a:hover .o-media-zoom{transition:transform 1.5s cubic-bezier(.165,.84,.44,1);transform:scale(1.05)}`: **1.05× zoom over 1.5s easeOutQuint.**
- **Nav bar surface** `[CSS]`: `.c-site-header` is `position:fixed; pointer-events:none` (an overlay), flex `space-between`, with the **logo absolutely centered** (`left:50%;transform:translate(-50%,-50%)`). There is **no solid scrolled background and no differently-colored border-bottom.** The header sits under a soft **gradient PNG scrim** instead: `.c-site-header:before{background-image:url(/assets/header-gradient-02…png);height:250%}`, a photographic top-down fade rather than a CSS fill or rule. No `backdrop-filter` on the header itself.

## 2. Motion & scroll

`[JS, values]` unless tagged otherwise.

- **Smooth scroll via Lenis**; scroll-linked animation via **GSAP ScrollTrigger**, with `onEnter`/`onLeave` callbacks present.
- **Durations cluster 0.3–0.6s**: `duration:` values run heaviest at `.3`, `.4`, `.5`, `.6`.
- **Primary GSAP ease: `"power1.out"`**, the only named ease found.
- **CSS easings in use** `[CSS]`: `cubic-bezier(.165,.84,.44,1)` (easeOutQuint, the dominant reveal and zoom curve), `cubic-bezier(.77,0,.175,1)` (easeInOutQuart, e.g. `transform .8s`), `cubic-bezier(.16,1,.3,1)` (easeOutExpo). Slow reveals reach `transform 1.5s` and `transform 1.2s,opacity 1.2s`.
- Pin and scrub scroll on the SOTD shop could **not** be confirmed; only `Pin:0` was visible in the minified source. Parallax is **observed** only, implied by the full-bleed `.ep-banner` and media-zoom layers but not provable from minified JS.

## 3. Text effects

- No CSS `SplitText` or char-split classes surfaced; the CSS carries a single `overflow:hidden`. **Per-char and per-word reveals, if present, run through GSAP inline styles rather than CSS** (**observed**); SplitText is absent from the bundle's GSAP plugins.
- **Display type is a high-contrast serif** `[CSS]`: `font-family:freight-big-pro,serif` (FreightBig Pro) at display, with `freight-text-pro,serif` for body. Label and UI type is sans **GT Eesti** (`GTEesti,sans-serif`) set uppercase with `letter-spacing:.1em` / `.03em`. Also loaded: `cieffe-video` (brand display face) and `IM Fell Great Primer`, an antique historical serif carrying the crafted, hand-drawn editorial accent.

## 4. Cursor & pointer

`[CSS]` throughout.

- **Custom cursor confirmed** over the WebGL hero: `.ep-banner-overlay{cursor:none;height:110%}`. The banner hides the native cursor and drives its own.
- A **pointer-following frosted tooltip** exists: `.tooltip-mouse{backdrop-filter:blur(30px);background-image:linear-gradient(110deg,rgba(252,255,255,.8),rgba(252,255,255,.5));border:1px…}` alongside `.mobile-overlay-tooltip`; the cursor carries a blurred glass label.
- Standard `cursor:pointer` elsewhere; Fancybox adds `zoom-in`/`zoom-out`/`grab`/`grabbing` on the image lightbox.

## 5. Loaders / intros

`[JS tokens]`; the behavior itself is **observed**.

A **loader with a percentage counter** is present: the app bundle carries `loader` (22), `percent`/`Percent` (34), `progress`/`Progress` (82), plus `intro` (6), `splash` (1), `reveal` (9). The exact visual, numeric percentage versus bar, is not observable from minified code, but a percent-driven preloader is unambiguous.

## 6. Notable signature interactions

- **Frosted glass system**, the case study's named signature `[CSS]`: menus and tooltips use `backdrop-filter:blur(30px)` over a warm-white `linear-gradient(110deg,rgba(252,255,255,.8) 0%,rgba(252,255,255,.5) 93%)`; overlays use `blur(10px)` (`.ep-overlay`, and `.transparent{backdrop-filter:blur(10px);background:rgba(255,255,255,.6);box-shadow:0 4px 45px rgba(0,0,0,.1)}`). The `--f-*` transitions and backdrop-filters also present in the CSS are **Fancybox defaults**, not bespoke, and are excluded from this claim.
- **WebGL interactive "experience banner"** `[CSS]`: `.ep-banner-container{aspect-ratio:16/6;width:100dvw;margin:6rem 0}` full-bleed, with the custom-cursor overlay, a cinematic hero that bleeds past container padding; mobile collapses to `aspect-ratio:1`.
- **Circle-draw icon buttons** (§1): the repeated stroke-draw plus 180° rotate is the recurring interaction motif standing in for hover fills.
- **AI prompt bar** `.c-prompt` / `.c-prompt-wrapper` with the `#e9e9e9` submit button `[CSS]` matches the case study's "contextual prompt bar with subtle interactive cues." An `.easter-egg-button` (fixed 8rem, bottom-left) and an `.ep-menu-container` frosted radial menu are also present.

## Exact tokens

`[CSS]`, from the `brunellocucinelli.ai` `:root`.

| Token | Hex | Role |
|---|---|---|
| `--color-light-gray` | `#f8f8f6` | **body background** (cream/off-white) |
| `--color-pale-almond` | `#f5f3ef` | pale warm surface |
| `--color-almond` | `#eeebe4` | almond surface |
| `--color-pale-pink` | `#f8f5f3` | pale surface |
| `--color-light-pink` | `#ece4df` | warm blush surface |
| `--color-pale-beige` | `#dfdbd8` | beige |
| `--color-black` | `#000` | **body text** |
| `--color-dark-gray` | `#262626` | charcoal |
| `--color-mid-gray` | `#56575b` | mid gray |
| `--color-dark-soil` / `--color-mid-soil` | `#71685f` / `#8d8277` | warm taupe accents ("soil") |
| `--color-overlay-bg` | `rgba(86,87,91,.3)` | scrim |

Body defaults: `--body-bg:var(--color-light-gray)` (`#f8f8f6`) on `--body-color:var(--color-black)`, a warm off-white ground under near-black text, with the almond and blush surfaces (`#eeebe4`, `#f5f3ef`) layered above it. **These are the `.ai` domain's tokens; the shop's exact hexes are unverified.**

**Fonts** `[CSS, typekit vbi4iuh.css]`: FreightBig Pro (display serif), FreightText Pro (body serif), weights 400/500/700 plus italics; GT Eesti (sans, uppercase labels); `cieffe-video` (brand face); IM Fell Great Primer (antique serif accent). Serif at display, FreightBig Pro.

**WebGL and GSAP** `[JS]`: GSAP + ScrollTrigger + Lenis + Fancybox + React; an interactive `.ep-banner` hero with `cursor:none`, canvas/WebGL, engine not fully resolvable from the minified integration loader. The Solomei AI "webxp" layer is injected via `art.solomei.ai/webxp-integration.min.js`.

## Could not verify

- **The awarded shop page's own code**: nothing was extracted from `shop.brunellocucinelli.com/en-gb/ai`, so the shop's exact hexes and durations cannot be proven identical to the sibling build's.
- **Which bundle size is the transfer size** (510 KB here, 1,559,314 B in [`../archetypes/corporate-luxury.md`](../archetypes/corporate-luxury.md)): response headers were not read.
- **Pin and scrub scroll** on the shop: only `Pin:0` was visible in the minified source.
- **Parallax**: implied by the full-bleed `.ep-banner` and media-zoom layers, not provable from minified JS.
- **Per-char and per-word reveals**: SplitText is absent from the bundle's plugins; any such reveal runs through GSAP inline styles.
- **The loader's visual form** (numeric percentage versus bar): a percent-driven preloader is unambiguous from the tokens, its rendering is not.
- **The WebGL engine** behind `.ep-banner`: not resolvable from the minified integration loader.
- **Concept-level AI behavior**: from the makemepulse case study only.
