---
title: "Text Effects on Winners — Two Channels Move Together, Never One Global Fade"
date: "2026-07-30"
author: "Coroboros"
tags: ["typography", "kinetic-typography", "scroll-driven-animation", "gsap", "splittext", "lenis", "css", "variable-fonts", "awwwards", "type-as-image"]
sources:
  - "https://www.awwwards.com/sites/terminal-industries"
  - "https://gsap.com/docs/v3/Plugins/SplitText/"
  - "https://developer.mozilla.org/en-US/docs/Web/CSS/animation-timeline"
  - "https://developer.mozilla.org/en-US/docs/Web/CSS/background-clip"
  - "https://blog.olivierlarose.com/tutorials/text-gradient-opacity-on-scroll"
  - "https://tympanus.net/codrops/2025/11/04/creating-3d-scroll-driven-text-animations-with-css-and-gsap/"
  - "https://tympanus.net/codrops/2026/03/11/svg-mask-transitions-on-scroll-with-gsap-and-scrolltrigger/"
  - "https://www.carmenansio.com/articles/variable-font-scroll"
  - "https://www.awwwards.com/inspiration/variable-font-weight-on-scroll-krew"
  - "https://gsap.com/community/forums/topic/27480-animating-text-with-a-gradient-on-scroll/"
  - "https://www.awwwards.com/sites/siena-film-foundation"
  - "https://www.awwwards.com/sites/typography-principles"
  - "https://www.awwwards.com/behind-the-scenes-designing-and-building-365-a-year-of-cartier.html"
  - "https://www.awwwards.com/websites/Editorial%20New/"
  - "https://github.com/undercasetype/Fraunces"
  - "https://pixelambacht.nl/2021/optical-size-hidden-superpower/"
  - "https://developer.mozilla.org/en-US/docs/Web/CSS/font-optical-sizing"
  - "https://web.dev/articles/variable-fonts"
  - "https://eyeondesign.aiga.org/making-rules-breaking-rules-the-art-of-magazine-typography/"
  - "https://www.todaymade.com/blog/bad-typography-examples"
---

# Text Effects on Winners — Two Channels Move Together, Never One Global Fade

Terminal Industries scrubs its pinned headlines on two channels at once (each character fades in on lime, then settles to white in reading order), and that pairing is what separates scroll-linked text that reads as art from a mechanical fade. One winner read live, plus documented peer techniques. Archetype context lives in [the parent reference](../award-winning-websites-2025-2030.md).

**The craft lever, across every recipe below:** two channels moving together (opacity *and* a color pass through an accent, or weight *and* tracking) plus a per-char or per-word stagger. A single-property global fade is what reads as mechanical.

## Terminal Industries teardown

