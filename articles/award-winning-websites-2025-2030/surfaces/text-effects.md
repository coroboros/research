---
title: "Text Effects — Terminal Industries Teardown and Seven Recipes"
date: "2026-07-30"
author: "Coroboros"
tags: ["typography", "kinetic-typography", "scroll-driven-animation", "gsap", "splittext", "lenis", "css", "variable-fonts", "awwwards"]
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
---

# Text Effects — Terminal Industries Teardown and Seven Recipes

Terminal Industries scrubs its pinned headlines on two channels at once — each character fades in on lime, then settles to white in reading order — and that pairing is what separates scroll-linked text that reads as art from a mechanical fade. One winner read live, plus documented peer techniques. Archetype context lives in [the parent reference](../award-winning-websites-2025-2030.md).

**The craft lever, across every recipe below:** two channels moving together — opacity *and* a color pass through an accent, or weight *and* tracking — plus a per-char or per-word stagger. A single-property global fade is what reads as mechanical.

---

## Terminal Industries teardown

Live URL is `terminal-industries.com` (the `terminal.industries` domain 404s). By REJOUICE, Awwwards Site of the Month (SOTM) Sept 2025. Stack confirmed from the running page:

- **Nuxt 3 / Vue** on Vercel. Fonts: **Suisse Int'l + Geist Mono**, per the corpus's deepest CSS read of the site ([minimalist](../archetypes/minimalist.md)).
- **Lenis smooth scroll** — `<html class="lenis">` with Lenis's CSS custom properties on the root.
- **GSAP** — identified by its inline-style fingerprint on animated elements (`translate: none; rotate: none; scale: none; transform: translate(0px,0px); opacity: …`, the exact string GSAP writes). Bundled, no window global.
- **No ScrollTrigger pin-spacers exist in the DOM.** Pinning is CSS `position: sticky`, not ScrollTrigger's `pin` — the Lenis-friendly pattern that avoids pin jank under a smooth-scroll proxy.
- Palette tokens: `--c-light-light-gray: #ddd`, `--c-lime: #abff02`, `--c-dark-green: #052424`, `--c-white: #fff`.

### The signature — "title-sequence"

Structure, confirmed:

- A `<section class="video-carousel">` is three viewports tall (`height: 2025px`, `overflow: clip`).
- Inside, `<div class="content">` is `position: sticky; top: 0; height: 100vh` — this is the pin.
- Inside the sticky box, several `<h2 class="title title-sequence">` stack at `position: absolute; top: ~395px`, occupying the same spot and handing off.
- Each headline splits per line then per char: `<span class="--line"><span class="--char" aria-hidden="true">W</span>…`. Spans are `aria-hidden`; the accessible text is exposed separately, the standard SplitText a11y pattern.

Mechanic, confirmed by probing computed styles across scroll positions: GSAP writes inline `opacity` and `color` per char, scrubbed to scroll progress with a left-to-right per-char stagger. A char's life cycle:

```
opacity:0 + color:#abff02 (lime) → opacity:1 + color:#abff02 → opacity:1 + color:#fff (white)
```

Each character fades in **as lime**, then settles lime→white, chars resolving in reading order. At one mid-scroll sample the first char was already `rgb(255,255,255)` while the tail was still `rgb(171,255,2)` — a visible sweep, not a global fade. That lime entrance color settling to white is the craft signature. As the sticky section scrolls, one headline hands off to the next.

Trigger: scroll-scrubbed, not fire-once; range is the three-viewport sticky section; per-char stagger; near-linear scrub. Not legible-first — it reveals from `opacity: 0`, which is safe here because it is a hero with the real text in the a11y tree and the reveal completes fast within one sticky span.

### Secondary mechanics on the same site

