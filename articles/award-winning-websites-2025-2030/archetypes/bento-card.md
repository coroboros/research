---
title: "Bento / Card — Effect Palette, Page Recipe, Mid-Page Aliveness"
date: "2026-07-30"
author: "Coroboros"
tags: ["web-design", "design-archetypes", "bento-grid", "feature-grid", "saas", "css", "tailwind", "motion-design", "scroll-driven-animation", "awwwards", "design-systems"]
sources:
  - "https://animejs.com"
  - "https://www.awwwards.com/sites/anime-js"
  - "https://www.awwwards.com/vote-for-site-of-the-month-may-2025.html"
  - "https://endex.ai/"
  - "https://www.awwwards.com/sites/endex"
  - "https://trymeridian.com/"
  - "https://www.awwwards.com/sites/meridian"
  - "https://www.awwwards.com/sites/apple-airpods-pro"
  - "https://thefwa.com/cases/apple-airpods-pro"
  - "https://www.apple.com/macbook-air/"
  - "https://vercel.com"
  - "https://vercel.com/geist/colors"
  - "https://www.shadcn.io/design/vercel"
  - "https://linear.app"
  - "https://supabase.com/design-system"
  - "https://fountn.design/website/supabase/"
  - "https://bentogrids.com/shots/clt45x72z0002y6nxvxwfaaqx"
  - "https://www.30secondsofcode.org/css/s/mouse-cursor-gradient-tracking/"
  - "https://bholmes.dev/blog/a-shiny-on-hover-effect-that-follows-your-mouse-css/"
  - "https://tympanus.net/codrops/2025/05/27/animated-product-grid-preview-with-gsap-clip-path/"
  - "https://tympanus.net/codrops/2025/06/03/elastic-grid-scroll-creating-lag-based-layout-animations-with-gsap-scrollsmoother/"
  - "https://tympanus.net/codrops/2026/03/02/sticky-grid-scroll-building-a-scroll-driven-animated-grid/"
  - "https://cuberto.com/"
  - "https://www.joshwcomeau.com/css/backdrop-filter/"
  - "https://www.superdesign.dev/styles/bento-grid"
  - "https://effect-labs.com/en/pages/blog/bento-grid-layouts.html"
  - "https://family.co/"
---

# Bento / Card — Effect Palette, Page Recipe, Mid-Page Aliveness

Bento is a *section* pattern (feature grid, product overview), and no award-anchored winner opens on a card grid. The 2025 winners lean editorial rather than toward a saturated tile wall, the bento-fatigue correction visible in the work; jury scores on the line run 7.62–8.05 overall. Effect palette, page recipe, and mid-page aliveness for the bento / card archetype. Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

## Corpus

Whole-site bento award winners are rare, so the awarded evidence concentrates in a few hard-awarded whole sites plus feature-grid sections inside design-canonical product pages.

Evidence tags: `(winner-verified)` = read from the awarded site's live CSS, JS, or DOM; `(shipped)` = observed live or in award-page media, implementation not read; `(technique)` = a documented method, typically Codrops; `(design-canonical)` = a documented design system with no verified award; `(single-source)` = one site only; `[CSS]` / `[JS]` = quoted from shipped code; **verified** / **stated** / **observed** = measured in source / claimed by the builder / seen but not read; `(stated, unconfirmed)` = a builder claim the source read could not confirm; `(inferred)` = derived from indirect evidence.

| Site | Award | Jury | Notable sub-scores | Role | Depth |
|---|---|---|---|---|---|
| **Anime.js v4** (`animejs.com`) | Awwwards **Site of the Day (SOTD) 6 May 2025** + Site of the Month May 2025 + Developer and Product honors | **7.62** — Design 7.63 / Usability 7.51 / Creativity 7.75 / Content 7.63 | Dev Award 7.84 · **Animations/Transitions 9.00** · Responsive 8.00 · WPO 7.80 · Semantics-SEO 7.40 · Accessibility 7.40 · Markup 7.40 | Anchor. Brutalist-bento hybrid, motion-brand pole | live CSS + JS + DOM |
| **Meridian** (`trymeridian.com`) | Awwwards **Honorable Mention 7 Nov 2025** | **8.05** — Design 8.20 / Usability 7.93 / Creativity 8.00 / Content 7.87 | tags Webflow, GSAP, WebGL, 3D, Microinteractions | The line's highest overall jury; ambient-decor middle | live CSS + JS + DOM |
| **Endex** (`endex.ai`) | Awwwards **Honorable Mention 24 Mar 2025** | **7.91** — Design 7.93 / **Usability 8.27** / Creativity 7.27 / Content 8.07 | — | Editorial-restraint pole | live CSS + DOM |
| **Apple — AirPods Pro / MacBook Air** | Awwwards SOTD + FWA for the AirPods Pro scroll-sequence page; the *product* pages carry the canonical bento sections, award-unverified | — | — | Structural-pure bento reference | rendered content |
| **Vercel** | No verified SOTD — design-canonical, Geist system | — | — | Monochrome feature-grid / border-shine | live markup |
| **Supabase** | No verified SOTD — design-canonical | — | — | Dark + emerald dev bento; spotlight/glow | documented |
| **Linear** | No verified SOTD — design-canonical | — | — | Structural-pure feature grid | rendered content |
| **Family** (`family.co`) | **Apple Design Award for the app, not a web award** — reference only | — | — | Card-physics / shared-element reference | reference |

Awwwards Honorable Mention panels grow as jurors keep adding notes, so any single decimal is a moving snapshot. Figures above read from the rendered jury grid on 13 Jul 2026, per-juror cells summed by hand.

**Evidence base.** Awwwards Honorable Mention pages serve only an SPA shell to `curl`, so sub-scores were column-averaged from each juror's four integer sub-scores in the rendered jury grid.

Anime.js's Awwwards entry lists its palette as `#252423` / `#DAD5D0`.

Technique references, cited for method rather than for an award: Codrops GSAP breakdowns (product-grid preview, elastic grid scroll, sticky grid scroll), Cuberto (Awwwards SOTD 22 Jun 2018, live-read here only for the easing vocabulary `cubic-bezier(0.16,1,0.3,1)`, `cubic-bezier(0.19,1,0.22,1)`, and spring `cubic-bezier(0.34,5.56,0.64,1)`), the documented Vercel border-hover recreation.