Live URL is `terminal-industries.com` (the `terminal.industries` domain 404s). By REJOUICE and PROPAGANDE; award record in the [minimalist corpus](../archetypes/minimalist.md#corpus). Stack confirmed from the running page:

- **Nuxt 3 / Vue** on Vercel. Fonts: **Suisse Int'l + Geist Mono**, per the [minimalist](../archetypes/minimalist.md) CSS read.
- **Lenis smooth scroll.** `<html class="lenis">` with Lenis's CSS custom properties on the root.
- **GSAP.** Identified by its inline-style fingerprint on animated elements (`translate: none; rotate: none; scale: none; transform: translate(0px,0px); opacity: …`, the exact string GSAP writes). Bundled, no window global.
- **No ScrollTrigger pin-spacers exist in the DOM.** Pinning is CSS `position: sticky`, not ScrollTrigger's `pin`, the Lenis-friendly pattern that avoids pin jank under a smooth-scroll proxy.
- Palette tokens: `--c-light-light-gray: #ddd`, `--c-lime: #abff02`, `--c-dark-green: #052424`, `--c-white: #fff`.

### The signature — "title-sequence"

Structure, confirmed:

- A `<section class="video-carousel">` is three viewports tall (`height: 2025px`, `overflow: clip`).
- Inside, `<div class="content">` is `position: sticky; top: 0; height: 100vh`: this is the pin.
- Inside the sticky box, several `<h2 class="title title-sequence">` stack at `position: absolute; top: ~395px`, occupying the same spot and handing off.
- Each headline splits per line then per char: `<span class="--line"><span class="--char" aria-hidden="true">W</span>…`. Spans are `aria-hidden`; the accessible text is exposed separately, the standard SplitText a11y pattern.

Mechanic, confirmed by probing computed styles across scroll positions: GSAP writes inline `opacity` and `color` per char, scrubbed to scroll progress with a left-to-right per-char stagger. A char's life cycle:

```
opacity:0 + color:#abff02 (lime) → opacity:1 + color:#abff02 → opacity:1 + color:#fff (white)
```

Each character fades in **as lime**, then settles lime→white, chars resolving in reading order. At one mid-scroll sample the first char was already `rgb(255,255,255)` while the tail was still `rgb(171,255,2)`: a visible sweep, not a global fade. That lime entrance color settling to white is the craft signature. As the sticky section scrolls, one headline hands off to the next.

Trigger: scroll-scrubbed, not fire-once; range is the three-viewport sticky section; per-char stagger; near-linear scrub. Not legible-first: it reveals from `opacity: 0`, which is safe here because it is a hero with the real text in the a11y tree and the reveal completes fast within one sticky span.

### Secondary mechanics on the same site

- **`.split-chars` (feature lists): fire-once color-in with accent flash.** Per-char spans carry `style="--v-delay: 0s"` (a per-char stagger var set by JS) running a pure-CSS `@keyframes color-transition`: `0% #ddd → 30% #abff02 (lime) → 100% #052424 (dark-green)`, `animation: color-transition 0.5s`, `animation-delay: var(--v-delay)`. On light sections the text writes on from pale-gray, flashes lime, lands readable dark-green. JS only sets the stagger variable.
- **Scroll hint ("Scroll to explore"): per-char opacity shimmer**, `opacity: 0.0036 … 1` as a wave across chars.
- **Footer emphasis: legible-first dim→bright.** `.footer-title strong .--char { color: rgba(255,255,255,0.2) }` is the baseline; emphasized words scrub 0.2 → 1 white.
- **Clip-mask line slide.** Present in CSS but not rendered on the homepage: a `.text` component with `.char-wrapper { overflow: clip }`, `.char { display: inline-block }`, `.char-wrapper + .char-wrapper { margin-left: -0.05em }`, chars sliding up out of a clipped box.

## Recipes

### 1. Sticky per-char color-settle sequence (Terminal's signature)

Headlines pinned center-screen; each char fades in on an accent color then settles to the base color, char by char, one headline handing to the next on scroll.

- **Mechanic.** Per-char `opacity 0→1` **and** `color: <accent> → <base>`, scrubbed. Two channels moving together is what separates it from a plain fade.
- **Trigger.** Scroll-scrubbed over a sticky section two to three viewports tall, per-char stagger in reading order, near-linear ease.
- **Approach.** CSS `position: sticky; top: 0` for the pin (not ScrollTrigger pin) + Lenis + GSAP ScrollTrigger (`scrub`, `pin: false`) driving SplitText chars. SplitText is free and carries a built-in `mask` option and `aria: "auto"` (adds `aria-label` to the parent, `aria-hidden` to split spans).
- **Legible-first.** No, it reveals from invisible. Keep the range short and the real text in the a11y tree.
- **Deps.** GSAP + ScrollTrigger + SplitText. Not pure-CSS, because two properties scrub per char with stagger.

### 2. Per-word or per-char dim→bright fade (legible-first, safest)

A paragraph or headline sits faintly visible and brightens word by word as it scrolls through center: reading pace made physical.

- **Mechanic.** Per-word or per-char `opacity: 0.15–0.2 → 1`, a dim baseline that never reaches invisible. Optionally `color` or `filter: blur(4px)→0` for a soft variant.
- **Trigger.** Scroll-scrubbed, `start: top`, `end: +≈0.7×viewport`, `stagger: 0.1`, `ease: "none"`.
- **Approach.** GSAP ScrollTrigger + split spans, or pure CSS with `animation-timeline: view()` and `@keyframes { from { opacity: .15 } to { opacity: 1 } }` per span with an index-based `animation-range`.
- **Legible-first.** Yes. Baseline ≥ 0.15 opacity keeps text readable throughout. The safe default for body copy.
- **Deps.** The GSAP version is bulletproof cross-browser; the pure-CSS version works in Chromium and Safari 26, degrading to full opacity elsewhere.

### 3. Fire-once per-char color-in with accent flash (Terminal's `.split-chars`)

On enter, text writes on from pale gray, pulses an accent, lands on its final readable color.

- **Mechanic.** Pure-CSS `@keyframes` on `color`: `0% pale-gray → 30% accent → 100% final`, per char, staggered by `animation-delay: var(--v-delay)`.
- **Trigger.** Fire-once on enter (IntersectionObserver adds a class), per-char stagger via a CSS var set in JS, ~0.5s each.
- **Approach.** Pure CSS animation. JS only splits text and sets the stagger.
- **Legible-first.** Partial. It starts pale-gray at low contrast but visible, and ends fully readable. Raise the start lightness on busy backgrounds.
- **Deps.** None. CSS plus a tiny splitter.

### 4. Clip-mask line or word slide reveal

Lines rise into place from behind an invisible edge: crisp, editorial, typeset.

- **Mechanic.** Wrap each line or word in an `overflow: clip` box; translate the inner `inline-block` from `translateY(100%)` to `0`. Use `overflow: clip`, not `hidden`: `clip` does not create a scroll container, which matters next to sticky or scroll-timeline sections.
- **Trigger.** Fire-once on enter, or scrubbed for a scroll-tied version; per-line stagger; expressive ease such as `cubic-bezier(.19,1,.22,1)`.
- **Approach.** `SplitText({ type: "lines,words", mask: "lines" })` gives the clip wrappers for free, or pure CSS with a wrapper + transform + `animation-timeline: view()`.
- **Legible-first.** No, hidden until revealed. Safe for headings, not for long body copy.
- **Deps.** Pure-CSS achievable; SplitText's `autoSplit` makes line-masking survive reflow.

### 5. Kinetic variable-font weight on scroll (pure CSS, no JS)

A word visibly gains or loses weight, and tightens tracking, as it scrolls: motion in the letterforms themselves rather than a transform.

- **Mechanic.** Animate `font-variation-settings: 'wght' 300 → 700` plus `letter-spacing`; the `wght` axis interpolates continuously.
- **Trigger.** `view-timeline-name` on the wrapper, `animation-timeline` + `animation-range: contain 0% contain 100%` on the heading, `animation: weight linear both`. Real-world example: Krew's variable font weight on scroll.
- **Approach.** Pure CSS scroll-driven animation. **Baseline caveat:** `animation-timeline` is not Baseline: Chromium 115+ yes, Safari only in recent versions, Firefox partial or behind a flag. The fallback renders the `from` weight, so either degrade gracefully or drive `font-variation-settings` with GSAP for full support.
- **Legible-first.** Yes. Text stays fully legible; only weight and tracking change.
- **Deps.** None for the CSS version beyond a variable font; GSAP only for Firefox or older-Safari parity.

### 6. `background-clip: text` gradient wipe heading

A headline fills or sweeps with a gradient, or brightens through a moving band, as it scrolls.

- **Mechanic.** `background: linear-gradient(...); -webkit-background-clip: text; color: transparent;` then animate `background-position` or a `--fill` gradient stop across the text. Per-word for an emphasis-fill variant.
- **Trigger.** Scroll-scrubbed `background-position`, or a fire-once CSS transition on enter.
- **Approach.** Pure CSS (`background-clip: text` + `background-size: 200%` + a `background-position` transition) for the fire-once version; GSAP scrub for the scroll-tied one.
- **Legible-first.** Conditional. If both gradient stops are legible against the background it is dim→bright-safe; if one stop is transparent or near-background it becomes a reveal. Keep both stops readable for body use.
- **Deps.** Needs the `-webkit-` prefix and can clash with underlines.

### 7. 3D scroll-driven text — cylinder or tube (peer, high-effort)

Words orbit on a rotating cylinder or recede down a tube on scroll.

- **Mechanic.** Per-word `rotateX`/`rotateY` on a `perspective` stage; `translate3d` places words on the drum; `backface-visibility: hidden` prevents mirrored text.
- **Trigger.** Scroll-scrubbed over a very long range (`end: "+=2000svh"`), `scrub: 2` for lag, `perspective: 70vw`, `transform-style: preserve-3d`.
- **Approach.** CSS 3D transforms + GSAP ScrollTrigger scrub.
- **Legible-first.** No. Rotating text is periodically unreadable by design. Decorative only.
- **Deps.** GSAP for the scrub math; the 3D itself is CSS.

## Type-as-image signature

Editorial winners do not pick a serif well: they treat the display type as the composition. Either a genuinely bespoke or commissioned face, or a retail variable face pushed past its defaults (extreme optical size, custom axis instances) and set as a full-bleed, oversized, art-directed object. The strongest lever available without commissioning a typeface is **optical-size (`opsz`) instancing on a display variable serif** plus **treating the masthead wordmark as drawn SVG art**, not a text node.

### The levers, ranked

1. **Push the optical-size axis to a custom display instance.** The biggest win, zero commission. `opsz` is the only axis that redraws glyph outlines for size; at large values a display serif gains contrast and refinement a static font cannot. Fraunces exposes `opsz 9–144`, `wght 100–900`, plus `SOFT 0–100` and `WONK 0/1` (leaning and bulbous alternates): an Old Style face explicitly built for art direction at display scale. How: `font-variation-settings: 'opsz' 144, 'wght' 340, 'WONK' 1;` on the masthead, decoupled from `font-size`. Sources: [github.com/undercasetype/Fraunces](https://github.com/undercasetype/Fraunces), [pixelambacht.nl/2021/optical-size-hidden-superpower](https://pixelambacht.nl/2021/optical-size-hidden-superpower/), [MDN font-optical-sizing](https://developer.mozilla.org/en-US/docs/Web/CSS/font-optical-sizing).
2. **Treat the masthead as drawn lettering / SVG, not a text node.** The exclusivity read juries reward comes from letterforms that behave "like photography does — both as flat color and dimensional" (Sawdust's bespoke *Wired* alphabet). Drawing a *single* wordmark as SVG paths (custom ligature, spliced counter, bespoke ampersand or numeral) gets roughly 80% of that read. How: hand-set the one hero word as `<svg>` outlines; body stays retail. Source: [Eye on Design, Type as Image / Lettering as Message](https://eyeondesign.aiga.org/making-rules-breaking-rules-the-art-of-magazine-typography/).
3. **Compose type AS the image: full-bleed, oversized, one word owns the frame.** Neville Brody's core move at *The Face*: "typography was also about image-making": alternate a large word on a page against near-empty spreads so scale, not decoration, carries the peak. How: peak section is one display word at 20–40vw, tight negative leading, deliberate overlap or collage of a second layer. Source: the same Eye on Design piece.
4. **Animate an axis on scroll or interaction for a kinetic masthead, as accent, not as the whole idea.** Obys *Typography Principles* (Awwwards Site of the Day, Webby nominee) is a WebGL + GSAP horizontal-scroll type microsite where the type is the subject. How: interpolate `wght`/`opsz`/`slnt` on scroll via `font-variation-settings` keyframes, pausing off-screen with IntersectionObserver. Sources: [awwwards.com/sites/typography-principles](https://www.awwwards.com/sites/typography-principles), [web.dev/articles/variable-fonts](https://web.dev/articles/variable-fonts).
5. **Use the GRAD axis for hover and scroll weight shifts that do not reflow.** Grade "changes the weight without changing the widths, so line breaks do not change": the masthead can breathe or darken on interaction with zero layout jump. How: `font-variation-settings: 'GRAD' var(--grad);` animating `--grad` from `-200` to `150`. Source: [web.dev/articles/variable-fonts](https://web.dev/articles/variable-fonts).

### The climax — composed still versus on-scroll component

The sustained climax is a composed peak spread where the type is the image **at rest**. The verified interactive winners build their climax as an *on-scroll* component instead: Siena Film Foundation (credited to Niccolò Miranda with G-NS Studio and Federico Valla) peaks on a WebGL cinematic-filmstrip slider plus a looping rollover; Cartier *365* peaks on scroll-reactive article components: jewelry step-by-step, film reel, mirror/backwards split. Neither reads as a dominant still. The still-that-reads-as-climax comes from magazine art direction, not from a cited web-award technique: design the peak so a scrubbed frame is already the payoff (oversized type plus one hero image locked in composition) and make motion decorative on top, never load-bearing. Sources: [awwwards.com/sites/siena-film-foundation](https://www.awwwards.com/sites/siena-film-foundation), [Awwwards, Behind the Scenes: 365 A Year of Cartier](https://www.awwwards.com/behind-the-scenes-designing-and-building-365-a-year-of-cartier.html), Eye on Design (above).

### Buildable without a commission

- **`opsz` custom instancing** on Fraunces or any `opsz`-bearing variable face, a verified free option.
- **Custom axis instances.** `GRAD`, `SOFT`, `WONK`, `slnt`, `wdth` set via `font-variation-settings`, animated on scroll.
- **One-off SVG or drawn masthead.** The single hero word hand-set as outlines with a bespoke ligature, ampersand or numeral. The strongest bespoke cheat: it reads as commissioned without a commissioned face.
- **Layout-as-composition.** Extreme scale, tight negative leading, overlap and collage, type as full-bleed hero.

**Genuinely needs a bespoke face:** a *consistent commissioned alphabet used site-wide*, the Sawdust/*Wired* model. Levers 1–3 carry most of the winning read; only a full custom alphabet (every glyph, every surface) requires the commission.

### Type anti-slop

- **Retail editorial faces overexposed to the point of reading as default.** "Editorial New" (Pangram Pangram, with Locomotive) and **Bodoni Moda** are common enough on Awwwards that "Editorial New" has its own [collection page of sites using it](https://www.awwwards.com/websites/Editorial%20New/). A high-contrast Didone at default `opsz` is the jury's obvious answer. Overexposure verified via the collection page; the Bodoni-as-default read is inference from that pattern, not a cited jury quote.
- **The movie-font and academic defaults.** Trajan (dubbed "the movie font"), Papyrus, Palatino: an instant unoriginal signal. Source: [todaymade.com/blog/bad-typography-examples](https://www.todaymade.com/blog/bad-typography-examples).
- **Font left at its defaults.** No `opsz` push, no custom instance, no drawn wordmark, three or more competing families. The masthead is a text node in a picked font, not an art-directed object.
- **Motion doing the work the composition should do.** If the still frame is flat and only the interaction saves it, the climax fails a jury scrub.

## Selection guidance

- **Body copy.** Recipe 2 (dim→bright, legible-first). The only one safe on long text.
- **Hero moment.** Recipe 1. The sustained top-to-bottom feel comes from the sticky section plus the accent-color pass, not from any single fade.
- **Cheap taste win, no library.** Recipe 3, or recipe 5 where support allows.
- **Baseline warning.** CSS scroll-driven animations (`animation-timeline`, `view()`, `scroll()`) are not Baseline as of 2026, with Firefox the gap. Anything that must work everywhere uses GSAP ScrollTrigger; pure-CSS scroll-driven recipes need a graceful `from`-state fallback.

## Could not verify

- **Terminal's scrub driver.** GSAP-internal easing curves, the exact scrub value, and whether the char scrub is driven by ScrollTrigger or a raw Lenis `onScroll` callback: both produce identical inline writes, and the absent pin-spacer only rules out a ScrollTrigger *pin*, not `scrub` with `pin: false`.
- **"Dominant still climax" as a named award technique.** No case study frames its climax as a sustained still; the verified winners peak on interaction. The principle is sourced from magazine design theory and applied by inference.
- **Bodoni Moda's own `opsz` range.** Not independently verified; Fraunces is the recommendation where the axis ranges are confirmed.
- **Aparey** as a second free `opsz` option: named by Pixelambacht, specimen not opened, axis ranges unconfirmed.
