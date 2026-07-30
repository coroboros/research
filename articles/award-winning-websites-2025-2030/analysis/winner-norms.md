---
title: "Winner Norms Measured Live — Three of Five Hold Only in Amended Form"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "photography", "hero-medium", "easing", "navigation", "live-measurement"]
sources:
  - "https://www.awwwards.com"
  - "https://tympanus.net/codrops/"
---

# Winner Norms Measured Live — Three of Five Hold Only in Amended Form

Five design norms often stated as absolutes, measured against Awwwards SOTD/SOTM winners. Three survive only in amended form, one holds without exception, one is moot.

The numbers come from live DevTools instrumentation of seven named winner sites at 1440×900 CSS viewport, devicePixelRatio 2, measured 2026-07-17, plus the winners' Awwwards Site of the Day (SOTD) and Site of the Month (SOTM) pages, SOTM case studies, and Codrops teardowns. Live-probed: **21 Hrs On The Moon** (SOTD Jul 10 2026), **Depo Luxe** by Cuchillo (SOTD Jul 7 2026, 7.62), **Bucks Sauce** (SOTD Jul 3 2026, 7.34), **Meech213** (SOTD Jun 29 2026), **Podium** (SOTD + Developer Award Jun 27 2026), **Balmoral** by MILL3 (SOTD Jun 19 2026, 7.21), **basement.studio** (11× SOTD agency, current build), **Locomotive** — locomotive.ca, SOTM 03/2023 per the Awwwards studio profile ([`studio-variance.md`](./studio-variance.md)); a SOTM Jun 2019 date for the same domain is also on record here and stays unresolved, the studio holding four SOTM.

Parent reference: [`../award-winning-websites-2025-2030.md`](../award-winning-websites-2025-2030.md).

## 1. Real photography ships upscaled — native resolution (~1:1 source pixels at desktop retina) is not the winning norm

**Holds only in amended form — refuted as an absolute by three dated SOTD winners measured live.**

Counter-examples, all at DPR 2; upscale = device pixels needed ÷ source pixels:

- **Depo Luxe** (SOTD Jul 7 2026, luxury/film, 7.62): all 16 full-bleed stills upscaled — worst 1024px natural rendered at 1440 CSS px = **2.81×**; the rest 1.57–1.68×. Hero film loops served 1920w full-bleed = **1.5×**.
- **Podium** (SOTD + Developer Award): visible about-section photos served 367px natural at 429 CSS px = **2.34×** — below 1× CSS resolution.
- **Balmoral** (SOTD): full-bleed 1440px natural at 1440 CSS px = exactly 1× CSS, **2.0×** under retina parity.
- Corroboration: basement.studio (current build, award-version caveat) at 2.46×.

Counter-counter-example: **21 Hrs On The Moon** served 83 images CDN-sized to ≤1.04× — perfect sizing exists, it just is not the winning norm.

**The bar winners actually clear:** no *visible* degradation, not pixel parity. Depo Luxe's 2.8× stretch reads cinematic rather than mushy — film grain, dark grading, and motion absorb it (verified by screenshot). A defensible floor sits **above** observed practice: ≥ ~1× CSS pixels on principal photography with no softness readable at arm's length — Depo Luxe (1024 at 1440 CSS) and Podium (367 at 429 CSS) both ship under it. Strict retina 1:1 is a bandwidth-hostile over-spec that current SOTD winners do not meet. **Observed legitimate exception:** archival or legacy assets that exist only at low resolution (archive photography, SD film stills), masked by grain/grade/motion — the Depo Luxe pattern. Performance mandates on media-heavy pages would produce the same effect; none was observed here.

## 2. Immersive and cinematic heroes are driven — real-time scene, scroll-scrubbed sequence, or dense film loop

**Holds only in amended form — the two-medium list is refuted; the absence of static-procession heroes holds.**

Observed third medium: **dense film loops.**

