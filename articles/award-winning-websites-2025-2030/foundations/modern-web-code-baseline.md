---
title: "Modern Web Code Baseline — Mid-2026"
date: "2026-07-30"
author: "Coroboros"
tags: ["css", "oklch", "design-tokens", "container-queries", "view-transitions", "baseline", "accessibility", "wcag", "core-web-vitals", "performance", "progressive-enhancement"]
sources:
  - "https://chrome.dev/css-wrapped-2025/"
  - "https://web.dev/baseline/2025"
  - "https://web.dev/blog/same-document-view-transitions-are-now-baseline-newly-available"
  - "https://web.dev/articles/baseline-in-action-color-theme"
  - "https://web.dev/articles/vitals"
  - "https://developer.mozilla.org/en-US/docs/Web/CSS/color_value/oklch"
  - "https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_colors/Relative_colors"
  - "https://developer.chrome.com/blog/css-relative-color-syntax"
  - "https://developer.chrome.com/blog/hardware-accelerated-animations"
  - "https://www.w3.org/TR/WCAG22/"
  - "https://www.w3.org/WAI/ARIA/apg/"
  - "https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Accessibility/WAI-ARIA_basics"
  - "https://www.deque.com/en-301-549-compliance/"
  - "https://evilmartians.com/chronicles/oklch-in-css-why-quit-rgb-hsl"
---

# Modern Web Code Baseline — Mid-2026

Six CSS features carry a Baseline verdict here; nine more stay open, `animation-timeline` among them. No feature below Baseline is treated as a default. The verdicts, and the accessibility and performance floor award front-ends rely on, are primary-sourced — web.dev, Chrome Developers, MDN, W3C. Visual archetypes live in [the parent reference](../award-winning-websites-2025-2030.md).

Three adoption classes emerge: adopt unguarded, ship behind feature detection, or treat as progressive enhancement only.

---

## Per-feature Baseline verdict

| Feature | Baseline status, mid-2026 | Verdict |
|---|---|---|
| Container queries | Widely available | adopt as default |
| `oklch()` | Widely available since May 2023; Widely recorded 2025-11-09 (~93–95% reach) | adopt as default, no `@supports` guard |
| `content-visibility` | Newly available 2025-09-15 (Safari 26 was the last engine) | shippable by default — unsupported engines ignore it and render normally |
| Same-document View Transitions + `view-transition-class` | Newly available 2025-10-14 (Firefox 144 completed interop) | progressive enhancement, feature-detect — the least settled cell here |
| Relative color syntax `oklch(from …)` | Newly available 2024-09 | progressive enhancement, not Widely |
| Cross-document View Transitions | not Baseline (Firefox and Safari lag) | progressive enhancement only |

Chrome's CSS Wrapped 2025 states verbatim that "Container Queries reach Baseline Widely available"; the timing checks out (Newly Feb 2023 + 30 months = Aug 2025). Firefox's initial same-document View Transitions release omits view-transition types and `document.startViewTransition` needs a JS guard — the source itself recommends a `transitionHelper`, which is why it sits in the feature-detected class rather than as an unguarded default.

**Newly available is not Widely available.** Newly-available features reach ~95% support roughly 30 months later, around 2028. That gap is why the feature-detected class stays guarded.

---

## Color — OKLCH as the authoring space

OKLCH is the baseline authoring color space, and the reason is its lightness channel. MDN: "The L in `oklch()` is the perceived lightness … different from the L in `hsl()`, where it represents lightness as compared to other colors."

Chrome Developers: "The OKLCH, OKLAB, XYZ or sRGB color spaces provide the most predictable results when lightening colors," and on palette generation, "The lightness channel is reliable and the hue channel can be rotated without side effects." web.dev: "OkLCh is a good format for this type of color manipulation, as it's designed to provide perceptual uniformity."

OKLCH derives from Ottosson's Oklab (2020), which tracks measured human visual response. The textbook counterexample — yellow and blue at HSL `L=50%` look very different in brightness, while OKLCH holds them level — is corroborated across MDN, Evil Martians, and CSS-Tricks. Known criticism of OKLCH targets hue linearity and gamut clipping on real displays, not the lightness claim.

### Factorization as a shipped technique

An entire brand ramp derives from a single `--base-color` custom property. web.dev, verbatim: "If you need to change the base color for branding, you can just update the `--base-color`, and the rest of the theme will flow from that."

MDN gives the canonical form `color-function(from origin-color channel1 channel2 channel3 [/ alpha])` and states relative colors work with `color()`, `hsl()`, `hwb()`, `lab()`, `lch()`, `oklab()`, `oklch()`, and `rgb()`. `var()` as origin and `calc()` on channels are both documented:

```css
oklch(from var(--base-color) l c calc(h + 180))  /* hue rotation */
oklch(from #123456 calc(l + 0.1) c h)            /* lightening */
oklch(from green l c h / 0.5)                    /* alpha */
```

Chrome Developers: "The goal of relative color syntax is to allow deriving a color from another color."

Two qualifications. "Entire theme" overreaches — the article derives the brand and accent ramp from `--base-color` while keeping `--background-color` and `--text-color` as separate base variables; it is a brand ramp. And `oklch()` itself is Widely available while relative-color derivation and gradient interpolation in oklch are only Newly available, so the authoring pattern is production-grade but the derived output needs a cascade fallback.

---

## The accessibility floor

Confirmed against W3C primaries. WCAG 2.2 is the current Recommendation.

