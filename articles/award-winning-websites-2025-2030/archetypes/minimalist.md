---
title: "Minimalist — Effect Palette, Page Recipe, Mid-Page Aliveness"
date: "2026-07-30"
author: "Coroboros"
tags: ["web-design", "awwwards", "minimalist", "css", "motion-design", "scroll-driven-animation", "typography"]
sources:
  - "https://www.awwwards.com/about-evaluation/"
  - "https://www.awwwards.com/sites/terminal-industries"
  - "https://www.awwwards.com/sites/gabriel-contassot"
  - "https://www.awwwards.com/sites/stefan-vitasovic-portfolio25"
  - "https://www.awwwards.com/sites/treize-grammes"
  - "https://www.awwwards.com/websites/minimal/"
  - "https://www.cssdesignawards.com/sites/terminal-industries/47847/"
  - "https://www.cssdesignawards.com/sites/gabriel-contassot-portfolio/45335/"
  - "https://x.com/awwwards/status/1975577815568220343"
  - "https://terminal-industries.com/"
  - "https://gabrielcontassot.com/"
  - "https://stefanvitasovic.dev/"
  - "https://www.13g.fr/"
  - "https://rogierdeboeve.com/"
  - "https://stripe.com/"
  - "https://www.rejouice.com/work/terminal-industries"
  - "https://tympanus.net/codrops/2025/03/05/case-study-stefan-vitasovic-portfolio-2025/"
  - "https://tympanus.net/codrops/2024/04/24/case-study-gabriel-contassots-portfolio-2024/"
  - "https://tympanus.net/codrops/2024/10/10/case-study-treize-grammes-2024/"
  - "https://tympanus.net/codrops/2024/07/26/case-study-rogier-de-boeve-portfolio-2024/"
---

# Minimalist — Effect Palette, Page Recipe, Mid-Page Aliveness

