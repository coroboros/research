---
title: "Delvaux — Live CSS and JS Read"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "corporate-luxury", "live-read", "css", "gsap", "scroll-driven-animation", "nuxt", "clip-path", "splittext"]
sources:
  - "https://www.awwwards.com/sites/delvaux-digital-flagship-store"
  - "https://51north.nl/case/delvaux-digital-flagship-store"
  - "https://craftcms.com/partners/51north"
---

# Delvaux — Live CSS and JS Read

Delvaux reads luxury through what it withholds: buttons never change color on hover, the largest image zoom in the stylesheet is 2%, and the site ships neither a custom cursor nor a fullscreen preloader. What does move is a vertical label roll on the CTA and a `clip-path` wipe serving as the house transition. Source-level read of the shipped CSS and JS bundle behind the [Delvaux Digital Flagship Store](https://www.awwwards.com/sites/delvaux-digital-flagship-store), for the [corporate-luxury archetype](../archetypes/corporate-luxury.md). Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

## Awards and stack

Awwwards [Honorable Mention, 15 Jun 2026](https://www.awwwards.com/sites/delvaux-digital-flagship-store), credited to 51North. The page shows no jury score and no aggregate; on 29 Aug 2026 it listed 13 community votes averaging 8.19.

Nuxt/Vue 3 frontend, Craft CMS backend at `api.delvaux.com`. Built by [51North](https://51north.nl/case/delvaux-digital-flagship-store), a [Craft CMS partner](https://craftcms.com/partners/51north), whose case study calls it an "editorial design approach… motion principles… dynamic transitions and subtle animations." The full GSAP suite is registered (ScrollTrigger, ScrollSmoother, SplitText, Flip, Observer), plus Swiper for carousels.

Evidence tags: `[CSS]` = `entry.CwVDPA0A.css`, `[JS]` = main bundle `dS0Cr8tO.js`, both read 9 Jul 2026. A static fetch returned the SSR shell only, so live composition is inferred from source rather than observed; runtime-only values are marked **observed** and collected under Could not verify.

## 1. Hover / micro-interactions

**Buttons and CTAs have no hover color-fill at all, neither pale tint nor full token.** `[CSS]` The `.cta` component is `height:35px; overflow:hidden; display:inline-flex; justify-content:flex-end; gap:10px`. Its fill is fixed by variant and never changes on hover:

- `.cta--black` → solid ink `background-color:#1d1d1b; color:#fff` (full token, not a tint)
- `.cta--white` → `#fff` bg / `#1d1d1b` text
- `.cta--outline-black` → transparent, `1px solid #1d1d1b`; `--outline-black20` → `1px solid rgba(29,29,27,.2)`; `--outline-white`; `--clear`
- `.cta--disabled` → `opacity:.2; pointer-events:none`

**Hover is a vertical label roll-swap.** `[CSS]` Two text copies live in `.cta__text-holder` (`height:100%`, relative). `.cta__text--hover` sits pre-offset at `translateY(100%)`, one line below, clipped by `overflow:hidden`. On `.cta:not(.cta--disabled):hover .cta__text` → `transform:translateY(-100%)`; both labels roll up in unison, the current one sliding out the top as the duplicate rolls into place. Transition `transform .2s cubic-bezier(.65,0,.35,1)`. The loading state swaps text to transparent and spins a 20px ring (`.cta.loading:after`, `spin 1s linear infinite`).

**Seasonal override** `[CSS]`: under the `.end-of-year` / `--dark` theme, `.cta--black` and `.cta--outline-black` recolor from ink to brand oxblood `#6f0b0b`: background and border, and text for the outline variant. This is the only place the burgundy fills a button.

**Text links** `[CSS]`: underlines are static, never animated: `.ts-general-body-link{text-decoration:underline}`, `.change-size-link{text-decoration:underline}`. Text CTAs such as `.product-grid-card__add-to-bag` and `.cys-slide__cta` are `background:transparent; color:#1d1d1b`, with no fill.

**Images and cards** `[CSS]`: near-zero hover motion. The only hover-scale in the stylesheet is `.color-selector__link:hover .color-selector__image → transform:scale(1.02)`, a 2% zoom. No product-grid image zoom rule exists, and no image-swap-on-hover rule exists.

**Nav items** `[CSS]`: `.navigation__list-item-link` cross-fades color over `transition:color 1s cubic-bezier(.65,0,.35,1)` between `#1d1d1b` and oxblood `#6f0b0b`, theme-driven. In the open mega-menu, `.navigation-open__item.--hovering:before` fades in a 2px ink bullet dot at `left:-7px` over `opacity .4s cubic-bezier(.25,1,.5,1)`: a marker, not an underline.

**The nav bar surface** `[CSS]`: `.header-navigation-background` is `position:fixed; top:0; background-color:#fff; color:#333; border-bottom:1px solid rgba(29,29,27,.03)`. The border-bottom is the same ink hue at **3% opacity**, a hairline that is close to invisible rather than a differently-colored accent border. It carries `pointer-events:none`, since it is a background plate behind the nav content. Over the hero it is `display:none`; on scroll, JS reveals the white plate. The header has no `backdrop-filter` and no `mix-blend-mode`. The show/hide toggle is verified; the exact scroll threshold is JS-driven (**observed**).

## 2. Motion & scroll

- **ScrollSmoother** registered `[JS]`; the exact `smooth:` value is not recoverable from the minified bundle.
- **Reveal system** `[JS]`: `initReveals` / `initTitleReveals` / `initBasicReveals` via `ScrollTrigger.create({start: "top " + revealPosition, once:true})`. Reveals fire once.
- **Media clip-path reveals** `[CSS]`: elements wipe in via `clip-path`, `.--in-viewport`/`.--revealed{clip-path:inset(0 0 0 0)}` from a clipped start; hero and section media use `transition:clip-path 1s cubic-bezier(.25,1,.5,1)`, with a 1.5s variant also present.
- **Custom ease** `[JS]`: `revealEase` = `CustomEase.create("revealEase", "0.25, 1, 0.5, 1")`, identical to the CSS `--animation-reveal-ease: cubic-bezier(.25,1,.5,1)` (easeOutQuart). CSS and JS stay consistent.
- **Timing scale** `[CSS]`: `--animation-t1:1.5s, t2:1.3s, t3:1s, t4:.7s, t5:.4s, t6:.2s`; eases `--animation-reveal-ease:cubic-bezier(.25,1,.5,1)`, `--animation-conceal-ease:cubic-bezier(.5,0,.75,0)`, `--animation-in-frame-ease:cubic-bezier(.65,0,.35,1)`.
- **GSAP durations in play** `[JS]`: common `duration:1`, `.8`, `1.4`, `.7`, `.3`; staggers `.03` (per-word), `.2` (per-line), `.05`; eases `power4.out` (15×), `power4.inOut`, `expo`, `back.out`, `power1.inOut`. Parallax uses GSAP `effects` (data-speed style), registered, but the homepage SSR markup carries no `data-speed`/`data-lag`, so per-element parallax values are **observed** only.
- **Section and overlay transitions** `[CSS]`: overlays (search, cart, login, customization) enter and leave with a horizontal clip wipe `clip-path:inset(0 0 0 0)` → `inset(0 0 0 100%)` over `1s cubic-bezier(.25,1,.5,1)`, backed by a `backdrop-filter:blur(4px)` on a `#1d1d1b1a` (10% ink) scrim animating blur 0→4px over 1s.

## 3. Text effects

**Headline reveal: masked line-and-word rise.** `[JS]` `new SplitText(el, {type:"lines, words", wordsClass:"title-reveal-words", linesClass:"title-reveal-line"})`. Each line's innerHTML is re-wrapped in a `<div class="title-reveal-line__text">` mask. On ScrollTrigger enter (`once:true`) a timeline runs:

- line-text elements: `duration:2, y:0, stagger:.2, ease:"power4.inOut"`; lines slide up out of their masks, 0.2s apart
- whole heading: `duration:3, y:0, ease:"power4.out"` starting at +0.4s, a slow container lift underneath
- the split reverts on complete

Words are split too (`stagger:.03` available), but the shipped title timeline staggers by line. `[JS]`

## 4. Cursor & pointer

**No custom cursor and no magnetic cursor.** `[CSS + JS]` No cursor-follower element, no `.cursor`/`magnetic` component in CSS or JS, only native `cursor:pointer`/`grab`. Pointer feedback is limited to Swiper grab cursors on carousels.

## 5. Loaders / intros

**No fullscreen preloader and no percentage counter.** `[CSS]` The only loader styles are small 8px spinning dots (`.loader`, `.cart-modal__content-loader`: `1s linear infinite alternate`) for async cart and data fetches, plus the CTA loading ring. Entrance motion is the scroll/clip reveal system rather than a gated intro screen. A hydration-time hero reveal likely exists but is **observed** only. `.ts-general-intro` is a Genath-serif typography class, not a loader.

## 6. Notable signature interactions

1. **The rolling-label CTA** (§1): the most repeated micro-interaction on the site, and buttons never change color on hover. `[CSS]`
2. **Clip-path wipe as the house transition**: menus, overlays, and section media all reveal and conceal via `clip-path:inset()` on `cubic-bezier(.25,1,.5,1)`. The mega-menu `.navigation-open-holder` opens from `inset(0 0 100% 0)`; overlays close to `inset(0 0 0 100%)` with a blur scrim. `[CSS]`
3. **Masked editorial headline rise** (§3): the signature scroll reveal. `[JS]`

## Exact tokens

- **Background:** `#fff`. **Ink / primary text:** `#1d1d1b`. **Header text:** `#333`. **Muted text:** `#1d1d1b80` (50%). **Hairline borders:** `rgba(29,29,27,.03 / .1 / .2)`. `[CSS]`
- **Brand accent (oxblood/burgundy):** `#6f0b0b` (also `#710000`): seasonal CTA fill, nav-hover color, hamburger in dark theme. Pale rose `#e5b0b0` / `#fef0ed` appear only in the third-party datepicker, never as brand hover tints. `[CSS]`
- **Fonts:** **Genath** (serif, weights Light / Light-Italic / Regular) at display: `.ts-general-intro{font-family:Genath,serif; font-variant-numeric:oldstyle-nums proportional-nums; font-variant-caps:small-caps}`. **Atlas Grotesk** (sans, Light / Light-Italic / Regular / Medium) for body and UI. Serif with oldstyle figures plus small-caps at display. `[CSS]`
- **GSAP specifics:** `CustomEase "revealEase" = "0.25, 1, 0.5, 1"`; SplitText `type:"lines, words"`; title timeline `power4.inOut` (lines, dur 2, stagger .2) + `power4.out` (container, dur 3); ScrollTrigger `once:true`; ScrollSmoother, Flip, and Observer registered. A lone `barba` string appears, but Nuxt owns routing, so its page-transition role is **observed** only. `[JS]`

## Could not verify

- The ScrollSmoother `smooth:` value: registered in the bundle, the number is not recoverable from the minified code.
- The scroll threshold at which the white header plate appears: JS-driven, not read.
- Per-element parallax values: GSAP `effects` is registered, but the SSR homepage carries no `data-speed` / `data-lag` attributes.
- A hydration-time hero reveal: likely, but absent from the SSR shell.
- The `barba` string's role: Nuxt owns routing, so any page-transition use is unconfirmed.
- Live composition overall: a static fetch returned the SSR shell only, so every behavior above is read from source, not observed in a browser.