### The score reality

Award winners cap at **7.62–8.05 overall jury**. The standout numbers on this line are always sub-scores: Anime.js Animations/Transitions 9.00, Endex Usability 8.27 and Content 8.07. This is the bento-fatigue ceiling, confirmed in the scores.

## Effect palette

### Hover and micro-interactions

#### Buttons and CTAs

The AI-default: every button gets the same pale wash, `background: color-mix(accent 10%, transparent)` fading in over `0.3s ease`, a washed-out tint reading as a disabled state, shipped identically on primary, secondary, and ghost. No winner examined does this.

- **Ghost outline plus transform-press.** The border stays a hairline (`1px solid` at a mid-neutral token, Anime.js `#625d5b` on a `#252423` ground) and **the background never fills**. The only animated property is `transform`, a sub-pixel press. Anime.js `.ui-button`: `border:1px solid var(--hex-fg-5)`, `border-radius:var(--br-s)`, `transition:transform .125s ease-out`, `font-weight:600`, `color:var(--hex-fg-4)`; on hover, `color:var(--hex-fg-3); border:1px solid var(--hex-fg-4)`. *When:* brutalist-bento and dev-tool grids where restraint is the brand `(winner-verified)`.
- **Token-step solid or inversion.** The primary CTA is already a solid fill; hover advances one deliberate step through the ramp (Vercel/Geist: Background → Color1 hover → Color2 active) or inverts foreground and background. A full token change with a crisp ~0.15s transition, pill geometry (`border-radius: 100px`). Anime.js `.ui-primary` is `background-color:var(--hex-red-5)`, `color:var(--hex-red-1)`, `border:none`. ≥2 sources.
- **Trailing-icon shift.** The label holds while an arrow or chevron nudges ~4px on the x-axis over `0.2s`. Pairs with either style above. `(single-source)`.

Winners animate geometry or a full token, never a pale translucent fill.

#### Text links

- **Underline draw.** A pseudo-element underline scales in from `scaleX(0)→1`, transform-origin left, ~`0.3s` with an expo-out ease. Cuberto live (`span::after { transform: scaleX(1) }`), `(single-source for the exact mechanism)`, though underline-draw itself is near-universal.
- **Neutral→foreground brighten.** Inline and nav links sit at a muted neutral (Anime.js `.text-ui` at `#b4b1af`, i.e. `--fg-3`) and lift to `--fg-1` on hover, no underline `(winner-verified)`.

#### Images and cards

The AI-default is one universal card hover: `transform: translateY(-4px) scale(1.02)` plus a gray `box-shadow` drop and maybe a `border-color` to accent, `0.3s ease`, every tile identical. This flattens the grid into one repeated gesture.

- **Cursor-tracked border-shine.** A conic gradient sits in the border via `mask` plus `mask-composite: intersect`; JS updates `--x` / `--y` on `mousemove` (and a `--start` angle) so a light streak rides the card edge under the pointer. Neighboring cards can share the listener so their borders faintly answer. *When:* dark dev and SaaS grids where the card is a flat panel, not a photo. Vercel border-hover plus Supabase cursor-aware glow `(design-canonical)`. ≥2.
- **Spotlight expand plus content reveal.** The hovered tile expands across its row, siblings reflow, a desaturated preview restores to color, heading and supporting copy fade up. Layout-aware, not a scale. *Codrops parameters, verified from the tutorial:* a paused GSAP timeline, `ease: power2.inOut`; sibling cards shift `2.5vw` inward (even→right, odd→left, top→down, bottom→up); a 12-point clip-path cross morphs open; the preview scales `(dim − 5vw)/dim`. `(technique)`.
- **Border-glow bloom.** A blurred accent gradient in a pseudo-element behind the card fades in on hover (`opacity 0→1`), reading as a soft under-glow rather than a hard shadow. The accent is the tile's own OKLCH token, not a global gray. *When:* dark grounds (`--bg` around `#0A0A0F`) where glow reads. Supabase plus Linear spotlight-card lineage `(design-canonical)`. ≥2.
- **Live-demo response, no lift at all.** The tile is a running canvas or WebGL demo; hover and drag drive the *actual* animation, so there is no card-chrome hover; the content reacts. Anime.js ships 6 canvases; every feature tile demonstrates the primitive it documents. `(winner-verified, single-source)`, and it is the anchor.
- **Tilt (perspective follow).** Pointer position drives a small `rotateX` / `rotateY` (≤6–8°) via motion values outside the React render cycle. Named in the standard bento affordance set alongside spotlight and border glow, but amplitude was never verified on a live winner. `(observed)`. Single hero tile only; tilting every tile is noise.

**The rule these encode:** pick one hover affordance per grid (border-shine, spotlight, glow, or live-demo) and let the tiles differ by content, not by each inventing its own motion.

#### Nav items

The AI-default: links get the pale-fill pill on hover.

- **Nav-item hover is a brighten, not a fill.** Items are muted-neutral text lifting to full foreground; no background pill. Anime.js `.main-nav-link` at `#b4b1af` `(winner-verified)`.

#### The nav bar

The AI-default: the bar turns frosted glass on scroll **and hangs a contrasting-colored `border-bottom`**. No winner examined hangs a differently-colored border under the nav; it is a template tell.

- **Transparent overlay, no scroll surface.** The header stays fully transparent over a consistent ground at every scroll position. Anime.js's 72px header reads `background: rgba(0,0,0,0)`, `backdrop-filter: none`, `border-bottom: 0`, `box-shadow: none` at the top *and* scrolled 800px, live-verified unchanged. Works because the page ground is one flat color. `(winner-verified)`
- **Transparent → frosted hairline on scroll.** Transparent at the top, then on scroll the bar gains `backdrop-filter: blur()` over a semi-opaque surface and a **same-family hairline** border (`rgba(255,255,255,0.06)` dark, `rgba(0,0,0,0.05)` light), never a contrasting accent line. Apple plus Vercel, documented. ≥2.

### Motion and scroll

The AI-default: `AOS`-style fade-up on every element with `data-aos-delay` incrementing per card, plus a full-page hero parallax. Uniform, heavy, and the parallax is on the archetype's own anti-pattern list.

