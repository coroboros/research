---
title: "The Scrub Fidelity Floor — Frame Density Holds, Pixel Parity Falsified"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "scroll-scrub", "image-sequence", "webgl", "performance", "asset-fidelity"]
sources:
  - "https://css-tricks.com/lets-make-one-of-those-fancy-scrolling-animations-used-on-apple-product-pages/"
  - "https://tympanus.net/codrops/2025/10/16/creating-smooth-scroll-synchronized-animation-for-optikka-from-html5-video-to-frame-sequences/"
  - "https://www.awwwards.com/sites/optikka"
  - "https://www.awwwards.com/siena-film-foundation-case-study.html"
  - "https://www.awwwards.com/sites/siena-film-foundation"
  - "https://tympanus.net/codrops/2026/07/15/the-architecture-behind-trionn-coordinating-gsap-three-js-lenis-and-web-audio/"
  - "https://www.awwwards.com/ribbit-case-study.html"
  - "https://www.itsoffbrand.com/our-work/lando-norris"
  - "https://www.awwwards.com/sites/lando-norris"
  - "https://www.awwwards.com/watches-wonders-immersive-experience-for-cartier.html"
  - "https://www.brad-holmes.co.uk/web-performance-ux/why-most-scroll-animations-miss-what-apple-gets-right/"
---

# The Scrub Fidelity Floor — Frame Density Holds, Pixel Parity Falsified

Frame density holds on every winner measured; pixel parity does not. Scrubbed hero sequences on winning sites turn on those two properties — whether they are dense true sequences, and whether they ship at or above device-pixel render size.

Dense true sequences are confirmed everywhere, with no exception found. "At or above device pixels" is falsified as an absolute: one 2025 Awwwards Site of the Day (SOTD) winner, OPTIKKA, and Apple's own 2019 page ship ~2× upscale at desktop retina.

Measured via curl + sips/ffprobe against the shipped CDNs of apple.com, optikka.com, and siena.film, 2026-07-17. Parent reference: [`../award-winning-websites-2025-2030.md`](../award-winning-websites-2025-2030.md).

## Apple — measured off their CDN

### AirPods Pro 2019, the canonical 148-frame teardown

Frame count 148, JPEG, live URL pattern `…/anim/sequence/large/01-hero-lightpass/{n}.jpg` (documented by CSS-Tricks). Frames downloaded and measured:

| Tier | Measured px (frame 0) | Notes |
|---|---|---|
| small | 400×460 | |
| medium | 800×530 | |
| large | 1458×820 | frame 147 is 1158×770 — frames are content-cropped, dimensions vary |
| large_2x / xlarge | **does not exist** (404) | no retina tier in 2019 |

Apple 2019 upscaled ~2× on a 2880-px retina viewport, mitigated by dark-field product isolation — small luminous earbuds on pure black, not full-bleed photography.

### AirPods Pro 2025 (apple.com/airpods-pro/)

Now **MP4 video scrub with an explicit `_2x` retina tier at every breakpoint** (`…/anim/hero/{tier}.mp4`), measured with ffprobe:

| Asset | Resolution | Frames | fps | Size |
|---|---|---|---|---|
| hero/small.mp4 | 734×800 | 203 | 30 | |
| hero/small_2x.mp4 | 1468×1600 | 203 | 30 | |
| hero/medium.mp4 | 1068×1200 | 225 | 30 | |
| hero/medium_2x.mp4 | 2136×2400 | 225 | 30 | |
| hero/large.mp4 | 1800×1050 | 225 | 30 | 6.05 MB |
| hero/large_2x.mp4 | **3600×2100** | 225 | 30 | 9.43 MB |
| case/large_2x.mp4 | 3456×1824 | 89 | 30 | |

Apple's current answer at desktop retina: **3600×2100 — at or above device pixels (2880×1800), H.264, 225 true frames for one hero section.** Every scrub section (hero, case, fit-feel, connectivity, heart-rate) gets its own dense real sequence.

## Awwwards winners under the hood

**OPTIKKA** — SOTD 2025-06-17, **7.3/10**, by Zajno. The Codrops case study documents **1,182 desktop frames** (880 tablet/mobile) **extracted from real video with FFmpeg at 30 fps**, WebP q80, DPR-aware canvas with cover math, progressive loading (first 10 frames immediately, ±5-frame scroll lookahead). Live frames measured: desktop **1440×832** uniform (14–66 KB each), tablet 1024×1366, mobile **393×852** (1x CSS pixels — a 3× upscale on a 3x phone). They state why they abandoned `<video>` scrub: stuttering, autoplay restrictions, compression fidelity loss.

**Siena Film Foundation** — SOTD 2025-03-18, **7.9/10**, Niccolò Miranda. The hero is **not** a canvas frame scrub — a Three.js WebGL filmstrip slider with Poster/Footage modes, GPU texture compression, channel packing. Source is real film stills and footage: delivered textures measured at **1920×1080** (289 KB WebP) up to **3900×2601** (408 KB WebP), the latter carrying a real camera-roll filename (`BYANYMEANS_2024-04-28_EJA-02511_R1.webp`). At 7.9, imagery ships at or above device-pixel size.