- **`.split-chars` (feature lists) — fire-once color-in with accent flash.** Per-char spans carry `style="--v-delay: 0s"` (a per-char stagger var set by JS) running a pure-CSS `@keyframes color-transition`: `0% #ddd → 30% #abff02 (lime) → 100% #052424 (dark-green)`, `animation: color-transition 0.5s`, `animation-delay: var(--v-delay)`. On light sections the text writes on from pale-gray, flashes lime, lands readable dark-green. JS only sets the stagger variable.
- **Scroll hint ("Scroll to explore") — per-char opacity shimmer**, `opacity: 0.0036 … 1` as a wave across chars.
- **Footer emphasis — legible-first dim→bright.** `.footer-title strong .--char { color: rgba(255,255,255,0.2) }` is the baseline; emphasized words scrub 0.2 → 1 white.
- **Clip-mask line slide** — present in CSS but not rendered on the homepage: a `.text` component with `.char-wrapper { overflow: clip }`, `.char { display: inline-block }`, `.char-wrapper + .char-wrapper { margin-left: -0.05em }`, chars sliding up out of a clipped box.

### Could not verify

GSAP-internal easing curves, the exact scrub value, and whether the char scrub is driven by ScrollTrigger or a raw Lenis `onScroll` callback could not be read — both produce identical inline writes, and the absent pin-spacer only rules out a ScrollTrigger *pin*, not `scrub` with `pin: false`. The color, opacity, and stagger behavior above is directly observed.

---

## Recipes

### 1. Sticky per-char color-settle sequence (Terminal's signature)

Headlines pinned center-screen; each char fades in on an accent color then settles to the base color, char by char, one headline handing to the next on scroll.

- **Mechanic** — per-char `opacity 0→1` **and** `color: <accent> → <base>`, scrubbed. Two channels moving together is what separates it from a plain fade.
- **Trigger** — scroll-scrubbed over a sticky section two to three viewports tall, per-char stagger in reading order, near-linear ease.
- **Approach** — CSS `position: sticky; top: 0` for the pin (not ScrollTrigger pin) + Lenis + GSAP ScrollTrigger (`scrub`, `pin: false`) driving SplitText chars. SplitText is free and carries a built-in `mask` option and `aria: "auto"` (adds `aria-label` to the parent, `aria-hidden` to split spans).
- **Legible-first** — no, it reveals from invisible. Keep the range short and the real text in the a11y tree.
- **Deps** — GSAP + ScrollTrigger + SplitText. Not pure-CSS, because two properties scrub per char with stagger.

### 2. Per-word or per-char dim→bright fade (legible-first, safest)

A paragraph or headline sits faintly visible and brightens word by word as it scrolls through center — reading pace made physical.

- **Mechanic** — per-word or per-char `opacity: 0.15–0.2 → 1`, a dim baseline that never reaches invisible. Optionally `color` or `filter: blur(4px)→0` for a soft variant.
- **Trigger** — scroll-scrubbed, `start: top`, `end: +≈0.7×viewport`, `stagger: 0.1`, `ease: "none"`.
- **Approach** — GSAP ScrollTrigger + split spans, or pure CSS with `animation-timeline: view()` and `@keyframes { from { opacity: .15 } to { opacity: 1 } }` per span with an index-based `animation-range`.
- **Legible-first** — yes. Baseline ≥ 0.15 opacity keeps text readable throughout. The safe default for body copy.
- **Deps** — the GSAP version is bulletproof cross-browser; the pure-CSS version works in Chromium and Safari 26, degrading to full opacity elsewhere.

### 3. Fire-once per-char color-in with accent flash (Terminal's `.split-chars`)

On enter, text writes on from pale gray, pulses an accent, lands on its final readable color.

- **Mechanic** — pure-CSS `@keyframes` on `color`: `0% pale-gray → 30% accent → 100% final`, per char, staggered by `animation-delay: var(--v-delay)`.
- **Trigger** — fire-once on enter (IntersectionObserver adds a class), per-char stagger via a CSS var set in JS, ~0.5s each.
- **Approach** — pure CSS animation. JS only splits text and sets the stagger.
- **Legible-first** — partial. It starts pale-gray at low contrast but visible, and ends fully readable. Raise the start lightness on busy backgrounds.
- **Deps** — none. CSS plus a tiny splitter.

### 4. Clip-mask line or word slide reveal

Lines rise into place from behind an invisible edge — crisp, editorial, typeset.