- **Staggered card entrance.** Tiles reveal on scroll-in with `opacity 0→1` plus a short `translateY` of 16–24px, staggered 40–80ms per tile. The distance stays small; bento reveals settle rather than fly. *Parameters from technique references:* GSAP `power2.inOut`; expo-out `cubic-bezier(0.16, 1, 0.3, 1)` (Cuberto live) for a decisive settle; micro-transitions land near `0.125–0.3s`, section reveals `0.6–1.2s`.
- **Lag-based / elastic grid scroll.** Columns scroll at differential speeds (center faster, edges trailing) via GSAP ScrollSmoother, giving a soft physical drift instead of parallax on a layer. *When:* image-dense tile walls; a fresher substitute for hero parallax. `(technique, single-source)`.
- **Sticky pinned scrub for one hero tile.** Pin a single feature tile and scrub its internal state to scroll. Restraint matters: pin *one* tile, not the grid. `(technique, single-source)`.
- **Perpetual internal loop.** Each tile owns one infinite micro-loop (typewriter, pulse, carousel, shimmer), memoized and isolated. Motion *inside* tiles rather than on scroll, and what makes the grid feel alive without a scroll gimmick. Corroborated by Supabase's per-tile animated cursor and node diagrams.

Winners keep parallax minimal or trade it for lag-scroll. Heavy hero parallax is an anti-signal here.

### Text effects

- **Per-char / per-word stagger, signature only when motion is the brand.** The display headline splits and staggers in. This is literally Anime.js's product, so it earns pride of place; elsewhere it is over-reach. `(winner-verified, signature-gated)`.
- **Tight-tracked static display, the supporting default.** A large sentence-case headline at weight 600 with negative tracking (Vercel: `-2.4px`, `tracking-tight`), no animation beyond the section reveal. Type as a calm anchor for busy tiles. ≥2.
- **Mono eyebrow plus tabular metrics.** Eyebrow labels and in-tile numbers in a monospace (Geist Mono, JetBrains Mono) with `font-variant-numeric: tabular-nums`; numbers can count up on reveal. The typographic *register shift* per tile (one serif, one mono metric) is the effect: variance signals each tile is its own world.

Kinetic per-char is signature and gated to motion brands. For everyone else type is supporting: tight tracking plus mono metrics carry it, and animating the headline is the tell.

### Cursor and pointer

The AI-default: a global custom cursor, a big lagging dot or ring replacing the native pointer sitewide plus a hover-to-grow blob. Wrong archetype: bento is scan-and-click, and a laggy dot fights fast card scanning.

- **Default cursor, deliberately.** `body { cursor: auto }`; the native pointer is kept because the grid is meant to be scanned and clicked. Anime.js is `cursor: auto` globally `(winner-verified)`.
- **Contextual custom cursor, demo-scoped only.** A custom cursor appears *only* inside an interactive demo tile (Anime.js `.scroll-cursor` / `.scroll-cursor-ghost` for its scrub and drag demo), never sitewide `(winner-verified, single-source)`.
- **Pointer drives a surface, not a replacement.** The pointer feeds `--x` / `--y` into a card's border-shine or spotlight glow; the cursor itself stays native. ≥2.

In bento the pointer powers effects on surfaces; it is not itself dressed up.

### Loader effects

- **Instant first paint, animate in place.** No preloader element (Anime.js has no `loader`, `preload`, `intro`, or `splash` node in the DOM, live-verified), and the hero and tiles animate in *after* paint. `(winner-verified)`
- **Staggered self-reveal as the intro.** The entrance *is* the card stagger, so the page assembles itself rather than gating behind a curtain.
- **Hero-demo autoplay.** If one tile is a live demo, it starts playing on load as the focal motion (the Anime.js rainbow visualization across its 6 canvases), reading as an intro without being a preloader `(winner-verified, single-source)`.

A blocking preloader is an anti-signal for this archetype; it belongs to the immersive and WebGL lines.

### Composition

**Anime.js v4: "everything is a live demo of motion, framed by restraint."**

| Element | Interaction | Verification |
|---|---|---|
| Button | Ghost outline, no fill, `transform` press `0.125s ease-out`, 4px radius | live |
| Text link | Muted `--fg-3 #b4b1af` → `--fg-1` brighten, `transition: all` | live |
| Card | Live canvas demo — hover and drag drive the actual animation, no card-chrome lift | live (6 canvases) |
| Nav bar | Transparent overlay, no background, blur, border, or shadow; unchanged on scroll | live |
| Cursor | Native globally; custom `.scroll-cursor` only inside the scrub demo | live |

Every element expresses the same idea, motion, at a different scale. The button presses, the link brightens, the tile animates, the type staggers, the demo scrubs; all are anime.js primitives. The unifying frame is warm-neutral brutalist restraint: a single ground `#252423`, off-white `#f6f4f2`, small radii 2–12px, and a 17-hue accent ramp used one accent per tile. Variety is content-level, not gesture-level. Nothing is decorated; everything is demonstrated.

**Vercel** `(design-canonical, no verified award)`: one material idea, light catching an edge, recurs at every scale (the conic-gradient border-shine tracking `--x` / `--y` on cards, the same glint on the solid pill CTA, a transparent-to-frosted nav with a same-family hairline, a native pointer feeding the shine) inside monochrome Geist precision (Ink `#171717`, tight `-2.4px` tracking, mono eyebrows, stacked shadows over heavy drops), so the light motif is the only warm event.

**The transferable rule.** Cohesion comes from a shared through-line (Anime.js: *motion*; Vercel: *edge-light*), not from repeating one gesture. Each element class carries its own mechanism, all of them tied to one idea. One pale-fill hover on every button plus one frosted-hairline nav everywhere has no through-line; it is sameness mistaken for consistency.

### Anti-signals — absent from every winner examined

- **Washed-out pale-tint button fill** (accent at ~10% alpha, fading in).
- **Contrasting-colored `border-bottom` under the nav bar.** Winners' nav borders, where they exist at all, are same-family hairlines; the anchor has none.
- **One universal card hover** (`translateY(-4px)` plus `scale(1.02)` plus gray drop-shadow) applied to every tile.
- **Global custom cursor.** Custom cursors are demo-scoped only.
- **Blocking preloader curtain** with a percentage counter on a content-first grid.
- **Per-letter kinetic headline on a non-motion brand.**
- **Heavy hero parallax.** On the archetype's own anti-pattern list.
- **Uniform fade-up-on-everything** with linear per-element delays.