**Lando Norris** — SOTD **8.18/10**, OFF+BRAND: real-time WebGL 3D + Rive motion, real photography galleries, no baked pre-rendered scrub. **Cartier Watches & Wonders** — SOTD multiple years, Immersive Garden: six real-time 3D scenes. High-scoring winners increasingly render live rather than bake frames.

**Trionn** — FWA, CSSDA, others: **371 WebP frames for one section**, `<img>` src swap with 0.12 lerp easing, `requestIdleCallback` preload batches of 20. **Ribbit** — PNG-per-frame from hand-drawn character animation, every frame a distinct drawn sample.

## Counter-examples

**Found — falsifies the device-pixel absolute:** OPTIKKA won SOTD shipping 1440-px-wide frames — 2× retina upscale on desktop, 3× on mobile. How it survived: **continuous 30 fps real footage** (motion correctness dominates), uniform WebP-q80 texture reading as deliberate compression grain, DPR-aware cover draw. It scored **7.3**, the lowest of the scored winners here. Apple 2019 survived ~2× via dark-field isolation — the upscaled region is mostly black. Both mitigations are unavailable to full-bleed photographic cover.

**Not found — the density finding stands:** **no SOTD or Site of the Month (SOTM) winner in this corpus scrubs a sequence synthesized from a handful of stills.** Every documented winner scrubs continuous real source — video extraction (OPTIKKA 1,182), 3D render (Apple 89–225 per section), drawn animation (Ribbit) — or renders real-time 3D (Lando Norris, Cartier). Winners who do build from stills (Siena) animate the full-resolution still live in WebGL/transform space, preserving every source pixel, instead of baking pushes into low-res frames. Absence of a counterexample after targeted searching is not proof of impossibility, but there is no precedent to point to.

**Video-scrub route:** now the dominant pattern at the top. Apple scrubs actual H.264 `<canvas>`-decoded video with a 2x tier (measured above); Brad Holmes describes the industry shift with no hard numbers. OPTIKKA's counter-move (video → frames) was about scrub smoothness on mobile, not source density — their frames still came from real video. Either way the source is always dense real footage; MP4 vs frame files is an implementation choice.

## The floor

1. **Upscale at worst scrub depth.** The two anchors, both at desktop retina: OPTIKKA at 2.0× (1440 source / 2880 device) scored 7.3 — the highest ratio measured on any winner's scrub sequence there, and 3× on a 3x phone; the 7.9 winner (Siena) ships 1920–3900 px, and the current Apple bar is 1.0× or better (3600/2880 = 0.8×, supersampled). Between those, **1.5× is the defensible ceiling for a `7.5+` score, 2.0× the worst shipped at desktop retina, and no measured winner ships source below 1.0× of CSS pixels.**
2. **Minimum source density: every frame is a distinct real sample** (footage frame or render frame); 30 fps extraction is the norm. Smallest true sequence documented in any winner: **89 frames** for one section (Apple case section). Typical hero figures: **148** (Apple 2019), **225** (Apple 2025), **371** (Trionn), **1,182** (OPTIKKA). A sequence synthesized from a handful of stills carries only as many real samples as it has stills — no documented winner ships that. Where only stills exist, the precedented route is Siena's: the full-resolution still animated live (WebGL/transform Ken Burns) rather than baked into a frame sequence.
3. **Within scrubbed sequences, treatment buys back resolution only on non-full-bleed or dark-field content, never on full-bleed photography** — static and film-loop full-bleed imagery is a different economy ([`winner-norms.md`](./winner-norms.md): Depo Luxe ships full-bleed stills at up to 2.81× under grain, grade, and motion). Apple 2019's ~2× survived because the upscaled field is black with a small luminous product; OPTIKKA's 2× survived on continuous-motion **real footage** — 1,182 frames extracted from video with FFmpeg at 30 fps per its Codrops case study — carried by a uniform WebP-q80 texture that reads as deliberate compression grain. The one photographic/film winner measured (Siena) ships 1920–3900 px — its treatment (grain, grade, filmstrip chrome) sits *on top of* full-resolution sources, not in place of them.

## Could not verify

Trionn's frame resolution (Next.js hashed bundles; needs a live browser session) and Ribbit's frame count and resolution — both undisclosed in their case studies. Apple 2019's exact on-page draw scale (contain vs cover behavior of the original canvas) — only delivered frame pixels were measured. Frames-per-scroll-viewport ratios — scroll track lengths unmeasured, so counts are absolute, not per-viewport density. Any jury statement tying resolution to score — the 7.3 (2× upscale) vs 7.9/8.18 (device-pixel or real-time) pattern is 3 datapoints of correlation, not a causal ruling. Lando Norris hero internals — the case study is silent on sequence vs real-time; tagged WebGL + Rive.
