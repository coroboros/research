---
title: "Navigation and Hover on Winners — No Brand Hairline, No Pale-Tint CTA Hover"
date: "2026-07-30"
author: "Coroboros"
tags: ["navigation", "sticky-header", "backdrop-filter", "button-design", "hover-states", "micro-interactions", "gsap", "awwwards", "anti-patterns"]
sources:
  - "https://www.awwwards.com/inspiration/sticky-header-navigation-aqtos-the-boss"
  - "https://www.awwwards.com/inspiration/blur-effect-scroll-navigation"
  - "https://www.awwwards.com/inspiration/inverted-section-scroll-interaction-doel-festival"
  - "https://www.awwwards.com/inspiration/sticky-section-with-background-colour-transition-finiam"
  - "https://www.joshwcomeau.com/css/backdrop-filter/"
  - "https://www.shadcn.io/blocks/navbar-sticky-blur"
  - "https://www.sliderrevolution.com/design/transparent-navbar-examples/"
  - "https://awesome-design-md-visualizer.vercel.app/preview/stripe"
  - "https://wdesignkit.com/templates/section/scroll-activated-sticky-header-with-bottom-border-effect/18331"
  - "https://theme.co/archive/forums/topic/thin-accent-line-below-navigation-how-to-change-the-color/"
  - "https://www.w3schools.com/howto/howto_css_navbar_border.asp"
  - "https://tympanus.net/codrops/2020/08/05/magnetic-buttons/"
  - "https://github.com/codrops/MagneticButtons"
  - "https://ianlunn.github.io/Hover/"
  - "https://www.awwwards.com/inspiration/magnetic-button-aiyanna"
  - "https://www.awwwards.com/inspiration/magnetic-hover-inette"
  - "https://raw.githubusercontent.com/primer/css/main/src/buttons/button.scss"
  - "https://tailwindcss.com/docs/hover-focus-and-other-states"
  - "https://github.com/shadcn-ui/ui/issues/2788"
  - "https://vercel.com/geist/button"
  - "https://designmd.cc/benchmarks/stripe"
  - "https://designmd.cc/benchmarks/vercel"
  - "https://www.925studios.co/blog/ai-slop-web-design-guide"
  - "https://cuberto.com/"
  - "https://www.figma.com/blog/config-2024-branding/"
  - "https://tympanus.net/codrops/2024/08/21/case-study-design-education-series/"
  - "https://www.awwwards.com/case-study-reinventing-locomotive-r.html"
  - "https://www.awwwards.com/sites/mat-voyce"
  - "https://www.awwwards.com/sites/ponpon-mania"
  - "https://webflow.com/made-in-webflow/website/gsap-flip-corners"
  - "https://www.trapti.dev/blog/creating-a-text-rolling-hover-effect-with-css-and-gsap/"
  - "https://thefwa.com/cases/mat-voyce"
  - "https://www.awwwards.com/sites/obys-2"
  - "https://www.awwwards.com/sites/cuberto"
---

# Navigation and Hover on Winners — No Brand Hairline, No Pale-Tint CTA Hover

No named award winner ships a brand-colored hairline under its nav on scroll, and no verified primary CTA hovers to a pale tint of itself. Two surfaces on genuinely awarded bold and maximal sites, 2023–2026: the nav bar's scroll treatment and the primary CTA's hover. The button-hover half is winner-read; the nav-bar half rests on design-system reconstructions.

Every claim ties to a named site, and durations, easings, and colors are quoted only where read in source. Archetype context lives in [the parent reference](../award-winning-websites-2025-2030.md).