## Page recipe

Three named shapes cover the line. Only the first is anchored on a whole-site award; the other two are the shipped canon.

### Named page shapes

#### Shape A — Pinned demo reel (Anime.js, winner-verified)

**Fingerprint.** One dark ground (`#252423`) held for the whole scroll. The page opens on a left-copy / right-demo hero, drops into one big central capability grid, then hands off to a run of full-viewport panels, each `height: 100lvh`, its copy `position: fixed; opacity: 0` and cross-fading on scroll, while a single persistent live demo runs and proves the heading. The bento *grid* of asymmetric tiles lives in the toolbox and modules sections; the feature gallery between them is a pinned reel, not a scrollable tile wall. It closes on a bundle-size stat, a sponsor wall, a get-started CTA, and a newsletter footer, and assembles itself with no loader.

**Ordered skeleton**, verbatim `id` / `data-label` from the DOM, intensity in brackets. Intensity `[n]` is a comparative 1–10 estimate of attention load (defined in [Composition Chains](../winners/composition-chains.md)).

1. `intro` / HEADING: hero, "All-in-one animation engine." · attention · display type with micro-animated accents · [8] · seam: scroll into a light-inverted panel.
2. `toolbox` / TOOLBOX: "The complete animator's toolbox" (`home-section-light`) · understanding · central capability visualization · [7] · seam: enters the pinned gallery.
3. `features-gallery` / FEATURES wrapping 8 pinned panels: `intuitive` "Intuitive API", `composition` "Enhanced transforms", `scroll` "Scroll Observer", `staggering` "Advanced staggering", `svgUtils` "SVG toolset", `draggable` "Springs and draggable", `clockwork` "Runs like clockwork", `responsive` "Responsive animations" · proof · one live demo per panel, copy cross-fades · [9, climax] · seam: ground returns to a light stat panel.
4. `modules` / MODULES: "A lightweight and modular API" with `Bundle size` `<span class="size">24.50</span> KB` · proof · bento stat tiles · [6].
5. `sponsors` / SPONSORS: "Our sponsors" · trust · sponsor logo wall · [4, rest].
6. `get-started` / GET_STARTED: "Start animating" · close · `Getting started` button over `npm i animejs` · [6].
7. `site-footer`: newsletter "Stay in the loop" plus sponsor block, link columns, "© 2026 Julian Garnier" · chrome · [3].

**Totals.** Roughly 14 addressable sections; scroll length 12–16 viewport-heights, since the 8 gallery panels each pin at `100lvh`. Climax is the pinned feature gallery, the draggable and scroll-observer panels. Rest is sponsors into footer.

**Fits.** Dev tools, animation and motion engines, any product where the demo *is* the pitch.

#### Shape B — Highlights bento plus deep-dive scroll (Apple, shipped)

**Fingerprint.** A product-render hero with a poetic tagline, then a compact "Get the highlights" bento tile group summarizing six claims in one screen, then a long alternating run of full-bleed deep-dive sections, one per theme, each with its own render-on-gradient, then a chooser, accessory and commerce cards, and the Apple mega-footer. The bento is the *summary layer*; the rest is linear long-form.

**Ordered skeleton.** `hero ("MacBook Air" / "Might takes flight." / "Now supercharged by M5.") → "Get the highlights." (6-tile bento) → Design → Performance ("M5. The chip that zips.") → comparison tiles → AI → macOS → Continuity → Display ("Love at every sight.") → Camera & Audio → Ports → Security ("Peace of mind at your fingertip.") → upgrade/chooser → Accessories / Trade In / Card / Education cards → environment → mega-footer`. The six highlight tiles carry distinct `overview-highlights-*` stems: ai, battery, continuity, mx, spotlight, storage.

**Totals.** 40+ headings; the bento is one screen inside a 30-plus-viewport scroll, climax diffuse across per-theme reveals. **Fits.** Hardware launches, multi-capability products, marketing pages with a summary-then-detail contract.

#### Shape C — Editorial 12-column feature grid (Endex verified; Vercel and Linear shipped)

**Fingerprint.** A dark hero with one oversized display H1, a one-line subhead, and a dual CTA, then a divided capability strip (a horizontal `divide-x` row of capability labels, marquee-scrolling on mobile), then a **12-column** grid (`lg:grid-cols-12`) of feature cards mixing wide and tall spans, each carrying a slice of product UI rather than an illustration, then enterprise and security proof, a CTA band, and a compact link-column footer. The editorial descendant of bento: a 12-column manuscript grid, not a saturated tile wall.

**Ordered skeleton (Endex, verbatim).** `hero "AI Built For Excel" → capability strip "Trace References · Sheet Navigation · Data Sources · Formatting · Deep Research · Memories · LLM Integrations · Undo · Conversion" → "Enterprise Deployments at the World's Largest Firms" → "Auditable from Start to Finish" → "LLMs engineered for finance" → "Reason over all of your data" → "Built for Power" → "Teams" → "Endex integrates natively with internal data and external sources" → "Enterprise-grade security" → "Hire your AI Excel Agent" (CTA close) → compact footer`.

**Fits.** SaaS, AI products, dev platforms, enterprise tools with many small capabilities to index.

### Hero architectures

**Left-copy / right-demo split (Anime.js, winner-verified).**

- The visible display heading is an `<h2>`, not the `<h1>`: `<h1 class="heading-logo header-logo">` is the wordmark, so the SEO H1 and the visual hero heading are different elements.
- The heading sits top-left at `#intro .home-section-text h2{font-size:var(--text-xxxxl)}`, the largest step, three lines split with `<br>` ("All-in-one / animation / engine") and a `<span class="animation-engine red-dot">.</span>` as the terminal period. The heading measures 432px from the left edge, against an animated circular SVG demo on the right.
- Subhead below in body DIN; the install command `npm i animejs` in a `<pre class="npm-install">` plus a `.learn-more` ghost button.
- Nav is a transparent sticky overlay (`#site-header{background-color:transparent;position:relative}` at desktop over a base `position:sticky`) with a same-family hairline on `#site-header-content`: `border-bottom:1px solid var(--hex-bg-4)` (`#353433`). Items are muted `--hex-fg-3` brightening to `--hex-fg-1` when active. The red `:before` pill belongs to the **Sponsor** button: `#site-menu sponsor-button .main-nav-link:before{background-color:var(--hex-red-6);border-radius:var(--br-s)}`.