- **Meech213** (SOTD) — video-led drifting collage of 1080p H.264 loops. The only probed winner whose film loops carry the hero with no engine under them.
- **Podium** — retina canvas (2880px backing) compositing **video textures**: driven presentation of film content.
- **Depo Luxe** — Awwwards-tagged "Film & TV / Luxury", five 1920w full-bleed autoplay loops measured live, scored 7.62. The hero is driven: the site runs a full-screen Three.js shader plane over the monochrome DOM — 46 fragment/vertex shaders, 16 `ShaderMaterial`, 44 `WebGLRenderer` refs ([`../winners/depo-luxe.md`](../winners/depo-luxe.md)) — and [`../archetypes/corporate-luxury.md`](../archetypes/corporate-luxury.md) records the footage as WebGL-displaced under heavy scroll-progress plumbing (`progress` ×161, `onUpdate` ×23) with its `data-speed` parallax scrubbed at `ease:"none"`. Real-time rendered *and* scrubbed, so it corroborates the driven norm rather than extending it.
- Confirming the driven norm elsewhere: 21 Hrs On The Moon (WebGL, 7 canvases), Ribbit (scroll-scrubbed PNG sequence per its Awwwards case study), Igloo Inc / Lusion v3 / Opal Tadpole (Site of the Year level, all real-time).

**No counter-example found:** **no immersive/cinematic winner was found whose hero is static stills with decorative motion only.** Searches across hotel, luxury, and fashion categories surfaced only *nominees* (Villa Vista Magnifika) for the fade-slideshow pattern — no SOTD. Depo Luxe interleaves full-bleed stills, but film loops carry the register.

**The amended norm:** in the immersive/cinematic register, winner hero media are dense and moving — real-time scene, scroll-scrubbed sequence, **or cinematic film loop**. Static procession plus decor was found on no winner in that register. The film-loop leg rests on two probed winners, and only weakly: Meech213 alone carries loops with nothing driving them, while Podium composites its loops through a retina canvas. Read it as one site, not a class. **Observed legitimate exception:** a finished film supplied as the hero — the Meech213 pattern, inside the observed set. Density and pixel floors for the scrubbed path: [`scrub-fidelity-floor.md`](./scrub-fidelity-floor.md).

## 3. One treatment per interactive role, page-wide — no measured exception

**Holds without exception across every button and link measured — no credible winner violates it.**

Counter-examples examined: brutalist and maximalist angles (Gucci SS18, Houkago Calpis, neo-brutalist collections), CHILE20 by Active Theory (SOTM Oct 2020, three differently art-directed "product worlds"), plus live computed-style diffs of every visible button and link on five winners.