- **Mechanic** — wrap each line or word in an `overflow: clip` box; translate the inner `inline-block` from `translateY(100%)` to `0`. Use `overflow: clip`, not `hidden` — `clip` does not create a scroll container, which matters next to sticky or scroll-timeline sections.
- **Trigger** — fire-once on enter, or scrubbed for a scroll-tied version; per-line stagger; expressive ease such as `cubic-bezier(.19,1,.22,1)`.
- **Approach** — `SplitText({ type: "lines,words", mask: "lines" })` gives the clip wrappers for free, or pure CSS with a wrapper + transform + `animation-timeline: view()`.
- **Legible-first** — no, hidden until revealed. Safe for headings, not for long body copy.
- **Deps** — pure-CSS achievable; SplitText makes line-masking robust across reflow via `autoSplit`.

### 5. Kinetic variable-font weight on scroll (pure CSS, no JS)

A word visibly gains or loses weight, and tightens tracking, as it scrolls — motion in the letterforms themselves rather than a transform.

- **Mechanic** — animate `font-variation-settings: 'wght' 300 → 700` plus `letter-spacing`; the `wght` axis interpolates continuously.
- **Trigger** — `view-timeline-name` on the wrapper, `animation-timeline` + `animation-range: contain 0% contain 100%` on the heading, `animation: weight linear both`. Real-world example: Krew's variable font weight on scroll.
- **Approach** — pure CSS scroll-driven animation. **Baseline caveat:** `animation-timeline` is not Baseline — Chromium 115+ yes, Safari only in recent versions, Firefox partial or behind a flag. The fallback renders the `from` weight, so either degrade gracefully or drive `font-variation-settings` with GSAP for full support.
- **Legible-first** — yes. Text stays fully legible; only weight and tracking change.
- **Deps** — none for the CSS version beyond a variable font; GSAP only for Firefox or older-Safari parity.

### 6. `background-clip: text` gradient wipe heading

A headline fills or sweeps with a gradient, or brightens through a moving band, as it scrolls.

- **Mechanic** — `background: linear-gradient(...); -webkit-background-clip: text; color: transparent;` then animate `background-position` or a `--fill` gradient stop across the text. Per-word for an emphasis-fill variant.
- **Trigger** — scroll-scrubbed `background-position`, or a fire-once CSS transition on enter.
- **Approach** — pure CSS (`background-clip: text` + `background-size: 200%` + a `background-position` transition) for the fire-once version; GSAP scrub for the scroll-tied one.
- **Legible-first** — conditional. If both gradient stops are legible against the background it is dim→bright-safe; if one stop is transparent or near-background it becomes a reveal. Keep both stops readable for body use.
- **Deps** — needs the `-webkit-` prefix and can clash with underlines.

### 7. 3D scroll-driven text — cylinder or tube (peer, high-effort)

Words orbit on a rotating cylinder or recede down a tube on scroll.

- **Mechanic** — per-word `rotateX`/`rotateY` on a `perspective` stage; `translate3d` places words on the drum; `backface-visibility: hidden` prevents mirrored text.
- **Trigger** — scroll-scrubbed over a very long range (`end: "+=2000svh"`), `scrub: 2` for lag, `perspective: 70vw`, `transform-style: preserve-3d`.
- **Approach** — CSS 3D transforms + GSAP ScrollTrigger scrub.
- **Legible-first** — no. Rotating text is periodically unreadable by design. Decorative only.
- **Deps** — GSAP for the scrub math; the 3D itself is CSS.

---

## Selection guidance

- **Body copy** — recipe 2 (dim→bright, legible-first). The only one safe on long text.
- **Hero moment** — recipe 1. The sustained top-to-bottom feel comes from the sticky section plus the accent-color pass, not from any single fade.
- **Cheap taste win, no library** — recipe 3, or recipe 5 where support allows.
- **Baseline warning** — CSS scroll-driven animations (`animation-timeline`, `view()`, `scroll()`) are not Baseline as of 2026, with Firefox the gap. Anything that must work everywhere uses GSAP ScrollTrigger; pure-CSS scroll-driven recipes need a graceful `from`-state fallback.