| Element | Order | Transform | Duration | Easing |
|---|---|---|---|---|
| Headline chars | 1 | stagger opacity/translate | per-char | anime.js default |
| Red-dot period | 2 | color/scale loop | perpetual | — |
| "the web" accent | 3 | text swap loop | perpetual | — |

These beats are the intro; there is no loader. Exact per-element durations were never read from the JS `(shipped)`.

**Centered display over dark, UI below (Endex, winner-verified).** H1 "AI Built For Excel" at `text-[48px] leading-[0.92] text-white sm:text-[56px] md:text-[88px]`, a tight-leading oversized display on dark. One-line subhead, "An Excel-native AI Agent that accelerates financial modeling and data analysis". Dual CTA ("Request Demo" primary, "Join Waitlist"), a `pointer-events-none` decorative layer behind, then a product screenshot and the divided capability strip. No loader; server-rendered text paints instantly.

**Product-render tagline stack (Apple, shipped).** H1 is the product name (`<h1 class="header-eyebrow …">MacBook Air</h1>`), a two-to-four-word poetic tagline directly under it, then a spec line. Media is a product render on an unbroken studio gradient; the bento is the first content beat after the fold.

### Loader and intro

The line pattern is instant first paint; the reveals *are* the intro.

- **Anime.js ships no preloader** `(winner-verified)`. The initial HTML has zero loader, splash, or curtain element; one `styles.css?v=4.4.1` and one `scripts.js?v=4.4.1`, plus async analytics. The hero headline stagger and the perpetual red-dot and "the web" micro-animations are the entire intro.
- **Endex** `(winner-verified)`. Next.js SSR delivers the hero copy in the initial HTML (3.8k visible characters server-rendered) with no blocking curtain; content is present before hydration.

A blocking `0→100%` counter curtain is an anti-signal for this line.

### Route transitions

Not a defining feature. The award-anchored surfaces are single-page long-scroll, so there is no route to transition between on the marketing page. Multi-page members use standard framework navigation, not a signature curtain that rhymes with a loader `(observed)`. An elaborate loader-rhyming route curtain reads as out of character; the anatomy is one continuous scroll.

### Copy voice

**Anime.js** `(winner-verified)`: H1 `All-in-one animation engine.` · subhead `A fast and flexible JavaScript library to animate the web.` · sections `The complete animator's toolbox` · `Springs and draggable` · `Runs like clockwork` · body `Break free from browser limitations and animate anything on the web with a single API.` and `Drag, snap, flick and throw HTML elements with the fully-featured Draggable API.` · CTA `Learn more` · close `Start animating` / `Get started quickly with our in-depth documentation.` · microcopy `Stay in the loop` · footer `© 2026 Julian Garnier`. The subhead's final "the web" is an animated text-swap span (a live render showed it reading "CSS"), so the quoted sentence is the HTML base value.

**Endex** `(winner-verified)`: H1 `AI Built For Excel` · subhead `An Excel-native AI Agent that accelerates financial modeling and data analysis` · sections `Auditable from Start to Finish` · `LLMs engineered for finance` · `Reason over all of your data` · CTA `Request Demo` / `Join Waitlist` · close `Hire your AI Excel Agent` · footer `Endex 2026. All Rights Reserved`.

**Apple** `(shipped)`: `MacBook Air` · `Might takes flight.` · `Now supercharged by M5.` · `Get the highlights.` · `M5. The chip that zips.` · `Love at every sight.` · `Peace of mind at your fingertip.` Three of these ship with `&nbsp;` or `<br>` inside.

**Vercel** `(shipped)`: `Recently shipped` · `Built by you, or your agents` · CTA `Deploy` / `Get a Demo`.

**Linear** `(shipped)`: subhead `Purpose-built for planning and building products. Designed for the AI era.` · sections `Make product operations self-driving` · `Built for the future. Available today.` · footer tagline `Linear – The system for product development` (en-dash).

**Voice formula.** Product-as-subject declaratives with an occasional second-person imperative ("Start animating", "Hire your AI Excel Agent"); never first-person "I", never "we" in headlines. The hero is a noun phrase or a claim of seven words or fewer; the subhead is exactly one sentence naming what it is and who it is for; section headings run two to six words. Verbs stay cool and competent (animate, accelerate, reason, ship, plan, build, audit), with Apple warming it through compressed poetry. The terminal period on a fragment headline is a house tic, and on Anime.js the period is literally the animated red-dot accent; Endex and Linear drop it. No exclamation marks anywhere. The line refuses hype adjectives and marketing throat-clearing: it states the capability and stops.

### Imagery art direction

The asset *is* the product surface: no stock photography, no human portraits.

- **Subject.** A live demo (Anime.js canvas and WebGL), product UI (Endex Excel-agent screenshots, Linear app frames), or a product render (Apple hardware). Anime.js ships no non-logo, non-icon `<img>`; Endex ships no portrait-alt `<img>`.
- **Crop, light, grade.** Neutral and true-to-UI. A dark neutral ground held page-wide (Anime.js `#252423`; Endex dark hero with `bg-white` only on the capability strip). Apple is the deliberate split: each highlight cell gets its own render-on-gradient or photographic background while the structural rhythm (radius, gutter) holds.
- **Treatment call.** One treatment page-wide for the dark grids; deliberately split per cell for the Apple structural bento.

### Footer

The norm is functional link-column chrome. The designed moment, where it appears, is a wordmark or tagline reprise or a newsletter capture, never a spectacle.

- **Anime.js** `(winner-verified)`. `<footer id="site-footer" data-color="fg">` carrying a Platinum sponsors block (sponsor logos plus "Become a sponsor"), a Site column (Home / Documentation / Easings editor / Learn), a Socials column (X / Bluesky / GitHub / CodePen), a "Stay in the loop" newsletter capture, and "© 2026 Julian Garnier". Sponsor-first, newsletter-second: a values statement, not just chrome.
  - **CSS-level recipe.** General footer links fill instantly on hover in monochrome: `.links-list li a:hover{color:var(--hex-current-1);background-color:var(--hex-current-7)}` with `transition-duration:0s`; inside the footer's `data-color="fg"` scope, `--hex-current-1` and `-7` resolve to `--hex-fg-1` and `--hex-fg-7`. The red variant is scoped to the Sponsor link alone (`.links-list li sponsor-button a:hover` → `--hex-red-1` on `--hex-red-6`). The trailing arrow nudges on hover: `a:hover .icon{transform:translate(.125rem)}`.