- **Balmoral** (e-com, 37 interactive elements): all section CTAs identical 14px uppercase text-links; product-card links uniformly 18px; cookie "Accept" (1px border) vs "Decline" (borderless) is primary/secondary hierarchy, not violation. White-on-photo vs dark-on-cream is systematic context inversion.
- **Bucks Sauce**: exactly one styled CTA treatment (solid dark "SHOP NOW") plus 24 uniform text links.
- **Podium, Meech213, basement.studio**: role-uniform down to identical token values (Meech213's nav: one treatment, active state = opacity only).

CHILE20's per-world art direction is chapter-level theming of the entire canvas — a declared narrative device, not per-instance restyling of one role (HUD consistency unverifiable, site offline).

**Observed variations that are not violations:** emphasis hierarchy (primary/ghost), systematic light/dark context inversion, declared chapter theming that re-themes *everything* at once. **Legitimate exception, not observed in the probed set:** embedded third-party brand components that keep their own identity (payment buttons, client sub-brands inside a portfolio piece).

## 4. Show-on-scroll-up nav with hysteresis — no probed winner runs direction-reactive nav at all

**Unrefuted at the outcome level, and moot as a mechanism — no probed winner has direction-reactive nav to flip.**

The stronger empirical finding: **none of the probed winners uses direction-reactive nav at all.** Live jitter tests (±5–8px alternating scrolls, 14–16 cycles, sampling transform/opacity/class each cycle): Balmoral's `site-header` is permanently fixed (class string never changed through down-2200 / up-330 / jitter); Podium, basement.studio, Meech213, Bucks Sauce — fixed persistent; Locomotive — static header that scrolls away; 21 Hrs On The Moon — no persistent nav. Zero state flips observed anywhere; no teardown or jury note documenting a flickering-nav winner was found.

**What the jitter tests support** is the outcome rather than the mechanism: zero visible hide/show flips under jitter, measurable by the scripted jitter cycles used here; hysteresis or an accumulator is one implementation among others. The winner norm the data shows: in these archetypes the nav is a minimal persistent header, and none of the probed winners adopts direction-reactive hiding at all. **Observed legitimate exceptions: none** — no probed winner flickers.

## 5. One easing family and one gesture metaphor page-wide — refuted at the token level, surviving at the register level

**Holds only in amended form — "one family" is refuted at the token level by three SOTD winners; the register-level version survives.**

Distinct `transition-timing-function` tokens live-counted across all elements:

- **Balmoral** (SOTD): **9 distinct tokens** — linear ×35, quad-out ×22, cubic-inOut ×5, circ-out, expo-out, quad-in, browser `ease`, plus combos. Four mathematical families on one page, from a top studio (MILL3).
- **Podium** (SOTD + Developer Award): 5 tokens — Tailwind's material pair (0.4,0,0.2,1 / 0,0,0.2,1), custom expo-out (0.16,1,0.3,1), browser ease-out — framework defaults coexisting with the signature ease.
- **Bucks Sauce** (SOTD): 4 tokens (Tailwind standard ×37 plus expo-outs and a sharp-in).
- Single-token winners also exist: 21 Hrs On The Moon (exactly one cubic-bezier page-wide), basement.studio (one), Meech213 (browser `ease` only — the default, and it still won).

**The invariant that survives:** no elastic or bouncy curve mixed with strict-mechanical ones on the same page — the measured sets span decelerating, in-out, and sharp-in tokens plus linear for continuous loops, yet none crosses into the elastic register (Thibault Guignand's Codrops breakdown likewise: power2 variants only). The supported form is register-level — no cross-register mixing (playful-elastic vs mechanical-strict vs cinematic-decel) — with token count free. **Gesture-metaphor lineage: could not verify either way** — no observable counter-example, no confirming teardown; unresolved. **Legitimate exception, not observed in the probed set:** a declared narrative register shift (a playful chapter inside a formal site), sustained for the whole chapter. The per-element-class reading of the same norm is in [`interaction-grammars-per-page.md`](./interaction-grammars-per-page.md).

## Could not verify

**basement.studio** measurements are of the current build; its SOTDs were earlier versions — corroboration only, never load-bearing. **Bucks Sauce** image-upscale readings (3.6–5.3×) are almost certainly lazy-load LQIP placeholders caught mid-swap — discarded from the §1 evidence. **CHILE20** is offline; per-world art direction comes from the Awwwards SOTM write-up, and its HUD consistency is unverified. Jury notes and scores never mention nav mechanics or easing tokens — the award-side evidence for §4 and §5 is structurally silent, and live observation was the only available instrument. All live numbers are single-run at one viewport (1440×900 @2x); `srcset` could serve differently at other sizes.

## What the measurements support

§3 holds as stated across everything measured. §4 holds as an outcome but is untested as a mechanism — the winners probed do not use it. §1, §2, and §5 hold only in amended form — winners violate the original phrasings routinely (§1: retina parity → "no visible mush"; §2: film loops belong in the driven set; §5: register-level, not token-level). No observed winner violates the amended forms — the ≥ ~1× CSS floor in §1 stays a recommendation, since two measured winners undercut it.