**Award records for the named targets** live in the archetype corpus tables: Mat Voyce, Ponpon Mania, and Cuberto in [bold maximal](../archetypes/bold-maximal.md#corpus); Obys in [experimental](../archetypes/experimental.md#corpus). Mat Voyce runs a two-color palette `#00D3FF`/`#DFFF6B`. Cuberto is the agency behind repeated Awwwards and FWA winners, and Codrops credits the magnetic-fill button pattern to it.

## Nav-bar surface

The families below rest on Awwwards entry tags, a teaching article, and a design-token reconstruction (see Could not verify); the button-hover section that follows is read from source.

### The default nav cliché

A fixed nav starts transparent over the hero, then at a ~50–100px scroll threshold snaps to a white or near-white solid bar with a soft drop-shadow and `transition: all 0.3s ease`, often shrinking in height, and pins a **1px border-bottom in the brand accent color** beneath it. The colored hairline plus the shadow-and-shrink combo are the tells.

### Family 1 — frosted translucent on scroll (dominant, ≥2 named sites)

- **Aqtos – The BOSS** (Glitch Agency): Awwwards entry tagged `header, sticky navigation, blur effect, blur, menu`. The scroll treatment is a backdrop blur.
- **Blend** (`blendingpoint.com`): Awwwards entry titled "Blur effect, scroll navigation."
- **Canonical recipe, verified values.** Josh Comeau documents the sticky frosted header as `background: hsl(0deg 0% 100% / 0.5); backdrop-filter: blur(16px);`: a semi-transparent white surface, 16px blur, and **no border-bottom at all**.
- The productized version (shadcn "Sticky Blur Navbar Block", "Vercel scroll with blur") is clean and borderless at the top, becoming a "frosted glass background with a subtle border" on scroll. The border is neutral, never brand-colored.

This is the only family that clears the two-independent-named-sites threshold cleanly.

### Family 2 — transparent over hero, then transparent or solid

- **Cuberto**, read first-hand from the production DOM: `header.cb-navbar` is `position: static`, `background: rgba(0,0,0,0)`, `backdrop-filter: none`, **zero border-bottom**. It never acquires a surface; the page color changes under it instead.
- **Stripe.** A community design-token reconstruction (`designmd.cc`) states the nav background is `{colors.canvas}` (white `#ffffff`) "or transparent depending on scroll," with no border-bottom documented. Reconstruction, not Stripe's own CSS.
- Named transparent-nav-over-hero sites: **Sézane, SOM, Handel Architects, Rob Mills, Martinkovic Milford, Ikos Oceania**. The roundup does not document each one's scroll transition, so the behavior is observed and the implementation unverified.

### Family 3 — invert via `mix-blend-mode: difference`

The nav text and logo invert against whatever section scrolls beneath, rather than the nav's own surface changing. Named real site: the **Blind Barber** anniversary site. Section-level cousin: **Doel Festival**, "Inverted Section Scroll Interaction" (invert + `mix-blend-mode` + scroll).

Single-source caveat: only one clearly real named site applies this at the nav level. The rest of the corroboration is CodePen demos (farisk, KaiWedekind), not winners. Real pattern, thin naming.

### Border-bottom verdict

**A contrasting brand-color hairline under the nav on scroll was not found on any named award winner.** Across every real reference the border story is one of two things:

- **No border.** The canonical frosted nav omits it entirely; the Stripe reconstruction documents none.
- **Neutral, subtle hairline.** Low-opacity white-on-dark or black-on-light, as in the shadcn/Vercel blur block's "subtle border" and the WDesignKit "scroll-activated sticky header with bottom border" template, which calls it a "stylish bottom line," neutral, no brand color.

The only appearance of a colored nav underline is theme and tutorial land (the X theme's gray line that turns green, Bootstrap and W3Schools `border-bottom` examples), and even there it is a **per-link hover** accent, not a nav-wide brand hairline on scroll. The brand-colored border-bottom is a default cliché, not a winner signature. For a defined edge on scroll, winners use a neutral low-opacity hairline or a pure blur boundary with no line.

## Button hover

### The default button cliché

A primary CTA that on hover does one of these, with `transition-colors` of ~150ms and no motion:

- **Opacity fade of the same color.** `hover:bg-primary/90`, shadcn/ui's literal default variant: a ~10% opacity fade of the *same* color. The button barely changes and reads as dead.
- **Pale or muted tint fill.** The ghost/outline recipe (`hover:bg-accent`, or `hover:bg-primary/10`) misapplied to a *primary* CTA, so a saturated button washes to a faint 10–20% tint of itself.

Both come straight from shadcn/ui's `buttonVariants`, whose strings are: default `bg-primary … hover:bg-primary/90`, outline and ghost `hover:bg-accent hover:text-accent-foreground`, secondary `hover:bg-secondary/80`. The AI-slop critique literature names the symptom directly: "hover states that do nothing," "buttons that snap instead of easing."

### What winners ship — the fill is fully saturated, and it moves

**1. Liquid fill sweeping in from an edge (Cuberto signature).** Verified in source. The fill is a solid circle element, `--button-filler: #ce1352` (vivid magenta, **not** translucent), 150% wide × 200% tall, parked below the button at `translate3d(0,75%,0)`, animated bottom-up on hover via GSAP over **0.5s, ease `Power3.easeOut`**, retracting on leave (`y → -75%`, 0.4s). Demo4's filler is full black `#000`, demo6's is full white `#fff`: every filler is a full token, zero opacity wash. The pattern is credited to Cuberto's button.

The edge is not universal. Hover.css (Ian Lunn, a widely deployed library) ships the same idea as a "Background Transitions" family of 16 named full-color effects (`Sweep To Right/Left/Bottom/Top`, `Bounce To …`, `Radial In/Out`, `Rectangle In/Out`, `Shutter In/Out`), all solid-color, edge chosen by name. Bottom-up is the canonical liquid variant; all four edges are in real use.

**2. Label swap-slide, synchronized with the fill.** Verified in source. On enter, the rest label tweens out (`opacity 0, y -20%`, 0.15s `Power2.easeIn`) while a duplicate rolls in from below (`y 100% → 0%`, 0.2s `Expo.easeOut`), with `overflow: hidden` clipping it. Corroborated on a named SOTD: **filipporuffini.com** uses a GSAP label swap. A second fully independent named winner is thin: the record is one SOTD plus technique docs.

**3. Hover color-shift on a primary CTA goes darker, never paler.** Three independent systems:

- **Stripe.** Primary `#533afd` → hover `#4434d4` (darker), paired with a `translateY(-2px)` lift and shadow.
- **GitHub Primer.** `.btn-primary` hover swaps `--button-primary-bgColor-rest` for `--button-primary-bgColor-hover`, a darkened token, verified in source.
- **Tailwind convention.** The canonical example is `bg-blue-500 hover:bg-blue-700`, darker.

**4. Magnetic pull, a carrier rather than a fill.** The button translates toward the cursor at **0.3× the offset from its center**, triggered when the pointer is within `button.width × 0.7`, LERP-smoothed at amount 0.1; the label counter-moves at 0.6× for parallax. Origin is Cuberto; Awwwards inspiration entries corroborate it on other sites. Magnetism carries one of the fill or swap mechanisms above.

**5. Full solid at rest, no hover wash at all.** Vercel Geist's primary is a full solid `gray-1000` `#171717`. A tint appears only on the tertiary/ghost variant, which "tint[s] with `gray-alpha` on hover": the tint lives on the *transparent* variant, not the CTA.

**Thin or unverified.** Shape and border morph: demo1 uses border `1px → 2px`, color `#d8d4cf → #000`, `border-color 0.2s ease`. Single-source, no second named winner, not a staple. Icon or arrow translate is commonly paired with primary CTAs, but no named-winner implementation with concrete values could be pinned; unverified.

### Pale-tint verdict

A washed-out 10–20% tint fill on a **primary** CTA is absent from real winners and documented brand systems. Every verified primary CTA does one of three things: stays a full solid (Geist `#171717`), shifts to a **darker** shade of the same hue (Stripe `#4434d4`, Primer's hover token, Tailwind `blue-700`), or takes a **fully saturated** directional fill or inversion (Cuberto `#ce1352`, Hover.css solid sweeps).

The faint tint is correct in real systems **only on ghost, tertiary, and outline variants whose rest state is transparent**: there a light tint is an emphasis increase from nothing. The cliché is porting that ghost logic, or shadcn's imperceptible `/90` fade, onto a saturated primary CTA.

Precision note: the only low-opacity value anywhere in the Cuberto/Codrops build is the **custom cursor** dropping to opacity 0.2 as it scales over interactive elements. Never the button fill.

Cursors and loaders on these sites: [Bold Maximal](../archetypes/bold-maximal.md#effect-palette).

## Refuted

- **A contrasting brand-color hairline under the nav on scroll is a winner signature.** False: it was found on no named award winner; every real reference shows either no border or a neutral low-opacity hairline (Border-bottom verdict above).
- **A washed-out 10–20% tint fill is the award-grade primary-CTA hover.** False: every verified primary CTA stays a full solid, shifts darker, or takes a fully saturated fill; the tint is correct only on ghost, tertiary, and outline variants whose rest state is transparent (Pale-tint verdict above).

## Could not verify

No live winner's production CSS could be read for the nav: HTML-to-markdown fetching strips CSS out of the JS-heavy SPAs most award winners are (basement.studio, the Awwwards collection pages, navbar.gallery all returned no usable style data). The verified blur and opacity numbers come from a teaching article and a reconstruction, not from a winning site's own CSS: treat the pattern-level conclusions as solid and the per-site numbers as directional. Stripe and Geist hover values come from design-token references, documented rather than source-verified. The transparent and invert nav families each rest on one strong named site plus weaker corroboration.