- **Endex** `(winner-verified)`. Compact three-column legal and contact (Security / Legal / Contact) plus "Endex 2026. All Rights Reserved" and LinkedIn / X. Pure functional.
- **Apple** `(shipped)`. A mega functional link farm: Shop and Learn, Account, Entertainment, Apple Store, For Business/Education/Government, Apple Values, legal.
- **Linear** `(shipped)`. Link columns closing on an oversized wordmark and tagline reprise.

### Spectacle menu

The Anime.js pinned feature gallery `(winner-verified structure; motion shipped)`.

- **Trigger.** Scroll into any of the 8 `feature-section` panels, each `height:100lvh` and pinned.
- **Beats.** The panel's copy is `position:fixed; opacity:0` and cross-fades in as the section enters view, `.feature-section.is-in-view{pointer-events:auto;z-index:1}` flipping interaction on; one persistent live demo runs full-viewport behind it and executes the exact claim in the heading: the "Springs and draggable" panel really does drag, snap, flick, and throw; the "Scroll Observer" panel scrubs to the scroll position; the "Advanced staggering" panel staggers on cue.
- **Payoff.** The demo proves the heading in real time. Describing is replaced by doing.
- **Replayable** because it is interactive and the demos loop; the exact moment can be re-driven without a reload.

Runner-up `(shipped)`: Apple's scroll-scrubbed "Get the highlights" tile reveals.

### Named tokens

**Anime.js** `(winner-verified, from styles.css?v=4.4.1)`:

```css
--hex-bg-1: #252423;   /* ground */
--hex-bg-4: #353433;   /* header hairline */
--hex-fg-1: #f6f4f2;  --hex-fg-3: #b4b1af;  --hex-fg-5: #625d5b;
--hex-red-1: #ff4b4b;
--br-s: .25rem;  --br-m: .5rem;  --br-l: .75rem;   /* br-l used exactly 14× */
--font-body: "DIN";   /* font-variation-settings: "wdth" 125 */
--font-code: "Mono";  /* Digital-7 for the clockwork counter */
```

**Endex** `(winner-verified)`: hero H1 `text-[48px] leading-[0.92] sm:text-[56px] md:text-[88px] text-white`; feature grid container `lg:grid lg:grid-cols-12`; capability strip `flex justify-between divide-x overflow-x-scroll whitespace-nowrap border-y bg-white lg:overflow-hidden`.

### Page-level anti-signals

- **No winner opens on a card grid.** Both award-anchored winners open on a copy-led hero (display headline, subhead, CTA) and only then descend into tiles. The grid is a middle-of-page proof layer, never the first fold.
- **No blocking loader.**
- **No signature route curtain.**
- **No stock photography or human portraits.**
- **No uniform tile treatment.** Award-worthy grids vary card spans dramatically and give each tile its own register. "Three equal cards in a row" plus one universal hover-lift are the flattening failures.
- **No exclamation, no hype adjectives.**
- **The 2025 winners lean editorial, not saturated-bento.** Endex uses a 12-column manuscript grid and a divided capability strip rather than a tile wall: the bento-fatigue correction, visible in the work.

## Mid-page aliveness

What keeps the prose and content zone between hero and footer alive, where merely-good bento builds get praise on hero and image reveals and then read dead.

### The fix is not kinetic prose

Where the middle stays alive it is carried by one of **three non-text engines**, never by animated headings or scroll-scrubbed paragraphs:

1. **Live looping product demos welded to a pinned scroll reel.** The demo *is* the mid-page (Anime.js).
2. **Ambient perpetual objects.** A WebGL sphere, a footer globe, logo marquees, a drag-parallax slider (Meridian).
3. **Real product-UI slices as content plus near-zero decor.** Editorial restraint that scores on Content and Usability rather than motion (Endex).

Hover on non-link text (headings, prose, numbers) is effectively absent across the entire tier, and smooth-scroll inertia is absent across the entire tier. Both are findings, not gaps.

### Inventory by site

**Anime.js v4: the demo is the middle** `(winner-verified)`. After the hero the homepage is eight `feature-section` panels, each `height:100lvh`, each with a persistent demo layer `.fixed-section{opacity:.001; position:fixed; will-change:opacity}`. As scroll advances, one panel's copy cross-fades out while the next fades in, and a single persistent demo canvas cross-fades between capabilities. The mid-page is a pinned demo reel, not prose with pictures.

- **Per-section page recolor.** Each panel carries a `color-*` class: `color-getting-started`, `color-animation`, `color-turquoise`, `color-utils`, `color-svg`, `color-draggable`, `color-timeline`, `color-green`. The JS rebinds the page-wide `--hex-current-1…8` token ramp per section (13 `hex-current` sets in the bundle), so buttons, links, the scroll cursor, and the demo all shift hue on entry. The section transition *is* a theme swap, not a slide.
- **Copy cross-fade, scroll-synced.** `.feature-section .home-section-text{opacity:0;position:fixed;top:var(--margin-s)}`; the paragraph is pinned and its opacity driven by scroll progress through the anime.js ScrollObserver. The prose rides the scrubber rather than fading up once. The base `.home-section-text` is `position:relative`; the `.feature-section` descendant carries the override.
- **Scroll-linked divider draw.** `.feature-section ul.feature-links{--scaleX: 0}` with `ul.feature-links:before{max-width:16rem; transform:scaleX(var(--scaleX)); transform-origin:0 0}`, a hairline that draws left to right as the panel enters.
- **Looping demo machines.** Demos default to `loop:true` (26 occurrences in the bundle, on objects keyed by `id`, e.g. `id: "draggable-meshes-rotate"`); when `.feature-section.is-in-view`, `pointer-events:auto` lets the visitor grab, drag, and throw the Draggable panel and re-run it. Perpetual and interactive.
- **Custom scroll-progress cursor.** `.scroll-cursor{width:3px; background-color:var(--hex-red-1); will-change:transform}` with a trailing `.scroll-cursor-ghost` on `--hex-red-2`, riding a `.scroll-bar` track built from a repeating 1px `linear-gradient`.
- **Hero idle loop.** `<span class="animation-engine red-dot">.</span>` with `#intro .home-section-text .red-dot .char{opacity:1!important}`; the headline is split into `.char` spans and the period is a char held visible while it pulses color and scale forever.
- **Motion budget.** Zero `@keyframes` and zero CSS `animation:` in the stylesheet; all motion is JS. Transitions are micro only: `transition:transform .125s ease-out`, `transition:color .05s cubic-bezier(.5,0,.5,1),background-color .05s cubic-bezier(.5,0,.5,1)`, and `transition-duration:0s` five times.