- **SC 1.4.3 (AA)** — text contrast "at least 4.5:1 … 3:1" for large text. No exception for translucent backgrounds: glass surfaces are measured against their composited background.
- **SC 2.4.7 (AA)** — visible keyboard focus is required for conformance. No global `outline: none`.
- **SC 2.5.8 (AA)** — interactive targets "at least 24 by 24 CSS pixels." The normative unit is CSS pixels, which makes this the concrete place where `px` — not `rem` or `clamp()` — maps directly to the spec. `rem` also satisfies it, so px is *a* correct unit here, not the only one.
- **SC 2.4.13 (AAA)** — Focus Appearance sets a measurable 2-CSS-px-perimeter and 3:1 focused-to-unfocused target. Above the legal floor.
- **SC 2.3.3 (AAA)** — "Motion animation triggered by interaction can be disabled, unless … essential" is the standards basis for the `prefers-reduced-motion` swap (Technique C39). Also above the legal floor.

Native semantics come first. W3C ARIA APG: "Unlike HTML input elements, ARIA roles do not cause browsers to provide keyboard behaviors," and "a role is a promise that the author … has also incorporated JavaScript that provides the keyboard interactions." MDN: "use HTML semantics where possible and only use ARIA where there is no HTML equivalent." For dynamic content, `aria-live` polite is "announced only if the user is idle," assertive "as soon as possible."

**Legal context.** The EAA 2025 / EN 301 549 floor is WCAG AA, so 1.4.3, 2.4.7, and 2.5.8 are legally load-bearing. 2.4.13 and 2.3.3 are best-practice targets above the mandate.

---

## Performance

**The compositor-thread animation set** is `transform`, `opacity`, and `filter`. Chrome Developers (Feb 2021), with the source's own emphasis: "the current CSS properties that are hardware-accelerated by default only include opacity, filter, and transform." Chromium's GPU-compositing design doc adds `backdrop-filter` as a fourth compositor-mutable property. Animate only these for 60fps.

**Core Web Vitals.** Google's official "good" thresholds at the 75th percentile are LCP ≤ 2.5s, INP ≤ 200ms, CLS ≤ 0.1 — web.dev: "LCP should occur within 2.5 seconds … an INP of 200 milliseconds or less … a CLS of 0.1 or less."

A stricter budget of LCP < 1.5s / INP < 100ms / CLS < 0.05 is therefore a **stretch target, not the platform baseline**, and is not Google's. A purported "March 2026 LCP lowered to 2.0s" appears only in low-quality SEO blogs; a domain-restricted search across web.dev, developer.chrome.com, and chromium.org found no official change, with all official sources still showing 2.5s.

The remaining performance practices — `content-visibility: auto` for offscreen work, IntersectionObserver lazy loading with dynamic import of heavy libraries, AVIF > WebP > JPEG in `<picture>`, font preload with `font-display: swap`, Speculation Rules — are individually sound platform practice, but only `content-visibility` carries a standalone confirmed verdict here.

---

## Tells of generated front-end code

The recognizable code tells — inline literals instead of tokens, `px` instead of `rem`, hex or `rgb()` instead of `oklch()`, div-soup instead of semantic HTML, missing `prefers-reduced-motion`, missing `@supports` guards, un-factored repetition, no container queries, one generic fade-in everywhere — are an **inference** from the confirmed baselines above. No citable practitioner source naming them was found, so the list carries no evidentiary weight of its own.

---

## Refuted

- **2025's headline CSS/HTML features shipped Chrome-first with explicit version gates** — invoker commands Chrome 135, dialog light dismiss Chrome 134, scroll-state queries Chrome 133, `moveBefore` Chrome 133, expanded range syntax Chrome 142 — **and are therefore not cross-browser Baseline** — unresolved: the version numbers are cited but the not-Baseline conclusion was never confirmed, so the list is not a verified not-Baseline set.

## Could not verify

Verdicts are pinned to mid-2026. Newly-available features (`content-visibility` 2025-09-15, same-document View Transitions 2025-10-14, relative color 2024-09) have only 9 to 12 months of cross-engine interop.

Three areas were **not verified here** and are not established as baseline:

1. **`rem` + fluid `clamp()` type and space scales as the current baseline.** Only the px-for-touch-targets counterpoint is evidenced; the broader thesis, including where px remains correct for 1px hairline borders and sub-pixel decoration, has no confirmed claim.
2. **Practitioner-named tells for generated front-end code.** Inference, as above.
3. **Several feature verdicts, unresolved** — `:has()`, `@property`, subgrid, cascade layers, CSS nesting, `text-wrap: balance`/`pretty`, scroll-driven animations (`animation-timeline`), `color-mix()` as a standalone verdict, and `animation-trigger`. Their adopt-default versus `@supports` status is open. `color-mix()` appears in supporting evidence for the color-token finding but was not separately confirmed.

Translucent `rgb(/ α)` and `rgba()` remaining correct where an alpha-over-background composite is genuinely wanted is asserted but not independently confirmed.

Open:

- Is `rem` + fluid `clamp()` the confirmed studio baseline, and precisely where does `px` remain correct beyond the 24px touch minimum?
- What are the mid-2026 verdicts for the nine unverified CSS features above?
- Is there a citable source naming the code-level tells of generated front-ends, or does that list stand as inference only?
- Does the general "a value hardcoded in two places is a code-quality failure" principle have an authoritative front-end citation beyond the color-token example — from Locomotive, Active Theory, or Immersive Garden studio practice, say?