Verified minimalist winners cluster at 7.25–7.68 on the Awwwards jury, and their mid-page life comes from one scroll-welded decor channel rather than from text hover. What awarded minimalist sites ship, effect by effect, page part by page part, and in the prose zone between hero and footer. Parent reference (typography, palette, use cases, canonical winner): [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

## Corpus

Evidence tags: `(winner-verified)` = read from the awarded site's live CSS, JS, or DOM; `(shipped)` = observed live or in award-page media, implementation not read; `(technique)` = a documented method, typically Codrops; `(design-canonical)` = a documented design system with no verified award; `(single-source)` = one site only; `[CSS]` / `[JS]` = quoted from shipped code; **verified** / **stated** / **observed** = measured in source / claimed by the builder / seen but not read; `(stated, unconfirmed)` = a builder claim the source read could not confirm; `(inferred)` = derived from indirect evidence.

| Site | URL | Award | Overall / Developer | Stack |
|---|---|---|---|---|
| **Terminal Industries** | `terminal-industries.com` | Awwwards Site of the Day (SOTD) 3 Sep 2025 + Site of the Month Sep 2025 + Developer Award; CSS Design Awards Website of the Day 4 Aug 2025 (8.42) | **7.68** overall (7.95 / 7.36 / 7.65 / 7.57), **7.89** dev (Animations/Transitions 8.80) | Nuxt/Vue, Lenis |
| **Gabriel Contassot** | `gabrielcontassot.com` | Awwwards SOTD 14 Apr 2024 + CSS Design Awards | **7.34** overall, **7.63** dev | Astro, Lenis 1.0.42, GSAP + ScrollTrigger |
| **Stefan Vitasović — Portfolio25** | `stefanvitasovic.dev` | Awwwards SOTD 20 Sep 2025 + Developer Award | **7.25** overall (7.31 / 6.94 / 7.51 / 7.38), **8.04** dev (Animations/Transitions 8.80) | Next.js, Framer Motion, R3F |
| **Treize Grammes (13G.)** | `13g.fr` | Awwwards Honorable Mention (HM) 11 Oct 2024, no jury score | HM tier, 6.5+ | Webflow, Lenis 1.1.13, GSAP 3.12.5 + ScrollTrigger, three.js r128, Swiper 11 |
| **Rogier de Boevé** | `rogierdeboeve.com` | Codrops case study 26 Jul 2024; no award confirmed, **(single-source)** | — | Astro, Three/Alien.js, GSAP, Lenis |

Terminal is the anchor: the deepest CSS read of the corpus, tokens `--c-lime:#abff02`, `--c-dark-green:#052424`, `--c-orange:#fb6b3c`, `--c-gray:#454742`, `--c-dirty-white:#f0f0f0`, set in Suisse Int'l + Geist Mono. Stefan runs `#f1efeb` foundation, `#252526` ink, `#066bbd` blue accent in HelveticaNow Display. Gabriel pairs Monument (display) with Söhne over a strict `#000` monochrome. Treize is two colors, `#131313` / `#EEEEEE`. Rogier sets JetBrains Mono + Neue Haas Grotesk over dark, high-contrast WebGL scenes.

**Stripe** (`stripe.com`, "HDS" design system) is reference-tier: its CSS is read for button and nav-surface triangulation, and it is not itself an award page.

Three cautions on the roster. `awwwards.com/sites/portfolio-25-1` is a **different site**, Roman Jean-Elie's "Portfolio '25" (7.21, tagged 3D / GSAP / Three.js / Next.js, SOTD 2 Nov 2025), not Stefan's, whose entry is `stefan-vitasovic-portfolio25`. Treize's award page publishes no jury aggregate, only per-voter community votes ([`brutalist.md`](./brutalist.md#refuted) carries the dated mean). Gabriel's SOTD date on the live award page is **14 Apr 2024**.

### The score reality

Jury scores cluster **7.25–7.68** across verified minimalist winners. The cause is the weighting (Design 40% / Usability 30% / **Creativity 20%** / Content 10%, with Honorable Mention at 6.5+): Creativity rewards spectacle; restraint caps the ceiling. The corpus's 8.5+ figures are Creativity sub-scores on immersive sites ([`immersive-cinematic.md`](./immersive-cinematic.md)), never a minimalist overall. So the tier to study is the line's own highest scorers, the 7.25–7.68 SOTD winners in the corpus above; the universal negative is inductive over that sample.

## Effect palette

### Hover and micro-interactions

The AI default ships the same pale-tint fill-sweep (`background` fading to a 5–10% wash of the accent) on every button, a left-to-right underline slide on every link, and a solid opaque nav bar with a contrasting `border-bottom` on scroll. One gesture applied uniformly, so button = link = nav item.

The winners give each element class a *different geometry*, all resolving to the *one* accent. The pale-tint fill is real but quarantined to ghost and tertiary buttons; primary CTAs move the full token. No examined winner hangs a colored border under the nav.

**Directional token-wipe inversion (primary CTA).** A pseudo-element the color of the dark token sits translated below the button inside an `overflow:hidden` pill and slides up on hover, inverting the token pair. Terminal's lime button (`#abff02` bg / `#052424` text) becomes `#052424` bg / `#abff02` text. **(winner-verified)**

```css
.cta-button { background-color: var(--c-lime); color: var(--c-dark-green); overflow: hidden;
  transition: color .3s cubic-bezier(.39,.575,.565,1), background-color .3s cubic-bezier(.39,.575,.565,1) .2s; }
.cta-button:before { background-color: var(--c-dark-green); transform: translate3d(0,100%,0);
  transform-origin: bottom; transition: transform .7s cubic-bezier(.19,1,.22,1); }
.cta-button:hover:before { transform: translateZ(0); }
.cta-button:hover { background-color: transparent; color: var(--c-lime) !important; }
```

The wipe runs `.7s` easeOutExpo; the ink recolors over `.3s` with a `.2s` delay, so the text flips as the fill arrives. Full-strength color the whole way, never a wash. **Where it fits.** The single hero CTA in a photography-led or high-contrast system.

**Full-token background shift, ink held (primary CTA, flat systems).** No wipe; hover swaps `background-color` to a dedicated hover *shade of the same brand hue* (`--hds-color-button-primary-bgHover`), text unchanged. The secondary variant shifts both background and text tokens. A true darker or lighter step of the accent, not a transparency wash. **Where it fits.** Airy Swiss-grid SaaS where a moving fill would read as noise. **(winner-verified, reference-tier)**: Stripe `.hds-button:hover`, `.hds-button--secondary:hover`. Second corroboration: Terminal's `.drawer-cta-button:hover` (white→lime, or lime→dark-green token swap, `.2s ease`). **(winner-verified)**

**Underline draw under the label (link and CTA sub-mark).** A 1px `:after` bar, `transform:scaleX(0)`, drawn to `scaleX(1)` with the origin flipping on hover. Terminal runs it at two speeds, and the two are not interchangeable:

```css
/* CTA label — slow, right origin */
.cta-button .link-active:after { transform: scaleX(0); transform-origin: right;
  transition: transform .7s cubic-bezier(.19,1,.22,1), background-color .7s; }
.cta-button:hover .link-active:after { transform: scaleX(1); transform-origin: left; }

/* content link — fast, left origin */
.content-link-text:after { background-color: var(--c-lime); transform: scaleX(0);
  transform-origin: left; transition: transform .3s var(--ease-out); }
.content-link:hover .content-link-text:after { transform: scaleX(1); }
```

The `.7s` right-to-left draw belongs to the **CTA label**; inline content links draw at `.3s`. This is the one place the classic underline slide belongs: on links, not smeared onto buttons. **(winner-verified)**

**Strike-through on link hover.** `@media(any-hover:hover){a:hover{text-decoration:line-through}}`: no motion, editorial confidence. On the nav, hovering the group strips the active link's decoration so focus follows the pointer: `.Nav_navLinks:hover .Nav_isActive:not(:hover){text-decoration:none}`. **Where it fits.** Typographic portfolios where every link is body-set, not a chip. **(winner-verified, single-source)**: Stefan Vitasović.

**Link-with-arrow nudge.** Text opacity resolves to 1 and an inline arrow glyph translates up-right on hover: `.content-link:hover .link-arrow{transform:translate(2px,-2px)}`. Micro-amplitude: 2px reads as "this goes somewhere". Pairs with the underline draw. **(winner-verified)**: Terminal. Directional-nudge-on-hover is corroborated in spirit by Treize's gesture-led CTAs **(shipped)**.

**Ghost and tertiary pale-tint fill, the only sanctioned wash.** Transparent button; hover fills to a 5% tint of the dark token (`--c-dark-green-05: rgba(5,36,36,.05)`), text unchanged. On dark surfaces the drawer variant uses `#ffffff1a`, a 10% white wash. This is the fill the AI default over-uses; the winner reserves it for the lowest-priority action and never the hero CTA. **(winner-verified)**: Terminal `.cta-button--ghost:hover`, `.drawer-cta-button--ghost:hover`.

**Nav-item indicator: a growing accent dot, not an underline.**

```css
.nav a:after { background-color: var(--c-lime); width: .3125rem; height: .3125rem;
  opacity: 0; transform: translate(-50%) scale(0);
  transition: transform 1s cubic-bezier(.075,.82,.165,1), opacity .3s; }
.nav a:hover:after { opacity: 1; transform: translate(-50%) scale(1.01); }
```

A 5px accent square centered below the label, fading in on a long easeOutCirc while the label recolors to the accent. A point, not a bar. **(winner-verified)**: Terminal `.nav a:after`, `.nav-dropdown-trigger:after`. **(single-source)** on the exact dot; the principle that a nav item takes a different mark from an inline link holds across the corpus.

**Nav-bar surface: float transparent, or frost translucent.** Two verified treatments, zero colored border-bottoms.

- **Float transparent**: `position:fixed`, `background:transparent`, white text, `pointer-events:none` on the shell with children re-enabling. No surface, no border; it sits over the hero. The dropdown *panel* is the only opaque surface: solid `#454742` warm gray, `border-radius:8px`, opening `dropdown-in .25s cubic-bezier(.16,1,.3,1)`. **(winner-verified)**: Terminal `.site-header`, `.nav-dropdown-content`.
- **Frost translucent**: the nav overlay is a semi-opaque light panel, `linear-gradient(transparent, rgba(236,239,241,.8))` + `backdrop-filter:blur(5px)`, no border line. **(winner-verified, reference-tier)**: Stripe `.hds-navigation-menu__overlay`.

Transparent float over a photographic or dark hero; frost-blur over content-dense pages.

### Motion and scroll

The AI default fires one `fade-up` (opacity 0→1, `translateY(20px)`, `~0.6s ease`) on every section from a single IntersectionObserver, over Tailwind's `transition: … cubic-bezier(.4,0,.2,1) .15s` on everything. Uniform distance, uniform easing, uniform timing.

**Lenis smooth-scroll as the substrate.** Near-universal: the page scroll itself is eased, and reveal choreography rides on top. Terminal runs Lenis under a custom Nuxt scroll layer (`document.documentElement.className === "lenis"`, `lenis@` in the bundle). Gabriel ships **Lenis 1.0.42** in `/_astro/hoisted.By4ZZI4s.js` (558KB): `window.lenisVersion="1.0.42"`, `this.toggleClassName("lenis",!0)`, `smoothWheel`, `data-lenis-prevent`, and runs `html.lenis lenis-smooth` at runtime. Treize loads `unpkg.com/lenis@1.1.13/dist/lenis.min.js` explicitly. Stefan is the exception: Framer Motion, no Lenis in the sampled chunks. Three of four ship it. **(winner-verified)**

**Expo easing family, ~0.7–1s for content reveals.** The signature curve is easeOutExpo `cubic-bezier(.19,1,.22,1)` at 0.7–1s for load-bearing reveals and fills; short color and opacity fades use easeInSine `cubic-bezier(.39,.575,.565,1)` at 0.2–0.3s; dropdowns and overlays use `cubic-bezier(.16,1,.3,1)` at ~0.25s; `--ease-out` is `cubic-bezier(0,0,.58,1)` for small UI. Two speed registers, not one. In Terminal's `entry.css` the grammar is countable: `cubic-bezier(.19,1,.22,1)` ×9 and `cubic-bezier(.39,.575,.565,1)` ×9, with the Tailwind default `cubic-bezier(.4,0,.2,1)` ×6, quarantined to utility overlays. **(winner-verified)**

**Clip-path masked reveal instead of bare fade-up.** Content wrapped in `overflow:clip` or `inset()` masks and revealed by moving the mask. Terminal wipes bottom-up, `clip-path:inset(0 0 100% 0)` → `inset(0 0 0 0)`. Gabriel varies the geometry per element class: `inset(0 0% 0 0)`, `inset(0 100% 0 0)` (right-to-left), `inset(100% 0 0 0)` (bottom-up), and kills kerning on one revealed text deliberately: `font-kerning:none;font-feature-settings:"kern" 0;clip-path:inset(0 100% 0 0)`. **(winner-verified)**

**Small-UI micro-reveal.** For inline state and element swaps Terminal names a Vue transition `reveal-y`:

```css
.reveal-y-enter-active { transition: opacity .6s cubic-bezier(.39,.575,.565,1),
  transform 1.2s cubic-bezier(.19,1,.22,1); }
.reveal-y-enter-from { transform: translate3d(0,100%,0); }
```

Two durations on one transition: the opacity resolves in `.6s` while the transform takes `1.2s`. A `.5rem` translate exists only on one scoped `[data-v-61c0a6e5]` leave-to variant. **(winner-verified)**

**Scroll-linked parallax by inverse scale, small offset.** Images scale inversely to scroll progress, `scale(1.2 + track.value * -0.2)`, while a masked inset opens; project media is synced to a camera or scroll value with a slight offset for depth. Amplitude is ±0.2 scale, never a 50%-translate parallax. **(stated)**: the Codrops case studies of Gabriel Contassot and Rogier de Boevé ("synced… with a slight offset to create a parallax effect").

**Section and route transition is a short opacity crossfade.** Stefan: `duration:0.5, ease:easeQuadInOut` via AnimatePresence. Gabriel: a full-screen color overlay fading at `slow.in` easing, `0.8s`. No slide-the-whole-page theatrics. **(stated)**: both Codrops case studies.

### Text effects

The AI default is a typewriter effect, or one headline fading up as a block. Either overplays or underplays.

**Per-char masked reveal, indexed stagger (signature).** Each glyph in its own `overflow:clip` wrapper with a kerning fix, translated in on an index-scaled stagger under expo easing:

```css
.text .char-wrapper { overflow: clip; }
.char-wrapper + .char-wrapper { margin-left: -.05em; }
.char { display: inline-block; }
.--char { opacity: 0; will-change: opacity, transform; }
.animated-logo { visibility: hidden; }
```

The wrapper scaffold is Terminal's, and it is load-time only: the intro wordmark, not mid-page prose. Translate and stagger are JS-driven, not in the CSS. Stefan's measured stagger is `duration: 1.25 + index * 0.025` per character with `easeExpOut`, driven by Framer Motion over masked segments positioned with `left` and `x` transforms. It appears once, high on the page. **(winner-verified scaffold; stated numbers, Codrops)**

**Scramble and decode text (supporting).** Characters cycle random glyphs before resolving, with hardcoded per-index timing (durations `[1.2, 1.5, 0.4, 0.2, 1, 0.6, 0.6]s`, delays `[0, 0.4, 1.3, 1.4, 1.5, 1.6, 2.1]s`), plus hover-prevention during the animation so re-triggers cannot collide. **Where it fits.** Menu labels or a monospace subhead. **(stated, single-source)**: Gabriel Contassot's Codrops case study.

**Clip-path line reveal.** Whole lines revealed by animating an `inset()` mask bottom-up or left-to-right (the masked reveal above), for supporting headings and captions where per-char reads busy. **(winner-verified)**: Terminal, Gabriel.

**Loader-counter recolor through the accent.** Display type animates its `color` through the palette: `@keyframes color-transition{0%{color:var(--c-light-light-gray)}30%{color:var(--c-lime)}to{color:var(--c-dark-green)}}`. Type carries the accent as motion, briefly, then settles to ink. The keyframe name carries a Vue scope hash in the shipped sheets (`color-transition-dfc3204d`, `-3ce802c4`) and the body is identical in all four component stylesheets. **(winner-verified)**: Terminal.

### Cursor and pointer

The AI default is a circle-follower or magnetic-blob cursor with lerp lag, the most over-shipped "award-y" tell.

**Deliberate system cursor (the archetype default).** No custom cursor: `cursor:pointer` on interactives, `cursor:default` elsewhere. Terminal ships no `cursor:none` at all (only pointer, default, not-allowed, progress); Stefan and Gabriel both keep `cursor:default`. Three independent sites make this canon, not a note. **(winner-verified)**

**`mix-blend-mode` on a text or overlay element, never a follower.** Where a blend effect appears it inverts a marquee or oversized label against whatever scrolls behind it: Gabriel `mix-blend-mode:difference`, Stefan `mix-blend-mode:multiply` and `mix-blend-mode:exclusion` on positioned label and image elements. Terminal's `entry.css` contains zero `mix-blend-mode` declarations. A restrained way to feel reactive without a JS cursor. **(winner-verified)**

### Loader effects

Loader forms are recipe-level; they live under [Loader and intro](#loader-and-intro).

### Composition

A winner reads as one design while button, link, image and nav all behave differently because the **geometry** varies per element class while three things hold constant: one accent, one easing family, one origin logic. The AI failure is the inverse: one geometry held constant across all classes, so nothing has hierarchy.

**Terminal Industries: one accent (`#abff02`), one easing family (expo / out-circ), one origin logic.** **(winner-verified)**

| Element class | Geometry on interaction | Shared invariants |
|---|---|---|
| Primary CTA | dark-green fill **wipes up**, token pair **inverts**, underline draws under label | lime resolve · `.7s cubic-bezier(.19,1,.22,1)` · origin = bottom edge |
| Ghost/tertiary btn | 5% dark tint fills, text held (ghost fill) | lime family · fast `.2s` |
| Nav item | label → lime, a 5px lime **dot grows** below (accent dot) | lime resolve · `1s cubic-bezier(.075,.82,.165,1)` · origin = center-below |
| Logo | color → lime, nothing moves | lime resolve · `.3s` |
| Content link | text opacity→1, underline **draws** L→R, arrow **nudges** up-right 2px (underline draw + arrow nudge) | lime · underline `.3s` · origin = left |
| Nav dropdown | trigger dot + arrow **rotates 180°**; panel = solid `#454742`, opens `.25s cubic-bezier(.16,1,.3,1)` | expo family · origin = top-center |
| Mobile menu btn | bespoke line-morph to X, one stroke flashes lime | lime accent · expo · staggered |

Five-plus distinct geometries (wipe, tint, dot, draw, nudge, rotate), none repeated, all speaking lime in an expo cadence resolving from a fixed edge. The spread is the craft; the constancy of accent, easing and origin is what stops it fragmenting.

**Gabriel Contassot: a near-monochrome system that still differentiates class.** **(winner-verified + stated)**

| Element class | Geometry | Shared invariants |
|---|---|---|
| Nav / menu labels | **scramble/decode** text on enter, hover-locked | mono type · indexed timing |
| Project images | `clip-path:inset()` reveal + inverse-scale parallax `scale(1.2+track*-0.2)` | scroll-linked · small amplitude |
| Inline links | underline draw + arrow direction cue | restrained, editorial |
| Oversized label | `mix-blend-mode:difference` inverts over scrolling content | no custom cursor |
| Route change | full-screen overlay fade, `slow.in 0.8s` | opacity-only |
| Intro | accelerating 1→100 counter, 2.8s | numeric, no spinner |

Coherence here comes from restraint of palette and type (one grotesk, one mono, near-zero color) while each class carries a different motion idiom. Variety of motion, unity of surface.

**The transferable rule.** Assign each element class its own recipe, then lock `--accent`, one easing family (expo for content, sine for color fades), and a single origin logic across all of them. If two classes share a geometry, one is redundant: differentiate or merge. The primary CTA and an inline link never resolve identically.

### Anti-signals — absent from every winner examined

- **A universal pale-tint fill-sweep on every button.** The wash exists only on the ghost button; every primary CTA moves the full token.
- **A colored `border-bottom` under a solid nav bar on scroll.** Zero winners.
- **The same underline slide on buttons, links and nav.** Winners split it: draw on inline links, dot on nav items, wipe or shift on buttons.
- **A custom circle-follower or magnetic-blob cursor.** Three sites keep the default cursor.
- **One global `fade-up 20px, .6s ease` on every section.** Reveals are masked under expo with indexed per-element timing.
- **Tailwind's `cubic-bezier(.4,0,.2,1) .15s` as the site's motion identity.** Fine for incidental UI; leaving everything on the framework default reads as no motion decision.
- **`Inter` as the display face.** Every winner picked a face with character; the roster names them.

## Page recipe

Section count runs 6–14; page length 4–22 viewport-heights (Terminal measures ~22 at a 676px viewport, the portfolios 4–14). Two structural families cover four of five winners; the fifth is a single-canvas outlier.

### Named page shapes

**Shape A: Product-narrative scroll (Terminal Industries, Treize Grammes).** A long, sectioned argument that opens on one held statement then walks a funnel: promise → social proof → mechanism reveal → enumerated benefits → human proof → conversion → oversized-wordmark close. Whitespace is the connective tissue: Terminal's footer alone carries `14.375rem` (230px) of top padding. The climax is the mid-page mechanism reveal (Terminal's "That's the Yard Operating System. YOS™" landing; Treize's "Be true / Be strong / Be bold" video triptych), not the hero. Rest beats are full-void gaps between sections. For SaaS, B2B and agency briefs with a mechanism to explain.

Ordered skeleton, Terminal, from the live DOM; the funnel order and the climax are **(winner-verified)**, the exact 9-count is approximate. Intensity `n/10` is a comparative 1–10 estimate of attention load (defined in [Composition Chains](../winners/composition-chains.md)):

1. Hero: sequenced statement over cinematic still · attention · 8/10
2. "Powering the yards behind the  brands you know": client-logo proof strip · proof · 4/10
3. Animated odometer/stat sequence recoloring into the accent · understanding · 6/10
4. "That's the Yard Operating System. YOS™": mechanism reveal (climax) · understanding · 9/10
5. Benefit 01 / 02 / 03: three enumerated sections · understanding · 5/10 each
6. "Built by logistics leaders…": executive quote + headshot · proof · 6/10
7. "How it Works": process · understanding · 5/10
8. Contact form: "Contact us and we will be in touch / same day, your way" · close · 7/10
9. Oversized-wordmark footer: `<h1>` "The yard of the future starts today." · close · 8/10

Seams are transparent masked cross-fades between sections, never hard cuts. Treize runs the same funnel across ~14 sections with Webflow `fade-up=""` reveals, the softer, less disciplined edge.

**Shape B: Gallery-index stack (Gabriel Contassot, Stefan Vitasović).** A text-only name card, then one full-bleed project per viewport, each masked-revealing on scroll, closing on a bare footer cue. The hero holds no image; the first project still below the fold is the reward. Medium is photography or video carried edge-to-edge in a single grade; type recedes to labels. Multi-route: each project opens a "single" page with a cover-slide transition. Seven to nine sections. For portfolios, design directors, studios.

Ordered skeleton, Gabriel, from the live DOM **(winner-verified)**:

1. Hero: "GABRIEL CONTASSOT" / "FREELANCE DESIGN DIRECTOR" / "18.24", text on void, "SCROLL TO EXPLORE" cue · attention · 6/10
2–8. Seven project stills, one per viewport (GIVENCHY · REPLAY · EQUINOX · SOPHIE · HARLEY · RENEW · ORIGINALS, in that exact order) · proof · 7/10 each, masked reveal on entry
9. Footer: "SCROLL UP" · close · 3/10

The seam is an inverse-scale parallax masked figure reveal between stills. Stefan runs the same shape as an SPA (`/`, `/projects`, `/about`) with a repeating-wordmark intro.

**Shape C: Single-canvas monolith (Rogier de Boevé).** **(technique / single-source)** One WebGL scene *is* the page: project images projected onto a "grid of transparent cubes, each assigned random alpha values"; navigation happens by "rotate the screens, which are evenly placed along a circular path" rather than moving the camera; the projection is "synced with the camera but with a slight offset to create a parallax". Chrome is deliberately sparse: "minimalist, sci-fi aesthetic … allowing the main visual to shine." For creative-developer portfolios where the medium is the message. The shape presupposes a WebGL build budget.

### Hero architectures

**H1: Sequenced statement over cinematic still (Terminal Industries).** **(winner-verified)** The hero headline is an `<h2 class="title title-sequence">`, not an `<h1>`; Terminal defers its only `<h1>` to the footer. Four statements cycle through the same slot via per-char masked reveal.

```css
.title-sequence { font-size: min(5.729vw, 146.667px); font-weight: 400; line-height: .95;
  letter-spacing: min(-.057vw, -1.46667px); }
```

Media is a full-bleed cinematic photograph (a golden-hour black-truck silhouette against amber sky) driven by a `<canvas>` frame-sequence (`BackgroundCanvas`) layered under an SVG `path-background` gradient mask. Nav floats transparent over the hero (System · Markets · Featured · Resources · About + DEMO / CONTACT). One CTA, "Take charge of your yard", never stacked.

Entrance beat table: easings and geometry winner-verified from CSS, durations tagged where not directly read:

| # | Element | Transform | Duration | Easing |
|---|---|---|---|---|
| 1 | Split curtain (top+bottom `#ededed` `50svh` panels) | retract off-screen | ~0.8–1.2s **(shipped)** | `cubic-bezier(.19,1,.22,1)` easeOutExpo |
| 2 | Odometer counter (`font-mono`, rolling digit stack) | 1→100, recolors `light-gray → lime(30%) → dark-green` | tied to load | linear roll |
| 3 | Hero H2 chars (`.char-wrapper{overflow:clip}`, `.char{display:inline-block}`, `margin-left:-.05em`) | `translateY` up, indexed stagger | ~1.0–1.25s, per-char +~0.025s **(technique)** | `cubic-bezier(.19,1,.22,1)` |
| 4 | Transparent nav | opacity 0→1 | ~0.25s **(shipped)** | `cubic-bezier(.16,1,.3,1)` |

**H2: Text-only name card (Gabriel Contassot, Stefan Vitasović).** **(winner-verified copy; motion shipped)** No hero image. Big name as `<h1>` (Gabriel "GABRIEL CONTASSOT" all-caps, Stefan "Stefan Vitasović"), role subhead one line below, generous void, a scroll cue ("SCROLL TO EXPLORE" / repeating wordmark). Nav is two to four links (INFO · CONTACT; Intro · Projects · About). No hero CTA; the scroll cue is the only affordance. Entrance is the loader counter handing into a per-char name reveal.

**H3: Editorial promise line (Treize Grammes).** **(winner-verified copy)** A short second-person imperative in `<h1>`, "Réveillez votre croissance" (the H1 opens "Réveillez" and "votre croissance" completes it), over a one-line subhead: "Agence de design de marque 100% créative : branding, stratégie, site et web app,  identités visuelles." (verbatim, including the double space; one DOM instance carries the singular typo "identité visuelles"). CTA present and warm: "Programmer une visio". The expressive edge: reveals are Webflow `fade-up=""`, not masked.

### Loader and intro

Three verified forms. Never a spinner, never a blocking brand-color splash.

**Split-curtain plus recoloring counter (Terminal Industries).** **(winner-verified)**

```css
.app-loader { position: fixed; z-index: 999; }
.top-mask { background: rgb(237,237,237); height: round(up, calc(var(--svh,1svh)*50), 1px); overflow: hidden; }
.loader { display: flex; flex-direction: column; justify-content: space-between; }
.digit-column { height: var(--digit-height); overflow: hidden; position: relative; }
.digit-stack { will-change: transform; }
```

Two `#ededed` curtain halves, `.top-mask` and `.bottom`, pixel-snapped to `50svh`; `.overlay` is a separate full-height tint. `.top` and `.bottom` are `overflow:hidden` clip masks. The counter is a `--font-mono` odometer whose digit stack rolls while the `color-transition` keyframe climbs `--c-light-light-gray` → `--c-lime` at 30% → `--c-dark-green`. **Handoff:** the panels retract to uncover an already-composed hero, and the counter's final dark-green rhymes with the footer's ground. A second loader variant, `.overlay[data-v-068da249]{background:rgba(0,0,0,0.7)}` (`#000000b3`), is the route-change form.

**Bare accelerating counter (Gabriel Contassot).** **(stated, Codrops)** A 1→100 numeric counter whose `setInterval` fires at progressively shorter intervals, `values = [1,2,…,100]` with `splitDuration = totalDuration/values.length` hardcoded per index, total ~2.8s, values positioned with `translateX()`. No curtain, no logo theater; it retracts straight to the text-only name card.

**Instant paint, reveals are the intro (Treize; the sanctioned default).** **(shipped)** Webflow `fade-up=""` sections paint immediately and the scroll reveals *are* the intro. Legitimate when the reveals carry enough choreography, but Treize's plain fade-up is the corpus's weakest motion and marks the line's floor.

### Route transitions

Multi-page winners only. The transition language rhymes with the loader curtain.

- **Terminal**: in-page element reveals use the Vue `reveal-y` transition (the small-UI micro-reveal above). Route changes reuse `.app-loader` with the dark `rgba(0,0,0,0.7)` overlay variant, a curtain cover that rhymes with the intro curtain. **(winner-verified markup; full sequence shipped)**
- **Gabriel**: project "single" pages bridge with video-carried case-study transitions **(shipped)**; inverse-scale masked figure reveals are the scroll-seam language.
- **Stefan**: SPA route changes; the Developer Award's Animations/Transitions sub-score is **8.80** on the award page, with "Transitions / Motion / Filters and Effects" the named strengths. Exact mechanics are JS-gated, not read. **(shipped)** Terminal Industries' award page carries an identical 8.80 Animations/Transitions figure under its own Developer Award (7.89): two real scores, not one misattributed.

The synthesis: a masked cover-slide between routes that echoes the loader curtain, with a lighter cross-fade for in-page element swaps. One curtain vocabulary, two amplitudes.

### Copy voice

Verbatim per winner, grep-confirmed against raw HTML unless tagged.

**Terminal Industries**: hero sequence, four separate `h2.title-sequence` nodes: "We have reinvented the future of logistics" / "through the yard." / "AI-native technology that turns manual tasks into connected missions." / "Moving the world by making goods flow." · section headings: "Powering the yards behind the  brands you know" (double space verbatim), "That's the Yard Operating System. YOS™", "Built by the Industry" · CTA: "Take charge of your yard" · close: "Contact us and we will be in touch " (trailing space verbatim) / "same day, your way" · footer `<h1>`: "The yard of the future starts today." · copyright: "Copyright Terminal Industries © 2025 All Rights Reserved". The single hype word in the page, "Revolutionary technology that transforms your yard from gate to dock", appears exactly once.

**Gabriel Contassot**: "GABRIEL CONTASSOT" / "FREELANCE DESIGN DIRECTOR" / "18.24" · cue "SCROLL TO EXPLORE" · footer "SCROLL UP" · nav "INFO" · "CONTACT".

**Stefan Vitasović**: "Creative Developer" · footer "2025." · subhead, live DOM `textContent`: "Design-driven creative developer focusing on motion and interactivity. Crafting award winning web experiences for over a decade. Currently Lead Creative Developer at 14islands, Stockholm. MSc in electrical engineering and information technology. Awwwards Jury member since 2020."

**Treize Grammes**: H1 "Réveillez votre croissance" · "Activez votre marque !" · triptych "Be true" / "Be strong" / "Be bold" · "On transforme…" · "Prenez rendez-vous avec l'un de nos associés" · CTA "Programmer une visio" · footer "Esprits créatifs pour marques créatives".

Voice formula for the line:

- **Person**: the hero is first-person-plural visionary ("We have reinvented…") or name-only ("GABRIEL CONTASSOT"); CTAs flip to second-person imperative ("Take charge of your yard", "Réveillez votre croissance", "Activez votre marque !").
- **Sentence length**: short declaratives, often fragments ("through the yard.", "same day, your way"). One clause per line; the line break does the punctuation.
- **Verb temperature**: warm imperatives at the CTA, cool declaratives in body. One heat spike per CTA, never sustained.
- **Punctuation signature**: a trademark mark on the product noun (YOS™), the period as a full stop on a fragment for weight ("2025.", "through the yard."), minimal commas.
- **Refuses**: adjective stacks, hype words ("revolutionary" is the ceiling, used once), and self-narration. Labels stay single words.

### Imagery art direction

Two treatments; each winner commits to exactly one, page-wide.

- **One dominant cinematic photograph held page-wide (Terminal).** Subject: industrial scale, a black truck. Crop: full-bleed, horizon-anchored. Light: golden-hour, single warm source, long shadow. Grade: amber and cream, low-saturation warm neutral matching the `--c-cream` ground. Treatment: driven as a `<canvas>` frame-sequence under an SVG gradient mask so the photograph animates subtly with scroll. **(winner-verified mechanism; grade shipped)**
- **Per-project full-bleed still series in a single grade (Gabriel, Stefan).** Subject: fashion and editorial portraits, motion captures. Crop: edge-to-edge, one asset per viewport. Grade: single hue; Gabriel runs a strict `#000` monochrome so every project reads as one body of work. Video used freely, held to the same grade. **(winner-verified layout; grade shipped)**
- **Dark gritty sci-fi WebGL (Rogier).** JetBrains Mono + Neue Haas Grotesk over desolate high-contrast scenes, Blade Runner 2049 and Dune as reference. **(technique / single-source)**

The rule the corpus enforces: **one grade across the whole page.** No mixed-source stock, no per-section color drift. The photograph or the monochrome *is* the color system alongside the single accent.

### Footer

Two modes. The designed footer is the line's award lever; the bare cue is the portfolio norm.

**Designed oversized-wordmark footer (Terminal).** **(winner-verified)**

```css
.footer-title { font-size: max(4.375rem, min(4.688vw, 120px)); font-weight: 400; line-height: .95;
  letter-spacing: min(-.141vw, -3.6px); max-width: min(57.292vw, 1466px);
  margin-bottom: min(4.688vw, 120px); }
.footer-title strong .--char { color: rgba(255,255,255,0.2); }   /* #fff3 */
.footer__wrapper { position: fixed; bottom: 0; transform: translateY(100%); }
.footer__height-holder { height: calc(var(--vh)*50); }
.overlay-sticky__wrapper { background: rgb(0,0,0); height: calc(var(--vh)*100); z-index: 2000; }
```

Ground is `var(--c-dark-green)` under a `footer-pattern` watermark at `opacity:.1`. The statement "The yard of the future starts today." renders in a `.footer-title` div, with the page's only `<h1>` wrapping the same text. Per-char emphasis de-emphasizes selected characters to 20% white. The 12-column grid runs `padding: 14.375rem 4.375rem 1.25rem` (230px top void): `logo-section` `1/span 4`, `footer-links` `6/span 4`, `footer-contact` `10/span 3`, `copyright` row 3 `1/span 6`, `credits` (REJOUICE logo, `.rejouice{width:6.25rem}`) `11/span 2`. Contact label in `SuisseIntl` at `1.25rem`; `contact-text` `#586a6a`; copyright `#fff6` at `.75rem`. **Sticky reveal:** the fixed wrapper slides up over a `50vh` height-holder as the page ends while a black `100vh` overlay at `z-index:2000` darkens the outgoing content. The footer arrives as a composed curtain, not a scroll-into.

**Bare functional cue (Gabriel, Stefan, Treize).** Gabriel "SCROLL UP". Stefan "2025." Treize "Esprits créatifs pour marques créatives" plus link columns (Branding · Réalisations · Site web · Ressources · Contact · Mentions légales). Type-only, no oversized moment.

### Spectacle menu

The one passage a judge replays: in every case a masked reveal choreographed against the single accent, never a particle effect.

- **Terminal, primary.** Trigger: page load. Beats: two `#ededed` curtain panels retract → the `font-mono` odometer rolls 1→100, its color climbing light-gray → lime → dark-green → curtains clear to a composed fold where the cinematic truck photo sits and the hero H2's characters cascade up out of their clip masks under easeOutExpo. Payoff: the counter's final dark-green is the footer's ground and the lime is the CTA; the intro pre-states the whole palette in one gesture. Replayable because it is one continuous move with no seam, and the recolor makes the accent feel earned rather than applied. **(winner-verified mechanism)**
- **Terminal, secondary.** The mid-page odometer re-fires the same recolor as proof numbers count up; the mechanism reveal "That's the Yard Operating System. YOS™" lands on it. **(winner-verified keyframe; scroll-trigger shipped)**
- **Gabriel.** An oversized label crossing a light/dark section boundary under `mix-blend-mode:difference`, plus scramble/decode text with hardcoded per-index timing and inverse-scale masked figure reveals, `scale(${1.2 + this.track.value*-0.2})` as an `inset()` mask opens. **(stated, Codrops; scramble timings single-source; the blend itself read live in the Astro CSS)**
- **Stefan.** The hero name reveal: masked segments driven by Framer Motion on an indexed stagger, `duration: 1.25 + index * 0.025`, `easeExpOut`, used once. **(stated, Codrops)**

### Page-level anti-signals

- **No winner opens on a card or bento grid.** The hero is a single held statement or a single photograph over void, never a tile field.
- **No hero carousel or slider.** Statements sequence in place; they do not slide as a gallery.
- **No hero stacks two CTAs.** One CTA or none; the scroll cue can be the only affordance.
- **The `<h1>` is not assumed to live in the hero.** Committing "hero = h1" by reflex misreads the line.
- **No spinner and no blocking brand-color splash.**
- **No second accent visible.** Two to three colors carry the page and the accent appears once per viewport; the rule is about what a viewport shows, not what the palette declares.
- **No mixed-grade imagery.**

## Mid-page aliveness

What keeps the middle of the page alive (the prose and content sections between hero and footer) at the top of this line, where merely-good builds land the hero and the image reveals and then read dead in between.

### The mid-page strategy

**At this tier the mid-page is not kept alive by text hover. It is kept alive by one scroll-welded decor channel that re-fires continuously (canvas frame-sequence, seam blend, or scroll-scrubbed clip) riding under one-shot content reveals.** Text hover is near-absent on prose and headings across the whole tier, and that absence is itself the finding.

### Per-site reads

**Terminal Industries: 7.68 SOTD (anchor, live CSS + live DOM).** Nuxt/Vue + Lenis, ~22 viewports (`scrollHeight 14717`, `vh 676`). The mid-page argument walks logo strip → "Powering the yards behind the  brands you know" → "Imagine the yard as an intelligent bridge…" → "Yard Operating System. YOS™" → "Built by logistics leaders…" → executive quote → contact. Live bundles: `entry.Bdya6FOo.css`, `PaddedCounter.D_9jWspQ.css`, `get-frames.BEFbNTY1.css`, `NewsSection.CgFcU66P.css`, `BackgroundCanvas.BfIfKjEO.css`, `NotchSection.CmaDBuu9.css`. Mid-page mechanics, all read from the live CSS:

- **Stat odometer** (`PaddedCounter`): slot-machine digit column, the shared `color-transition` keyframe recoloring gray → lime → dark-green. That keyframe body is baked identically into *every* component sheet (BackgroundCanvas, NotchSection, NewsSection, get-frames); the palette pre-state recurs section to section.
- **Canvas frame-sequence** (`get-frames`): `.video-sequence{overflow:clip}`, `.video-sequence canvas{position:absolute;width:100%;height:100%}`; full-bleed cinematic photography drawn to canvas and scrubbed by scroll position, 2 canvases live.
- **Scroll-scrubbed clip reveal**: `clip-path:var(--d27fb6da)`, a JS-updated CSS variable bound to scroll progress, alongside static one-shot masks `clip-path:inset(0 0 100% 0)` → `inset(0 0 0 0)`.
- **Mid-page card hover** (NewsSection): the one place a heading responds to hover on this site: `.slider-card__wrapper:hover{color:var(--c-white)!important;text-shadow:0 1px 6px rgba(0,0,0,.4),0 2px 12px rgba(0,0,0,.25)}`, plus a rollover image `opacity:0;transform:scale(1.2)` → `opacity:1;transform:scale(1)`.
- **Contact-form ambient**: `.border-holder{background:radial-gradient(circle at 50% 50%,var(--c-lime),transparent 15rem)}`, a lime radial glow behind the field, dimmed on sibling hover (`.slot__wrapper:hover+.background-gradient{opacity:.2}`).
- **Text hovers, the complete set**: `.phone-number:hover{color:var(--c-lime)}`, `.nav-dropdown-trigger:hover{color:var(--c-lime)}`, `.logo:hover{color:var(--c-lime)}` at `transition:color .3s`, `.call-us-cta__number:hover{filter:brightness(1.05)}`, `.drawer-link:hover{background-color:#ffffff1a;color:var(--c-lime)}`. No prose or heading hover beyond the NewsSection card title.

**Gabriel Contassot: 7.34 SOTD (live CSS + bundle + runtime, Astro).** Ships **zero** `:hover` rules across the stylesheet, grep-confirmed; the only `transition-*` declarations are Tailwind's unused `.transition` utility (`transition-property:color,background-color,…,transform,filter,backdrop-filter`, `transition-duration:.15s`, `transition-timing-function:cubic-bezier(.4,0,.2,1)`, 6 occurrences) applied to nothing. Motion is **GSAP + ScrollTrigger** with **Lenis 1.0.42** for smooth scroll, both module-scoped in `hoisted.By4ZZI4s.js`. Its mid-page life is directional masked reveals (`inset(0 0% 0 0)`, `inset(0 100% 0 0)`, `inset(100% 0 0 0)`: right, left and bottom wipes, geometry varied per element class), one `mix-blend-mode:difference` seam label, a deliberate kerning kill on a revealed text, and inverse-scale figure parallax. The data point: a monochrome portfolio wins SOTD with **no hover affordance at all**; the life is 100% scroll-driven masked reveals plus one blend seam.

**Stefan Vitasović: 7.25 SOTD (live CSS, Next.js).** Reveal motion is Framer Motion; no transition rules on reveals in the CSS. The tier's one real text hover on body-set links is `@media(any-hover:hover){a:hover{text-decoration:line-through}}`. Sibling-aware nav hover strips the strike from the active link. Idle grid lines surface on hover: `@media(any-hover:hover){.Lines_horizontal,.Lines_vertical{display:block}}`. Blend overlays use `mix-blend-mode:multiply` and `mix-blend-mode:exclusion` on positioned label and image elements.

**Treize Grammes: Honorable Mention (live CSS, Webflow).** CDN scripts, verbatim: `unpkg.com/lenis@1.1.13/dist/lenis.min.js`, `gsap@3.12.5` + `ScrollTrigger.min.js`, `three.js/r128/three.min.js`, `swiper@11`. Text hovers are color swaps: `.footer__link:hover{color:var(--base-color-neutral--white)}`, `.footer__link__legals:hover{color:var(--base-color-neutral--green)}`. ScrollTrigger drives the mid-page reveals: one-shot content, scrubbed decor. The softest register of the four, and the only one running a WebGL layer under a minimalist skin.

### The aliveness inventory

Ranked by how load-bearing each is across the tier.

1. **A scroll-welded decor channel that runs the full page height**: the single most important mid-page mechanism and the one merely-good builds omit. One of: a canvas frame-sequence scrubbed by scroll (Terminal); a `mix-blend-mode:difference` label crossing every light/dark seam (Gabriel); a scroll-scrubbed `clip-path:var()` whose value tracks scroll progress (Terminal). This channel is *decor*: it re-computes as a function of scroll position, so it re-fires every pass. It is what makes the space between reveals feel driven rather than static. **(winner-verified)**
2. **Masked content reveals, geometry varied per element class**: `clip-path:inset()` wipes fired once as sections enter, bottom-up on Terminal, plus left, right and bottom variants on Gabriel. Never one global fade-up.
3. **A recoloring stat or number moment**: Terminal's slot-machine odometer climbing gray → lime → dark-green. The number is the mid-page climax of the proof section.
4. **Inverse-scale figure parallax**: image scales `1.2 → 1.0`, amplitude ±0.2, as its mask opens. Small amplitude; never a 50%-translate parallax. **(technique)**
5. **Mid-page card hover, only where the layout has cards**: Terminal's NewsSection heading `text-shadow` deepen plus the `scale(1.2→1)` rollover. The rare mid-page heading hover in the corpus.
6. **One ambient touch, or its declared absence**: Terminal's lime radial glow behind the contact field is the entire idle band. The corpus-wide pattern is about one quiet channel; the page is otherwise held still between inputs. Stillness is the register, not coverage skipped.
7. **Section-transition seams**: masked, never hard cuts; the void gap between sections is active whitespace. The blend-label seam turns the boundary itself into the show.

The per-char masked reveal is **load-time only**: Terminal's `char-wrapper` scaffold is on the intro wordmark, not mid-page prose. Mid-page headings are revealed by clip-path line wipes; per-char mid-page would read as busy at this line.

### Hover on text

The tier ships almost no hover on non-link text, and that is the data.

- **Prose body text**: none, anywhere in the corpus.
- **Headings**: one instance total, Terminal's NewsSection card title. No standalone heading in a prose section responds to hover on any site read.
- **Links, including body-set editorial links**, two forms: strike-through, `a:hover{text-decoration:line-through}` guarded by `@media(any-hover:hover)` (Stefan), and color-sweep to accent, `color:var(--c-lime)` at `transition:color .3s` (Terminal nav, phone, logo; Treize footer). The accent sweep is a plain color transition, not a per-char sweep along the text.
- **Numbers**: one, `.call-us-cta__number:hover{filter:brightness(1.05)}`, a 5% brightness lift.
- **List and drawer rows**: `background-color:#ffffff1a` plus `color:var(--c-lime)`.
- **Per-char rise on hover, weight-shift, optical-size shift on hover**: not shipped by any site read. The optional variable-font `wght` micro-shift on hover is not observed live at this tier.

Verbatim, the entire hover-on-text surface at this tier is: `a:hover{text-decoration:line-through}` · `…:hover{color:var(--c-lime)}` · `…__number:hover{filter:brightness(1.05)}` · `.slider-card__wrapper:hover{color:var(--c-white);text-shadow:…}` · row `:hover{background-color:#ffffff1a}`. No color-sweep along the glyphs, no background highlight on prose, no material underline on headings. A build that adds heavy per-char hover to mid-page prose is out of register for this line.

### Re-fire behavior

The law, *content persists, decor reverses*, holds at this tier, verified by mechanism.

**Re-plays every pass, scrubbed and positional:** the canvas frame-sequence (the drawn frame is a pure function of scroll position, so it re-renders identically at the same scrollY on every pass, both directions); `clip-path:var(--d27fb6da)` (clip value bound to scroll progress, re-computes both directions); the `mix-blend-mode:difference` seam label (the inversion is a render-time function of what is behind it, so it re-inverts every time the seam is re-crossed); inverse-scale figure parallax tied to the scroll track. **(winner-verified mechanism / technique)**

**Fires once and persists:** the char intro reveal (`visibility:hidden` → revealed once); `clip-path:inset()` section masks with an in-view trigger; the odometer count-up, which settles on the final number and is not re-driven on re-entry. **(winner-verified scaffold / technique)**

The precise reading: the mid-page feels alive on re-scroll **because the decor channel is positional, not triggered**; it has no "already fired" state to get stuck in. Merely-good builds fire everything once on an IntersectionObserver and the page is inert on the second pass. The fix is not to make reveals replay, which reads cheap; it is to add one positional or scrubbed decor channel that has no fired state.

### Smooth scroll

Near-universal at this tier and register-independent: **3 of 4** run Lenis. Terminal (`html.lenis`, `.lenis-smooth`, `.lenis-autoToggle` classes in the shipped HTML/CSS), Treize (`lenis@1.1.13` via unpkg), Gabriel (**Lenis 1.0.42**, bundled and active with `html.lenis lenis-smooth`, `window.lenisVersion === "1.0.42"`). Only Stefan lacks it: Framer Motion, no Lenis in the sampled chunks. Lenis is the tier norm.

### Mid-page anti-signals

The tier's mid-page negatives follow from the reads above: text hover stays on links (Hover on text), only decor replays (Re-fire behavior), and one quiet ambient channel is the ceiling (the aliveness inventory, item 6).

## Refuted

- **"Stefan's hero subhead reads 'Crafting web experiences from Stockholm, Sweden. Awwwards Jury Member since 2020.'"** is false, and invented: the string is unfindable in the live DOM. The verified `textContent` is the longer 14islands/MSc sentence recorded under Copy voice.
- **"Terminal's `reveal-y` is `opacity` + `translateY(.5rem)` at `.25s ease`"** is false on both values: the live rule is `transition:opacity .6s cubic-bezier(.39,.575,.565,1),transform 1.2s cubic-bezier(.19,1,.22,1)` from `translate3d(0,100%,0)`. `.5rem` exists only on one scoped `[data-v-61c0a6e5]` leave-to variant.
- **"The line's voice formula refuses exclamation marks"** is false: Treize ships "Activez votre marque !" live.
- **"Stefan's per-char reveal wraps each glyph in its own `overflow:clip` wrapper"** is false, mis-attributed: Codrops describes "masked segments with `left` positioning and `x` transforms, not individual character wrappers with overflow clipping". The wrapper scaffold is Terminal's. The stagger `duration: 1.25 + index * 0.025` and `easeExpOut` stand, driven by Framer Motion, not GSAP.
- **"The `#ededed` `50svh` loader halves are `.overlay` panels"** is false: they are `.top-mask` and `.bottom`. `.overlay` is a separate full-height tint.
- **"`.footer-title` is the page's `<h1>`"** is false: it is a `div`. The `<h1>` is a separate wrapping element carrying the same text.
- **"Terminal ships no second accent"** is false as a palette claim: the palette declares `--c-orange:#fb6b3c` alongside `--c-lime`. True only of visible per-viewport usage.
- **"Gabriel ships no smooth-scroll library (winner-verified absent)"** is false: Lenis 1.0.42 is bundled in `hoisted.By4ZZI4s.js` and active at runtime.
- **"Gabriel's motion is hand-rolled JS, no GSAP"** is false: `gsap.registerPlugin(...)`, `_gsap`, `GreenSock` and `ScrollTrigger` are all in the bundle, module-scoped rather than on `window`.
- **"The gallery-index register can win without Lenis"** is unsupported: 3 of 4 sample sites run Lenis and the case rests on Stefan alone.

## Could not verify

- **In-flight replay on the live pages.** Terminal's Nuxt + Lenis setup rejects synthetic `scrollTo` and wheel events under automation, so the re-fire determination is mechanism-grounded, not motion-captured.
- **Terminal's entrance durations.** The curtain retract (~0.8–1.2s), nav fade (~0.25s) and per-char stagger (~1.0–1.25s, +~0.025s per char) in the hero beat table are `(shipped)` / `(technique)` estimates; only the easings are read from CSS.