**Meridian: ambient objects, native scroll** `(winner-verified)`. A Refokus/Webflow build whose mid-page is kept alive by perpetual ambient geometry and drag-parallax, not by the cards animating. Stack: Webflow + Refokus + Swiper 11 + jQuery; the CSS ships only `@keyframes spin`, 13 `:hover` rules, and 32 `transition*` declarations (24 of them `transition:` shorthands).

- **Hero WebGL sphere.** `home_hero_sphere_canvas` plus `_highlight` and `_background`, a canvas globe with idle rotation; `canvas` appears 218× across the JS chunks.
- **Footer globe.** `footer_globe_wrap` / `_lines` / `_img`, a second ambient sphere closing the page.
- **Marquees.** `logos-marquee_track`, `marquee_component`, `nav_banner_marquee_inner`. The idle horizontal motion is the low-key "always something moving".
- **Drag-parallax case-study slider.** Swiper 11 with `data-swiper-parallax-x` on 12 slide layers.
- **Feature bento cards.** `home_feat_content_card` ×6 over `bg-with-sphere`, `bg-gradient-sphere-grey`, and `bg-dashed-lines` variants, three each. The tile *background* carries the visual life; the tile chrome stays still.
- **Reveal-on-enter via custom IntersectionObserver.** No Webflow IX2 (`data-w-id` = 0); Refokus ships its own framework with `data-animation`, `data-delay`, `data-hover` attributes plus `IntersectionObserver` ×4 and `requestAnimationFrame` ×6.
- **Lottie in cards.** The five `gsap` strings in the bundle are Lottie's internal frame driver (`_gsapFrame` ×3), not ScrollTrigger, which counts zero.

**Endex: the quiet register that still scores** `(winner-verified)`. A Next.js/Tailwind page with near-zero decorative motion that still took an Honorable Mention on content and craft.

- **Divided capability strip.** `divide-x` / `divide-Grey`, a rule-divided band of capabilities directly under the hero, marquee-scrolling on mobile. It reads alive through density and rhythm, not animation.
- **Editorial 12-column feature grid.** `lg:grid-cols-12` and `md:grid-cols-12` cards carrying **real product-UI slices**, so the content itself is the interest.
- **Exactly one decorative reveal.** The compiled CSS ships four keyframes (`spin`, `swiper-preloader-spin`, `wiggle`, `slideDownFromTopLeft`) and the DOM carries exactly one content `animate-` class, `animate-slide-down-from-top-left` at `.4s ease-out`. No IntersectionObserver reveal system, no `data-scroll`.
- **Life lives in hover and real content.** The mid-page does not breathe; it reads. That the jury still returned Usability 8.27 and Content 8.07 is the load-bearing lesson: an honest, dense editorial bento clears the award bar on real UI in the tiles and clean rhythm.

**Vercel** `(design-canonical, live markup)`. The alive tiles are CSS-transition widgets, not a motion library: the install-command tile animates width on `duration-[400ms] ease-[cubic-bezier(0.32,0.72,0,1)]` with `motion-safe:animate-command-fade-in`; nav links brighten muted→foreground on `transition-colors duration-100`. No Lenis, GSAP, Framer Motion, or Locomotive anywhere in the served markup.

### Hover on text

Across all three award winners, every text-hover response sits on an interactive element: link, button, nav item, list-row-as-link, form field. None ship a hover on a heading, a body paragraph, or a standalone metric.

**Anime.js**, verbatim, all six rules:

```css
#site-menu .main-nav-link:hover                       { color:var(--hex-fg-1) }
.text-layout p>a:hover, .text-layout li>a:hover       { color:var(--hex-current-1);
                                                        text-decoration-color:var(--hex-current-1) }
.text-layout p a:hover code                           { color:var(--hex-current-1);
                                                        background-color:var(--hex-current-6);
                                                        text-decoration:none }
ul.feature-links li a:hover .icon                     { transform:translate(.125rem) }
.links-list li a:hover                                { color:var(--hex-current-1);
                                                        background-color:var(--hex-current-7) }  /* transition-duration:0s */
.text-layout .ui-button:hover                         { color:var(--hex-fg-3);
                                                        border:1px solid var(--hex-fg-4) }
```

The prev-link icon nudges the other way, `-.125rem`. No `h1`, `h2`, `h3`, `p`, or metric carries a `:hover` anywhere.

**Meridian**, verbatim: `.c-rich-text a:hover{color:var(--color--orange-500)}` · `.c-text-link.cc-orange-light:hover{color:var(--color--orange-200)}` · `.footer_top_social_link:hover{background-color:var(--_theme---onsurface-light);color:var(--_theme---onbrand-dark)}` · and the one material-on-text gesture in the whole tier, a footer sitemap underline draw: `.footer_top_sitemap_link_underline{background-color:var(--_theme---onsurface-light);width:0%;height:1px;transition:width .5s cubic-bezier(.165,.84,.44,1)}`. Even that is an underline, not the word itself.

**Endex**, all Tailwind utilities on interactive elements: `.prose_prose__gIoBf a:hover{color:rgb(23 121 148…)}` (teal), `.hover:underline` / `.hover:no-underline`, color utilities `.hover:text-white` / `.hover:text-green` / `.hover:text-teal`, plus group-hover mechanics on cards: `.group:hover .group-hover\:w-full{width:100%}` (bar expand), `.group-hover\:translate-x-2{--tw-translate-x:0.5rem}` (arrow nudge), `.group-hover\:scale-\[1\.02\]` (a whisper card scale), and a decorative `grid-square` `rotateY(90deg) scale(.2)` flip. Durations cluster at `.15s`, eleven times.

**The sanctioned text-hover vocabulary is exactly three moves:** a neutral→foreground or accent color brighten on links and nav with no pill; an underline or bar draw (`scaleX` or `width` 0→1, roughly 0.3–0.5s, expo or quart ease) on links; an icon or arrow nudge of about `.125rem` beside a link. Headings, paragraphs, and metrics get nothing. A per-char rise, a weight or optical-size shift, or a color sweep along a heading is out-of-register for bento.

### Re-fire behavior

**Anime.js** obeys the law with a twist. Persisting: the demo canvases loop perpetually and stay interactive in view, so they re-play by nature of being running machines; the per-char hero stagger fires once and holds. Reversing: the per-section copy opacity, the `feature-links:before` divider `scaleX`, the page recolor, and the scroll cursor are all bound to scroll position, so scrolling up un-fades, un-draws, and un-recolors them. The twist is that anime.js welds even the *copy* to the scrubber, so the prose re-fades each pass, legible as intentional because the copy is furniture for the demo, not the payload.

**Meridian** obeys cleanly. IntersectionObserver reveal-on-enter fires once and the content stays; the marquees, WebGL spheres, and Lottie loops never stop, and Swiper parallax responds live to drag.

**Endex** has almost no surface to re-fire: one CSS reveal on load, stateless hover.

Running demos and ambient objects are the persistent layer; anything welded to a scrubber reverses on reverse-scroll. No winner ships a content payload that re-animates its entrance every pass.

### Smooth scroll

Absent across the entire tier: none of the three award winners smooth the wheel. No Lenis, Locomotive, or `@studio-freight` string appears in any served bundle.

- **Anime.js.** Native scroll read by its own `ScrollObserver` (11 occurrences, with `onScroll` 6×); `lenis` / `Lenis` = 0. A single global `scroll-behavior:smooth` governs anchor jumps only, and `.scroll-container{overscroll-behavior:contain}` is scoped to horizontal in-card demo scrollers.
- **Meridian.** `lenis` / `smoothscroll` / `inertia` / `damping` = 0 across all JS; no `scroll-behavior:smooth`.
- **Endex.** No Lenis, GSAP, Framer Motion, or Locomotive anywhere: the substring hits `framer` ×11 and `gsap` ×2 are `ComponentFrameRoot`, `forceFrameRate`, and a PostHog `flagsApiHost`; the package tell `framer-motion` counts zero.

Smoothing is absent, not register-dependent. Bento is a scan-and-click layout, which is also why the native pointer is kept. Adding Lenis to a bento build buys nothing the jury rewards and fights the scan-and-click reading pattern.

### Mid-page anti-signals

- **No kinetic prose.** Zero per-char or per-word scroll-scrubbed headings or paragraphs in the content zone. Per-char is hero-only and gated to the motion brand.
- **No hover on headings, body, or numbers.**
- **No smooth-scroll inertia.**
- **No universal card lift.** Meridian's group-hover scale is `1.02` on select cards only; Anime.js has no card lift at all; Endex uses group-hover color and translate on specific cards, never a blanket lift.
- **No global custom cursor.**
- **No blocking loader.**
- **No fade-up-on-everything with linear per-element delays.** Reveals, where present, are IntersectionObserver enter-once.

### Fixing a merely-good bento build

The dead middle is not fixed by adding text effects. It is fixed by committing to one of the three engines and running it through the content zone:

1. **If the product has a demoable surface.** Pin a `100lvh` panel per capability, run a real looping and interactive demo in it, cross-fade the copy against it, and recolor the page-wide accent per section. The mid-page becomes proof, not prose.
2. **If it does not.** Seat one ambient perpetual object (a WebGL or canvas sphere, or a marquee) that is always faintly moving, add a drag-parallax slider for case studies, and reveal cards on enter via IntersectionObserver. Native scroll.
3. **If the brand is editorial.** Put real product UI in the tiles, never placeholder shapes; divide a dense capability strip under the hero; let hover and rhythm carry it. Accept that the middle reads rather than breathes, and know that path still clears an Honorable Mention when the content is genuine.

Text hover stays in its lane: link brighten, underline or bar draw, arrow nudge. Nothing on headings or paragraphs.

## Refuted

- **"The Docs nav item gets the red `:before` pill"** is false: the pill belongs to the **Sponsor** button, `#site-menu sponsor-button .main-nav-link:before`. No `.docs-link` styling exists; a live screenshot shows Sponsor carrying the pill while Docs is muted text.
- **"Footer links fill red on hover — `a:hover{color:var(--hex-red-1);background:var(--hex-red-6)}`"** is false: that rule is scoped to `.links-list li sponsor-button a:hover`. General footer links use `--hex-current-1` on `--hex-current-7`, resolving to `--hex-fg-1` / `--hex-fg-7` inside the footer's `data-color="fg"` scope — a monochrome fill. The instant timing and the icon nudge hold.
- **"The Anime.js hero heading is `--text-xxl`"** is false: it is `--text-xxxxl`. `--text-xxl` is the toolbox and feature-panel heading size; copying it sets the hero two steps too small.
- **"Meridian scored 7.89 overall"** is false: **8.05**. Fifteen juror totals (7.40, 6.60, 8.00, 8.00, 8.00, 8.40, 6.90, 9.40, 8.20, 7.40, 9.40, 7.10, 9.20, 9.00, 7.70) sum to 120.70 over 15. Sub-scores: Design 8.20, Usability 7.93, Creativity 8.00, Content 7.87. Still the line's highest overall, still below 8.5.
- **"Endex scored 7.79 overall"** is false: **7.91** over fifteen jurors, one of them scoring 10/10/10/10.
- **"Endex Content 8.27, Design 8.13, Usability 8.07, Creativity 7.60"** is false on every figure. Live column means over fifteen jurors: Design **7.93**, Usability **8.27**, Creativity **7.27**, Content **8.07**. **8.27 is the Usability column, not Content.** The editorial-content lesson holds (Content 8.07 is Endex's second-highest column), but the number and its label were wrong.
- **"Ceiling 7.62–7.89"** is false: **7.62–8.05**, following from Meridian. The "no 8.5+ whole-site" finding stands.
