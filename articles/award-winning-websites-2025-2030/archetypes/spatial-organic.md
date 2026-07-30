---
title: "Spatial Organic — Effect Palette, Page Recipe, Aliveness"
date: "2026-07-30"
author: "Coroboros"
tags: ["web-design", "design-archetypes", "spatial-organic", "webgl", "scroll-driven-animation", "view-transitions", "variable-fonts", "gsap", "lenis", "css", "awwwards", "motion-design"]
sources:
  - "https://www.awwwards.com/sites/igloo-inc"
  - "https://www.awwwards.com/igloo-inc-case-study.html"
  - "https://www.webgpu.com/showcase/igloo-inc-procedural-crystals/"
  - "https://www.igloo.inc/"
  - "https://www.awwwards.com/sites/exo-ape"
  - "https://www.exoape.com/"
  - "https://www.awwwards.com/exo-ape-wins-site-of-the-month-may-2022.html"
  - "https://www.awwwards.com/sites/cyd-stumpel-portfolio-2025"
  - "https://cydstumpel.nl/"
  - "https://www.awwwards.com/sites/sculpting-harmony"
  - "https://www.awwwards.com/sculpting-harmony-wins-site-of-the-month-november-2023.html"
  - "https://thefwa.com/cases/sculpting-harmony"
  - "https://the-brandidentity.com/project/with-type-that-moves-and-dances-resn-designs-the-sculpting-harmony-exhibition-to-dramatic-effect"
  - "https://www.itsnicethat.com/news/resn-sculpting-harmony-web-design-graphic-design-news-071223"
  - "https://www.awwwards.com/sites/obys-2"
  - "https://obys.agency/"
  - "https://www.awwwards.com/sites/aristide-benoist-portfolio"
  - "https://www.awwwards.com/sites/aristide-portfolio-2021"
  - "https://aristidebenoist.com/"
  - "https://tympanus.net/codrops/2025/11/19/how-to-build-cinematic-3d-scroll-experiences-with-gsap/"
  - "https://tympanus.net/codrops/2026/03/06/obys-the-small-studio-designing-big-digital-narratives/"
  - "https://arc.net/"
  - "https://www.granola.ai/"
---

# Spatial Organic — Effect Palette, Page Recipe, Aliveness

Spatial-organic winners top out at 7.92 overall on the Awwwards jury and pay a standing Usability tax for heavy WebGL and glass, and the line keeps its middle alive with native `animation-timeline` rather than JS scrub. Effect palette, page recipe, and mid-page aliveness for the spatial-organic archetype — a ninth line extending the parent reference's eight archetypes, which postdates the article. Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

The DNA — z-depth, organic clip-paths, procedural texture, native browser APIs, earthy palette — is assumed. What follows is the per-element repertoire, the page assembly, and what keeps the middle alive.

Evidence tiers: `[CSS-verified]` / `(winner-verified)` = read directly off the live site's authored stylesheets, bundles, or rendered DOM. `(score-verified)` = read from the Awwwards site page. `[case-study]` / `(media-only)` = confirmed in an award case study or design writeup, parameters quoted where published. `(observed)` = visible behavior, implementation unverified. `(single-source)` = one site carries the exact variant; a lead, not a law.

## Corpus

| Site | Award | Overall | Design / Usability / Creativity / Content | Depth |
|---|---|---|---|---|
| **Igloo Inc** (`igloo.inc`) | Awwwards **Site of the Day (SOTD) 23 Jul 2024** + **Site of the Year (SOTY) 2024** + Developer Site of the Year; Dev Award 7.66 with **Animations/Transitions 9.60**, WPO 8.00, Accessibility 6.60 | **7.92** | 8.05 / 7.5 / **8.31** / 7.91 | score-verified + case study; live shell read |
| **Exo Ape** (`exoape.com`) | Awwwards **SOTD 23 May 2022** + **Site of the Month (SOTM) May 2022**; Dev Award 8.16 with Animations **9.00**, WPO 8.20 | **7.89** | 7.99 / 7.73 / 7.73 / **8.24** | winner-verified (inline CSS + all six Nuxt bundles) |
| **Sculpting Harmony** (Resn × Getty, `gehry.getty.edu`) | Awwwards **SOTM Nov 2023** + FWA; Dev 7.78 with Animations 8.60 | **7.89** | 7.97 / 7.52 / **8.19** / 8.04 | media-only — the live TLS certificate has expired |
| **Cyd Stumpel** (`cydstumpel.nl`) | Awwwards **SOTD 9 Mar 2025**; Dev 7.74 | **7.22** | 7.29 / 7.06 / 7.23 / 7.35 | winner-verified (authored theme CSS, JS, rendered DOM) |
| **Aristide Benoist** (`aristidebenoist.com`) | Awwwards **SOTD 11 Oct 2017** for this entry; the site's own ledger reads 30 SOTD / 3 SOTM / 2 Independent of the Year, plus 27 Developer Award, 6 Mobile of the Week, 22 Mobile Excellence | **7.37** | 7.62 / **6.67** / 7.72 / 7.78 | score-verified; post-JS DOM + render |
| **Obys Agency** (`obys.agency`) | Awwwards **SOTD 04 May 2026** + Developer Award; Awwwards Studio of the Year 2023; CSSDA Studio of the Year **×4** (2020, 2021, 2023, 2024) | — | — | rendered DOM |
| **Arc** (`arc.net`), **Granola** (`granola.ai`) | **Not Awwwards winners** — style anchors only. Arc runs warm cream `#FFFCEC` and bespoke *Marlin*; Granola bespoke *Melange* and an "oats" warm token family | — | — | Granola winner-verified CSS; Arc shell-only (client-rendered SPA) |

The line splits into three registers sharing one DNA: **in-engine WebGL** (Igloo, Sculpting Harmony), **editorial-organic warm** (Cyd Stumpel), and **cinematic-photo dark** (Exo Ape at the core, with Obys as the index-first edge and Aristide as the dark-generative edge).

### The score reality

Overall jury scores on this line top out at **7.92** (Igloo); the corpus's highest whole-site score is Lusion's 8.25 ([`experimental.md`](./experimental.md)). Jury averaging compresses the overall, and the archetype pays a standing **Usability tax** — heavy WebGL and glass (backdrop-filter, dark-on-dark contrast) cost the Usability sub-score, which caps the overall in the high 7s. The Usability column runs **6.67–7.73** across the whole line and nobody buys the cost back. The 8.19–8.31 figures that exist are **Creativity sub-scores**, never overall. Igloo — the Site of the Year — scores 7.92 overall; its genius is recorded in the 9.60 Animations/Transitions dev sub-score, not the SOTD average. The real ceiling to build against is roughly 7.9 overall and 8.3 creativity.

---

## Effect palette

### Buttons and CTAs

The AI-default: one universal button rule — a pale, washed-out tint fill sweeping a 20–40% pastel of the accent with a soft blurred drop-shadow, applied identically to every button, link, card, and nav item.

The pale-tint fill sweep appears on **zero** sites examined. Winners split the treatment by element class and carry the interaction on displacement, committed in-family fills, or a drawn line.

- **Accent-displacement push.** The base surface barely changes; the button translates a few pixels and a **hard, un-blurred offset shadow in the accent color** appears on the opposite side, reading as a physical card lifting off a colored underlayer.

  ```css
  .button:hover { background: color-mix(in srgb, var(--color-background) 95%, var(--color-accent));
                  color: var(--color-accent);
                  transform: translate(-2px, 2px);
                  box-shadow: -1px 1px 0 0 var(--color-accent) }
  ```

  Cyd Stumpel, on a base `64px` pill radius `[CSS-verified]`. The 95/5 mix is the tell: the winner *refused* a fill and signalled through displacement, accent text, and a hard accent shadow. Corroborated in a softer blurred variant by Arc (`transition: transform .15s, box-shadow .15s ease-out`, `rgba(0,0,0,.1) 0 5px 5px`, radius 10px) and, as a non-award production reference, by Mailchimp's `.ctaPrimary:hover` (`translateY(-0.375em)` plus a hard `0 0.375em 0 0 var(--cta-depth-color)`). The pattern spans one winner (Cyd) plus two non-award references (Arc, Mailchimp); the exact 1px accent-shadow variant is single-source.
- **Committed in-family token fill.** For a fill, winners swap to a defined `-hover` token one step within the same brand family, never a pale pastel. Granola's group-hovers resolve to `--color-fill-accent-hover`, `--color-fill-soft-opaque-hover`, and `--color-oats-green-300 → 400` — one warm step darker `[CSS-verified]`. Cyd's primary form submit is `background-color: color-mix(in srgb, var(--color-accent, var(--color)) 80%, var(--color))` — a strong 80% accent fill reserved for the true primary action, not sprayed across every button. The strong fill stays on one action per view.
- **Inversion pair.** The same button ships in two committed token states rather than one fading in. Arc: white background with brand-blue text `#2702C2`, and its exact inverse, both at radius 10px `[CSS-verified]`. Granola's primary CTA is a solid dark pill, `#292929` on warm-cream `#FCFCF8`, fully rounded; its hover end-state was never captured, so the behavior is `(observed)`.

### Text links

- **Underline draw.** A pseudo-element rule scaling `0→1`, not a `text-decoration` toggle. Exo Ape runs one system across the whole site — `.nav-link:hover:after`, `.list-link:hover:after`, `.footer-link:hover:after` all take `{transform: scaleX(1); transform-origin: left center}` from a resting `scaleX(0)`, inside a `@media (hover:hover)` guard on Vue-scoped selectors; the link colour also shifts to `--color-light-grey` `[CSS-verified]`. Arc uses the simpler `a:hover { text-decoration: underline }`. This is where the accent line belongs — on links, never as nav chrome.
- **Underline as a background material.** Cyd draws the underline with a gradient whose height animates: `background-image: linear-gradient(var(--underline-color) 0 0); background-size: 100% var(--underline-height)`, resting at `--initial-underline-height: 0.1em`, drawn to a full-height highlight on `:focus-visible` (`--underline-height: 100%`, `border-radius: .2em`, `color: var(--hover-color)`). On mouse hover a `.link-hover__tooltip` fades in with `{opacity:1; pointer-events:auto; transform: translateY(0)}` `[CSS-verified]`.
- **Accent wash plus arrow nudge.** For inline and utility links: a 10% accent wash, a 1px lift, and a diagonal arrow shove. Cyd `.platform-link:hover { background-color: color-mix(in srgb, var(--color-accent), transparent 90%); transform: translateY(-1px) }` with `.platform-arrow { transform: translate(2px, -2px) }` `[CSS-verified]`. Arc corroborates the arrow nudge; the 10% wash is single-source.

### Images and cards

- **Radius-morph plus crossfade.** The card's border-radius animates to a rounder value while a resting graphic crossfades to the full image and the caption slides up.

  ```css
  .work-thumb:hover .work-thumb__circle { opacity: 0;
      border-radius: var(--hover-radius-full);
      transition: opacity .2s .1s ease-out, border-radius .2s .1s var(--default-ease) }
  ```

  The full image crossfades in, `.img-container` rounds to `var(--hover-radius)`, the title slides to `translateY(0)`, and the labels stagger through modern CSS: `--delay: calc((abs(sibling-index() - (sibling-count() / 2))) * 0.05s)` `[CSS-verified, Cyd]`. Single-source for the exact recipe. The corners breathing is the archetype signature and costs far less than a WebGL displacement.
- **Still→video swap.** Exo Ape's work blocks come alive as motion the instant the cursor lands: `.block:hover .image{bottom:1px; height:calc(100% - 2px); left:1px; right:1px; top:1px; width:calc(100% - 2px); z-index:1}` insets the still by 1px to reveal a hairline frame, while `.block:hover .video{bottom:0; height:100%; left:0; right:0; top:0; width:100%; z-index:2}` expands the video full-bleed above it `[CSS-verified]`.

### Nav items and the nav bar surface

Nav items ride the same underline-draw as body links; none takes a fill.

For the bar itself, two winner patterns and never the AI border-bottom:

- **Transparent → same-family glass.** Transparent over the hero, then a low-alpha same-family tint plus `backdrop-filter: blur()` once content scrolls under it. Arc and Granola both ship the machinery; Granola's header is `position: fixed` and transparent at the top, and the only line it defines is a **same-family hairline `#E3E3E3`** held at `0px` width at the top — a low-contrast divider, not an accent bar `[CSS-verified]`.
- **Solid same-bg bar.** Cyd's header is `position: sticky`, `background: #FFF5EE` — the exact page cream, fully opaque — with `border-bottom: none` `[CSS-verified]`. A legitimate glass-free alternative when the palette is a single warm ground.

A contrasting accent `border-bottom` is absent everywhere: Arc and Exo Ape carry no border-bottom at all, Granola's is a same-family hairline, Cyd's is none. Two winners (Exo Ape, Cyd) plus two style anchors (Arc, Granola) against the AI default.

### Motion and scroll

- **Native scroll-driven reveal.** `animation-timeline: view()` reveals, guaranteed off the main thread. Present in the authored CSS of Cyd, Arc, and Granola `[CSS-verified — one winner (Cyd) plus two style anchors]`. This is the archetype's default reveal, not a JS observer.
- **Cinematic camera scrub.** A pinned canvas with the scene scrubbed to scroll, driven by hand-tuned eases rather than a linear parallax. Published parameters `(technique, Codrops "Cinematic 3D Scroll with GSAP", Nov 2025)`: custom eases `cinematicSilk 0.45,0.05,0.55,0.95`, `cinematicSmooth 0.25,0.1,0.25,1`, `cinematicFlow 0.33,0,0.2,1`, `cinematicLinear 0.4,0,0.6,1`; `ScrollSmoother { smooth: 4, smoothTouch: 0.1 }`; camera timeline `scrub: 1`, `start: "top top"`, `end: "bottom bottom"`, container `500vh–900vh`; text-overlay scrub `0.5–0.8`. Igloo corroborates the pinned-scene approach `[case-study]`. **Where it fits.** Pages where a real 3D scene carries the story, never as decor.
- **Chromatic scene dissolve.** Between full-screen scenes, transition through chromatic aberration plus displacement plus a frost dissolve rather than a cut or a fade. Igloo `[case-study, single-source]`. The transferable idea: transition on a material property, not on opacity.
- **View-Transition page nav with radius morph.** Route changes animate a rounded-inset clip so the shape, not just the opacity, carries between pages: `::view-transition-old(...) { clip-path: inset(0 round var(--border-radius-from)) }` `[CSS-verified, Cyd]`.
- **Reveal distance.** Where a fade-up is used, keep it small and add a blur-in for depth — `translateY(40px) scale(.97) blur(4px) → 0`. No verified winner throws further than 40px.

### Text effects

- **Bespoke display as the artwork.** The signature is the typeface and the scale, before any motion. Exo Ape sets display in **Times**, Granola in bespoke **Melange**, Cyd in bespoke condensed **Bueno-VF**, Arc in bespoke **Marlin** `[all CSS-verified — two winners (Exo Ape, Cyd) plus two style anchors]`. Rotate off the overexposed kit sans; the display face is the identity.
- **Per-char scrub reveal** — signature, hero only. SplitText chars stagger in on scroll. Published parameters `(technique)`: `stagger: 0.02`, `duration: 0.25→0.2`, `ease: power2.out` entering and `power2.in` exiting, section hold `0.5–1.0`, section scrub `0.5`. Behaviorally corroborated by Sculpting Harmony's kinetic type `[case-study]`. **Where it fits.** One or two hero lines, no further.
- **Shader text scramble** — signature for WebGL builds. Glitch and scramble by offsetting an **SDF texture** rather than mutating the DOM, which avoids layout recalculation. Igloo `[case-study, single-source]`.
- **Variable-font scroll-morph** — verified on a winner, on the `ytuc` optical axis rather than `wght` or `wdth`. See Mid-page aliveness.

### Cursor and pointer

Custom cursor is a *choice*, and the default cursor is a legitimate, deliberate signature.

- **Custom cursor element.** Present on Exo Ape (`DIV.cursor`) and Granola `[CSS-verified — one winner (Exo Ape) plus one style anchor]`. **Where it fits.** Image- or scene-forward sites where the cursor becomes a label — "view", "drag", play/pause.
- **Deliberate default cursor.** Cyd, an SOTD winner, ships **no** custom cursor element and leans on the system pointer while the interaction lives in the button displacement and the View Transitions `[CSS-verified]`. Single-source, but a strong permission: on a text- or editorial-leaning organic build, the OS cursor is correct.
- **Magnetic pull** was not verified in authored CSS on any corpus site. It stands optional, never a default.

### Loader effects

- **Intro folds into the scene.** The load *is* the opening shot; a real-time rendered intro "flows seamlessly into the rest of the experience", so there is no separate loader screen. Igloo `[case-study, single-source]`. The transferable principle: to mask asset load, animate the hero's own first state rather than overlaying a spinner.
- **Instant paint plus scroll-driven entrance.** No heavy preloader on Arc or Granola; the entrance rides the `animation-timeline: view()` reveals already in the CSS `[CSS-verified — two style anchors, no winner]`.
- **A composed opening line.** Exo Ape's `P.intro` carries the opening statement over the first-fold photograph.

### Composition — how variety coheres

**Cyd Stumpel — warm editorial-organic.** One voice made of a warm cream ground, a single accent, fat rounded geometry (64px pills, radius-morph), and View-Transition continuity. Each class varies the *mechanism*, never the palette or the easing:

| Element | Mechanism |
|---|---|
| Button | accent-displacement push — negligible 5% tint, text→accent, `translate(-2px,2px)`, hard 1px accent offset-shadow |
| Text / utility link | 10% accent wash, `translateY(-1px)`, arrow `translate(2px,-2px)` — same accent, lighter touch, no displacement shadow |
| Image / work tile | border-radius morph, circle→full-image crossfade, caption slide-up — no accent at all; the geometry carries it |
| Nav | solid same-cream sticky bar, no border, no glass — the chrome stays silent so the tiles speak |

The glue is one easing table driving everything: `--default-duration: 1.3s`, `--default-ease: var(--ease-out-quart)` = `cubic-bezier(0.25,1,0.5,1)`, `--bouncy-ease: cubic-bezier(0.34,1.56,0.64,1)` for interactives, plus `--ease-in-back: cubic-bezier(0.36,0,0.66,-0.56)` and `--ease-out-back: cubic-bezier(0.34,1.56,0.64,1)` for the route morphs `[CSS-verified]`. Same accent token, same radius language, same clock — four different mechanisms cohere. A cutting-edge grace note: avatars fan out via `translateX(calc(-1.15em * sibling-index()))`.

**Granola — productivity with personality** `[CSS-verified style anchor]`. One voice made of the bespoke serif Melange, an "oats" warm token family, soft-opaque glass tokens, and organic `clip-path` sections. Variation is encoded in the **token names**, so no element improvises a colour: the primary CTA is one solid dark pill, the single loud element; group-hover fills on cards and list rows resolve to `--color-fill-soft-opaque-hover` or `oats-green-300→400`, a one-step same-family darkening; the nav is fixed-transparent into a same-family hairline plus backdrop-filter glass; sections use organic `clip-path` edges instead of hard rectangles. Coherence comes from the token layer, not from repeating one effect.

**The transferable rule.** Cohesion is a *shared substrate* — one accent token, one easing table, one radius language, one type face — under **class-specific mechanisms**: displacement for buttons, draw for links, morph for images, silence or glass for nav. The AI failure is the inverse: one mechanism copied onto every class over an unshared, ad-hoc palette.

### Anti-signals — absent from every winner examined

- **Pale, washed-out tint fill sweep on buttons.** Zero sites use it as the primary hover. There is no middle-pastel wash anywhere: fills are either negligible (5%, carried by displacement) or committed (80–100%, or a one-step `-hover` token).
- **Contrasting accent `border-bottom` under the nav on scroll.** Zero.
- **One universal hover across all element classes.**
- **Reflexive circle-follower cursor and magnetic-everything.**
- **Full-screen spinner or `0→100%` preloader gate.**
- **Blanket 40px+ fade-up parallax on every section.**
- **Static PNG grain and flat decorative drop-shadows for depth.** The archetype earns depth from z-layering, glass refraction, and procedural noise; no corpus site leans on a PNG-grain overlay.

---

## Page recipe

### Named page shapes

**1. The In-Engine World.** The entire page is one continuous WebGL scene. There are no DOM sections and no HTML chrome — the wordmark, manifesto, copyright, scroll cue, and sound toggle are all rendered *inside* the engine as a fixed HUD, and scroll scrubs a real-time simulation. The most extreme spatial-organic expression: depth is literal, not a `backdrop-filter`. Skeleton: `in-engine intro that flows into the scene → scroll-scrubbed 3D narrative → persistent in-engine HUD`. Fits crypto, AI, and spatial-computing brands, single-hero-object launches, anything where the spectacle *is* the message. Winners: Igloo Inc; Sculpting Harmony as the chaptered, music-synced variant.

**2. The Editorial-Organic Portfolio.** Warm cream ground; an oversized display-wordmark marquee up top; real portrait photography composited onto organic clip-path shapes; mixed condensed-display, serif, and sans type with playful stickers; then a work grid with radius-morph hovers, a writing band, services, and a contact-first footer; native View Transitions carry route changes. Skeleton: `wordmark-marquee hero → role/intro band → selected work (morph tiles) → blogs → services → contact footer`. Fits freelancers, studios with personality, warm-premium brands. Winner: Cyd Stumpel, with Granola and Arc as style anchors for the register.

**3. The Cinematic-Photo Studio.** Full-bleed atmospheric photo or video hero, transparent nav, one intro sentence, an oversized bottom-anchored grotesque display line, a custom cursor; then video-forward proof and a contact-block footer with a real address. Earthy-neutral palette. Skeleton: `photo hero + intro + XXL display → featured work (video) → reel → media → story → contact footer`. Fits design and production studios, premium DTC with cinematic assets. Winner: Exo Ape. **Edges:** Obys collapses the hero into a project index; Aristide runs the same spine in a dark generative-WebGL register.

### Per-winner scroll-throughs

**Igloo Inc — the whole page is one scene.** No DOM sections exist. The document body is `<div id="app"><div id="webgl"><div></div></div><style>…</style></div>`, with zero text nodes and no readable `<canvas>` in the light DOM; `body` and `html` are both `overflow: hidden`, so scroll is wheel-hijacked and scrubs a real-time simulation instead of translating a document. Attention and understanding fuse — the spectacle is the message — and proof and close are absent from the observed fold. Climax is the igloo fully assembled with a dark entrance; rest is the ambient snow-terrain drift between scroll inputs.

**Cyd Stumpel — editorial-organic portfolio.** The homepage is assembled from ACF blocks (`homepage-header`, `selected-work`, `latest-blog-posts`, `link-list`, plus `text-with-media` / `media-row` / `cards`), in this order. Intensity is a comparative 1–10 estimate of attention load (defined in `../winners/composition-chains.md`):

1. **Hero** (`homepage-header`) — attention — a full-width repeating display-wordmark marquee (overflow-x) into a utility row (nav-logo, email link, availability) and serif nav, then an editorial portrait on an organic red clip-path blob beside an oversized serif role headline and bouncy SVG stickers. Type-as-image plus a real portrait. Intensity 9.
2. **Role band** — understanding — cycling role headlines: Freelance Developer / Creative Engineer / Conference Speaker / Parttime Lecturer / Front end Consultant. Intensity 5.
3. **Selected work** (`selected-work`) — proof — `.work-thumb` tiles (Rotgans Media House, Club NAR) on a 12-column subgrid with radius-morph hover and `.serif` + `.sans` captions. Intensity 7.
4. **Latest blogs** (`latest-blog-posts`) — writing cards. Intensity 4.
5. **Services** (`link-list`) — Web Development / Consultancy / Speaking. Intensity 5.
6. **Footer** — close — "Available October 2026", the work-days and teaching schedule, "Have a project in mind?", a copy-email CTA. Intensity 6.

Seams are organic clip-path top edges (`--clip-top: 6.9444vw`); route changes run through View Transitions.

**Exo Ape — cinematic-photo studio.** `Hero (full-bleed photo + intro + XXL display) → The Studio → Work / Featured Projects (video tiles, "Browse all work") → Work in motion / Reel → In the media / Spread the News → Our Story → contact footer`. Media-forward: 8 `<video>`, 0 `<canvas>`, custom cursor throughout. Intensity arc: hero 9 → featured 8 → reel 8 → media 4 → story 5 → footer 5.

**Obys — index-first.** No hero headline. Nav (Work, About) → a project index whose length reads two ways — a logical `01→19` list against counters running to 25 in the raw HTML, unreconciled because the WebGL index duplicates its rows 3× for the marquee ([`../winners/studio-obys.md`](../winners/studio-obys.md)) — each a name plus category and service tags, with a persistent view-mode toggle ("Vertical, Horizontal, Grid") and a CET clock → footer with a studio statement, `info@obys.agency`, "©2026 Obys". The index is the page; proof by portfolio density.

**Aristide Benoist — dark generative.** A dark monochrome canvas hero (2 `<canvas>`) with a horizontal filmstrip of thin vertical image slats, the `ARISTIDE` wordmark horizontal at top-left, and a ruler-tick scrubber strip → a numbered project index (01/30 … 30/30, each "EXPLORE") → clients wall → awards ledger → contact stack (EMAIL / INSTAGRAM / TWITTER / LINKEDIN / GITHUB). Pure black, greyscale imagery.

**Sculpting Harmony — chaptered WebGL exhibition** `(media-only)`. A real-time Gehry sketch intro → a chaptered scroll narrative broken by poster-like introductions of materials imagery and text, each chapter its own colour; kinetic condensed type stretches, squeezes, and dances to LA Phil musical extracts; 3D study models can be tilted and panned; the cursor trails Gehry quotes.

### Hero architectures

**A. The In-Engine Fold** (Igloo). No HTML hero — the first fold *is* the live 3D scene. Corners carry a monospace HUD baked into the engine: wordmark top-left, "Manifesto" plus mission copy top-right, "Scroll down to discover" and "Sound: Off" bottom-left, a live node-graph drawn over the object. **No CTA button.** The H1 is the wordmark, not a headline. Entrance: the scene paints, the hero object idles as a luminous ice core, the HUD is present from frame zero because it is the same engine, the node-graph animates live values, and scroll begins the object's assembly.

**B. The Wordmark-Marquee plus Portrait Fold** (Cyd Stumpel). Top is a full-width repeating display wordmark strip in Bueno-VF at a `clamp`-driven display scale, roughly 167px; row two is a small "CYD" nav-logo left, with `info@cydstumpel.nl`, "Available October 2026", and a serif nav right; the hero body is a real portrait on an organic red clip-path blob beside an oversized serif role headline in italic and roman, with bouncy SVG stickers. **No fill CTA in the fold** — an email link and nav only.

| Element | Order | Transform | Duration | Delay | Easing |
|---|---|---|---|---|---|
| sticker (badge) | 1 | `@keyframes scale-in{0%{scale:0}100%{scale:1}}` | 0.4s | `--medium-delay` 0.2s | `--bouncy-ease` `cubic-bezier(0.34,1.56,0.64,1)` |
| sticker-1 (planet) | 2 | `move-right-1` | 1s | 0 | `--default-ease` (ease-out-quart) |
| sticker-1 on scroll | — | retimed to scroll via `animation-timeline: --page-title` | — | range `entry 100lvh entry 150lvh` | — |
| titles grid | — | `align-self: end`, `overflow: clip` | — | delays lengthen on View-Transition nav | — |

The scroll retiming consumes a named timeline through `animation-timeline`, and the `view-timeline-name` defined on the header is `--homepage-header`.

**C. The Full-Bleed Photo plus Bottom-Display Fold** (Exo Ape). A full-bleed cinematic blue-hour photo or video; a transparent nav pairing the `exo` grotesque with the `ape` italic serif wordmark on the left against Work/Studio/News/Contact on the right; an intro paragraph upper-left in Lausanne grotesque; an **oversized bottom-anchored display H1** stacking three words — `Digital / Design / Experience` — in `Lausanne-300`, computed at `208.333px` on desktop; "Scroll to explore" bottom-right; a custom `DIV.cursor` follower. The type token `--font-s-h0` is authored at `25.6vw` and responsively overridden to `17.3611vw` at desktop, which is where the 208px lands — both figures are real but never at the same viewport.

**The shared law: no hero object carries a filled CTA button in the fold.** The fold sells with the scene, the photo, or the type; the call to act is a scroll cue or an email link.

### Loader in the page sequence

Ranked by how the winners actually ship:

1. **No boundary — the intro is the scene.** Igloo's real-time in-engine intro flows straight into the world; the HUD is present from the first painted frame; a single JS bundle renders WebGL into `#webgl` with no preloader DOM.
2. **Component-level entrance.** Cyd paints instantly — no full-screen preloader block exists in the authored CSS — and the entrance is carried by the bouncy sticker `scale-in`, a pixel-art box-opening illustration, and scroll-driven `animation-timeline` reveals. Absence as data: an SOTD winner ships no `0→100%` gate.
3. **A composed sentence or a line-draw as the opening beat.** Exo Ape's `P.intro` over the hero photo; Sculpting Harmony's introductory page drawing a Gehry sketch in real time before handing into chapter one.

None uses a spinner or a numeric counter.

### Route transitions

**Cyd Stumpel — View Transitions** `(winner-verified, from view-transitions.css)`. The mechanism is the JavaScript API plus pseudo-element rules, not the MPA opt-in at-rule: `document.startViewTransition(...)` in the bundle drives **63** `::view-transition-old` / `-new` / `-group` rules (25 / 20 / 18). Named groups: `main`, `header`, `page-content`, `homepage-header`, plus `page-title`, `selected-work`, `footer`. The signature is a **shared-element morph on `.work-thumb`**: `[data-view-transition*=to-normal] .work-thumb{view-transition-name:var(--vt); view-transition-class:work-thumb}`, morphing across home ↔ archive ↔ work-detail with `--thumb-radius: 8.3333vw` on mobile and `50%` under `@media (hover:hover) and (min-width:768px)`. `page-title` swaps via `title-to-up` on `--ease-in-back` exiting and `title-from-down` on `--ease-out-back` entering. `::view-transition-group(main)` cross-fades on `--default-ease`, delayed by `--fade-out-time`, over `--get-in-place-time`. Timing tokens: `--default-duration: 1.3s`, `--get-in-place-time: 0.5s`, `--fade-out-time: 0.3s`. The transition language **rhymes with the entrance** — the same ease-out-quart and the same back-ease that drive the bouncy hero stickers.

Obys's "Vertical / Horizontal / Grid" toggle is a within-page layout transition, not a route curtain. Igloo, Exo Ape, Aristide, and Sculpting Harmony are single-page scroll experiences.

### Copy voice

**Igloo** `(shipped — text is baked into the WebGL scene, so read from the render, not the DOM)`: `IGLOO` · `// Copyright © 2026 Igloo, Inc. All Rights Reserved.` · `////// Manifesto` · `Our mission is to build the next generation of consumer brands at the intersection of Community, AI, and crypto.` · `Scroll down to discover.` · `Sound: Off`. Manifesto register, first-person-plural, monospace-terminal punctuation, declarative. Refuses pricing, features, buttons.

**Cyd Stumpel** `(winner-verified DOM and render)`: H1 `CYD STUMPEL` — CSS-uppercased from a DOM source case of "Cyd Stumpel"; role headlines `Freelance Developer`, `Creative Engineer`, `Conference Speaker`, `Parttime Lecturer`, `Front end Consultant`; utility `info@cydstumpel.nl` and `Available October 2026`; the body opens `I'm a creative developer & teacher from…`; stickers `AWARD WINNING DEVELOPER` (purple) and `MOTION WEB DESIGN` (blue), which are outlined-SVG graphics rather than DOM text; footer `Have a project in mind?`, `Copy email info@cydstumpel.nl`, `All work`. First-person, plain, warm, playful; short noun-phrase roles; lowercase email; availability stated openly; self-promotion only through ironic stickers.

**Exo Ape** `(winner-verified)`: intro `Global digital design studio partnering with brands and businesses that create exceptional experiences where people live, work, and unwind.`; H1 `Digital Design Experience` stacked; sections `The Studio` / `Featured Projects` / `Work in motion` / `In the media` / `Our Story`; CTAs `Browse all work` / `Browse all news`; microcopy `Scroll to explore`; footer address `Willem II Singel 8, 6041 HS, Roermond, The Netherlands` — rendered across three lines — plus `hello@exoape.com` and phone `+31 772 086 200`. Third-person institutional, one long atmospheric intro sentence, warm verbs, Title-Case section labels, imperative CTAs. Refuses hype adjectives and first-person.

**Obys** `(winner-verified DOM)`: footer `The studio is shaped by people who care deeply about design and the process behind. Each project becomes a case study and a meaningful part of our portfolio, developed with care and attention.` · `info@obys.agency` · `All rights reserved. ©2026 Obys`; view labels `Vertical, Horizontal, Grid`; nav `Work` / `About`. Understated third-person studio voice, process-oriented, no tagline, no hero headline.

**Aristide Benoist** `(winner-verified post-JS DOM)`: `Aristide Benoist — Independent developer`; index entries rendering as separate numbers and per-character letters — `01`, `30`, `h o u s e o f G u c c I` — with the ` / ` slash a visual layout artifact rather than a DOM substring, and a capital `I` closing the title; each entry carries `EXPLORE`; utility `INDEPENDENT DEVELOPER` / `AVAILABLE APR. 2023`; awards ledger reading number-before-label, `30 SITE OF THE DAY` / `3 SITE OF THE MONTH` / `2 INDEPENDENT OF THE YEAR`; footer `ALL RIGHTS RESERVED ARISTIDE BENOIST 2026®`. Terse all-caps utility labels, numeric and indexical, award ledger as proof. Refuses adjectives and sentences.

**Sculpting Harmony** `(media-only; a design-director quote, not site copy)`: Bruno Arizio — `Our intention was not to follow a certain style, but to capture a feeling`.

**Voice formula.** Person splits by author: product or brand → first-person-plural manifesto; studio → third-person institutional; solo practitioner → first-person plus all-caps utility labels. Sentence length is one long atmospheric sentence for the intro and short noun-phrase labels everywhere else. Verbs stay warm and human — "live, work, and unwind", "care deeply", "capture a feeling" — never the leverage/unlock register. Punctuation carries monospace terminal marks in the WebGL register and em-dash plus slash-indexing in the portfolios. The line refuses hype adjectives, pricing, feature lists, and exclamation marks, and states availability plainly.

### Imagery art direction

- **Exo Ape** — cinematic architectural and landscape photography plus video; blue-hour and golden atmospheric grade, desaturated, full-bleed. One treatment page-wide, framed by a sand-neutral palette (`--color-sand: #e0ccbb`). 8 videos, 0 canvas, never stock.
- **Cyd Stumpel** — real editorial portrait photography, warm-graded, composited onto organic red clip-path shapes, layered with pixel-art and sticker graphics. A deliberately *split* treatment: photo, illustration, and type-as-image coexist.
- **Igloo** — fully synthetic: monochrome ice and snow WebGL render, luminous ice blocks over greyscale terrain in atmospheric fog. One in-engine grade.
- **Aristide** — greyscale fashion and architecture photography sliced into thin vertical bands over pure black; high-contrast, desaturated. One dark treatment page-wide.
- **Sculpting Harmony** — archival sketches, study models, and materials photography plus interactive 3D models; pop-colour chapter grades; poster-like material introductions between chapters `(media-only)`.

The formula: real photography, in-engine render, or archival material — never stock. Either one atmospheric single-grade per page, or a deliberate split into photo plus illustration plus type-as-image. Palette earthy-desaturated or monochrome; organic clip-path crops replace rectangular frames.

### Footer

- **Cyd Stumpel** — a designed **contact-first** moment: "Have a project in mind?", availability, the work-days and teaching schedule, a copy-email CTA. Section edges use the organic clip-path (`--clip-top: 6.9444vw`), and the contact CTA is the accent-displacement pill — `translate(-2px,2px)` with `box-shadow: -1px 1px 0 var(--color-accent)` at 64px radius.
- **Exo Ape** — a contact block: real address, `hello@exoape.com`, phone `+31 772 086 200`, socials (Behance, Dribbble, LinkedIn, Instagram), and footer nav (Work, Studio, News, Contact).
- **Obys** — an index-tabular footer: studio statement, email, copyright, with the view-mode toggle and a CET clock as persistent chrome.
- **Aristide** — tabular contact plus proof: a socials stack, a clients wall (Netflix, Google, Obama Foundation, Twitch, Bear Grylls, MGM Studios), and the awards ledger.
- **Igloo** — in-engine: the copyright line baked into the HUD bottom-left; no DOM footer.

Spatial-organic footers are contact-first, availability-forward designed moments, or an in-engine copyright HUD. None ships a fat multi-column sitemap.

### Spectacle — the passage a judge replays

- **Igloo — the scroll-assembled igloo.** Scattered luminous ice blocks lock into a dome as you scroll over a monochrome snow plain, with a live node-graph drawn over the structure (28 / 27 / 40 / 21 / 27 on the captured frame) and the entrance opening as a dark aperture. Replayable because it is a physical build reacting to your scroll and the entire UI lives inside it. The Site of the Year 2024 centerpiece, Animations/Transitions 9.60.
- **Cyd Stumpel — the work-thumb that becomes the next page.** On hover the tile radius morphs rounder to 50%, a resting circle graphic crossfades to the full image, and the caption slides up (`opacity .2s .1s`, `border-radius .2s .1s var(--default-ease)`); on click that *same* `.work-thumb` morphs across a View Transition into the project page. Continuity: the tile you touched is the tile that becomes the route. Replayable because geometry, not decoration, carries it.
- **Sculpting Harmony — type that dances to the orchestra** `(media-only)`. The bold condensed typeface stretches and squeezes and "dances to the crescendoing music of the LA Philharmonic", chapter colours shifting, while Gehry's 3D study models tilt and pan and the cursor trails Gehry's own quotes.
- **Exo Ape — XXL display over cinematic film.** The oversized bottom-anchored grotesque line over a full-bleed blue-hour scene, the custom cursor gliding, project films revealing on scroll behind the type.
- **Aristide — the sliced filmstrip.** A horizontal row of thin vertical greyscale image slats that expand and scrub over pure black, WebGL-driven with a ruler-tick scrubber.

The judge's single-replay picks: Igloo's in-engine assembly and Sculpting Harmony's music-synced kinetic type.

### Design tokens read live

**Cyd Stumpel** — `--default-ease: var(--ease-out-quart)` = `cubic-bezier(0.25,1,0.5,1)`; `--bouncy-ease: cubic-bezier(0.34,1.56,0.64,1)`; `--color-background: seashell`; `--highlight-color: #e2fc91`; `--clip-top: 6.9444vw`; `--border-radius: 0.5rem`; `--header-height: 6.25rem`; H1 in `Bueno-VF` variable display, uppercase. The ease table holds **30** unique `--ease-*: cubic-bezier(...)` definitions, 32 counting named aliases. On `--color-accent`, see Refuted.

**Exo Ape** — `--color-story: #070707`, `--color-dark-grey: #0d0e13`, `--color-light-grey: #e4e0db`, `--color-sand: #e0ccbb`, `--color-off-white: #f8f8f8`; display in `Lausanne-300/400/500` plus `Times` serif; fluid type scale `--font-s-h0` authored at `25.6vw`.

### Page-level anti-signals

No winner in this line opens on a bento or card grid — the fold is a single hero object, a full-bleed photo, or a display-wordmark marquee, never a tile matrix. None ships a full-screen `0→100%` preloader gate, a contrasting accent `border-bottom` under the nav on scroll, a fat multi-column sitemap footer, a filled CTA button in the fold, stock photography, a neon or corporate-blue system palette, or one universal hover copied across every element class.

---

## Mid-page aliveness

One structural fact frames everything: **Igloo, the head of the corpus, ships no mid-page prose at all.** The middle *is* a scroll-scrubbed real-time simulation. The line's most extreme answer to dead prose is to ship no prose. The sites that *do* keep prose — Cyd, Exo, and the quiet SaaS anchors — are where the reusable technique lives.

The line's defining mid-page channel differs from every other archetype: **native CSS scroll-driven animation** (`animation-timeline: view()` and `scroll(root)` with named `view-timeline-name`), not GSAP ScrollTrigger scrub. Where the immersive line welds decor to scroll with JS, spatial-organic reaches for the browser's own timeline API. The native-first DNA shows up literally in the mid-page code.

### Channel A — the native scroll-driven layer

- **Cyd variable-font scroll-morph** `(winner-verified)`:

  ```css
  .page-title__title { font-variation-settings:"ytuc" 80;
                       animation-timeline: --page-title;
                       animation-range: entry 100lvh entry 115lvh;
                       animation-name: vf-size-title }
  .footer__logo      { animation-timeline: --footer;
                       animation-name: vf-size;
                       font-variation-settings:"ytuc" 100;
                       animation-range: var(--footer-scroll-range) }
  @keyframes vf-size { from { font-variation-settings:"ytuc" 100 }
                       to   { font-variation-settings:"ytuc" 0; transform: translateY(0.2em) } }
  ```

  A variable-font optical axis morphs as the title and footer wordmark scroll through their view-ranges — scroll-linked, native, reversible. The axis is `ytuc`, not `wght` or `wdth`.
- **The timeline inventory** `(winner-verified)`. `view-timeline-name` is declared exactly four times: `--footer`, `--footer-page-title`, `--page-title`, `--scroll-wrapper`. `timeline-scope` appears only in JS, set on the document element to `--page-title, --footer-page-title`. Eleven `@supports(animation-timeline: view(y))` guards (twelve counting all variants) gate the system — base state visible, pre-animation state living only inside the guard.
- **Granola native parallax and scroll-fill** `(winner-verified CSS, style anchor)`. `.sticky-demo-preview{animation: shrink-to-sticky-sm linear both; animation-timeline: scroll(root); animation-range: 0 100vh}` shrinks the product demo as you scroll; `.video-call-parallax{animation-timeline: scroll(root); animation-range: 0 120vh}`; `.floating-item{animation-timeline: scroll(root), scroll(root); animation-range: 0 50vh, 60vh 80vh}` floats on two axes; the "how it works" steps fill through named view-timelines, `.hiw-step-fill-0/1/2{animation-timeline: --hiw-step-0/1/2}`. Granola runs **13** `animation-timeline` declarations in total. Even the quiet SaaS register builds its mid-page motion natively.

### Channel B — the idle ambient band

- **Cyd** `(winner-verified)`: `@keyframes breathe{0%,100%{translate:0 0}50%{translate:0 -0.15em}}` running `5s var(--default-ease) infinite` on a mid-page folder image entered with `fromFolder 2s var(--ease-in-elastic) forwards`, and `@keyframes ticker{from{transform:translateX(0)}to{transform:translateX(-20%)}}` at `20s linear infinite` — a wordmark marquee that never stops.
- **Granola** `(winner-verified CSS)`: a per-letter cycle through the brand palette, `@keyframes chromaColor{0%{color:#fff}25%{color:#febe29}40%{color:#ff91e0}55%{color:#cebef8}70%{color:#d1e043}to{color:#fff}}`, combined on `.generating-muted-wave-letter{animation: chromaColorMuted 4s ease-in-out infinite, chromaGeneratingLetterWave 2.5s ease-in-out infinite}` where `chromaGeneratingLetterWave` adds a `translateY(-1.25px)` per-letter rise, plus a `chromaGenerateIdleSweepLoop 2.2s linear infinite` shimmer on a label pseudo-element. Also `dancing-bar-top-1/2/3` and `-bottom-1/2/3` (six audio-viz bars), `float-explosion-lg/sm`, `float-green-lg/sm`, `bg-slide`. The idle layer is loud in code and quiet on screen — a 1.25px rise in muted colours.
- **Exo and Igloo** `(shipped)`: Exo's idle band is eight looping films plus the WebGL layer — its inline sheet contains zero CSS `@keyframes`, so the ambient is entirely JS and WebGL. Igloo's is the running simulation plus the live node-graph.

This is the one archetype where **several idle channels running between inputs is canon**, not an accent. A build whose middle freezes between scroll and hover is off-archetype.

### Channel C — interactive figure treatments

The content-section workhorse: Cyd's radius-morph work-thumb and Exo's still→video swap, both quoted in the Effect palette. Geometry and footage carry them; neither uses an accent colour.

### Channel D — fire-once masked reveals on sparse headings

- **Exo** `(winner-verified)`: GSAP SplitText with `type:"lines"` and `linesClass` — one line-masked heading reveal, one split instance, and `Observer` ×11 for directional scroll. Cleaner than character confetti.
- **Cyd** `(winner-verified)`: the current theme ships **no SplitText at all** — `splittext` counts zero in the bundle. Heading and section reveals run through native `animation-timeline: view()`, including a scroll-drawn header underline, `@keyframes header-underline{from{clip-path:inset(0 100% 0 0)}to{clip-path:inset(0 0 0 0)}}`. The line's text reveals are moving away from JS character-splitting toward native scroll-driven draws.

### Channel E — section seams and route transitions

Cyd's View-Transition system carries the section-to-page hand-off as a branded morph rather than a cut, and organic `clip-path` section edges (`@keyframes clip-to-footer`, `clip-down`) shape the seams. The header underline draws in on `animation-timeline: view()` as the header crosses the fold — even the nav boundary is a scroll-drawn reveal.

**Net.** The spatial-organic middle is kept alive by native scroll-driven parallax, reveal, and variable-font morphs; a multi-channel idle band; interactive figures that answer the cursor; fire-once line reveals on the few headings; and shaped seams with View-Transition route morphs. Only one of those five touches text, and even it is drifting native. Dead prose is a symptom of building the middle out of static prose instead of these channels — and specifically of using JS where this line uses `animation-timeline`.

### Hover on text specifically

The tier ships hover on links and figures, and almost nothing on non-link text. Consistent across two winners and the quiet anchor.

- **Link underline draw — the one text-hover the line ships**, in two materials: Exo's pseudo-element scale-draw, identical across nav, list, and footer links; and Cyd's `background-size` gradient material, animatable in height, with a tooltip fading in alongside on mouse hover.
- **No bespoke hover on headings, prose, list rows, or numbers.** Verified absent on Cyd, where every text `:hover` is either an `a:hover` (`text-underline-offset:.1em`) or a figure or container. Verified absent on Granola, whose genuine hovers are Tailwind `group-hover:scale-105`, `group-hover:translate-x-full`, and `group-hover:scale-100` on cards — its 204 `:hover` rules are inflated by an embedded `react-tweet` widget (`.tweet-header` ×29, `.tweet-container` ×7), not by Granola's own copy. No colour-sweep along text, no weight or optical-size shift on hover, no per-char rise on hover, no background highlight on a heading anywhere in the read corpus.
- **Where per-char and variable-font text motion actually lives:** not on hover. It is either **idle-looped** (Granola's `chromaColor` per-letter wave, running forever at 4s inside a product mockup) or **scroll-linked** (Cyd's `ytuc`-axis morph on the page title and footer logo, welded to a view-timeline). The line moves letters and font axes with scroll and time, never with the pointer.

If a build needs text alive in the prose zone here, the answer is a link underline draw where there are links, plus a scroll-linked variable-font axis morph or a slow idle per-letter loop at sub-2px amplitude on the display words. A per-word hover emphasis-sweep on prose is an editorial or minimalist move and is absent from this line.

### Re-fire behavior — content persists, decor reverses

The tier obeys the law precisely, and the archetype's twist is that the reversible channel is largely native.

**Fire-once content.** Exo configures its ScrollTrigger reveals with `once:` (one occurrence), with `scrub` and `toggleActions` both counting zero in the bundle — images and headings reveal once and persist. Cyd uses `toggleActions: "play"` (one occurrence): play on enter, with the leave, enterBack, and leaveBack slots omitted, so no reverse.

**Reversible decor.** Cyd's native `animation-timeline` channels — the page-title and footer morphs, the header underline draw — are welded to scroll position, so driving up and down re-plays them continuously, alongside a GSAP `scrub` channel (four occurrences) and a custom `scrubDuration`. Granola's every `animation-timeline: scroll(root)` and `--hiw-step-N` timeline is scrubbed to the scrollbar, reversible by construction. Exo's reversible channel is a custom lerp and rAF loop feeding the WebGL scene and parallax off a continuously-smoothed scroll value.

On a repeated up-and-down drive, headings and gallery images stay revealed while the parallax, the `ytuc` axis morph, the step-fills, and the WebGL camera all move continuously with scroll. No violation found.

The distinctive point against the immersive line: immersive achieves reversible decor with dozens of GSAP `scrub:` channels; **spatial-organic achieves it with native `animation-timeline`**. Cyd's eleven `@supports` guards and Granola's thirteen declarations do the work GSAP scrub does elsewhere. Native-first is not just the hero DNA; it is the re-fire layer.

### Smooth scroll — register-dependent, not universal

This is where spatial-organic diverges from the immersive line.

- **Studio, portfolio, and experience builds smooth the wheel.** Cyd runs **Lenis** — 28 lowercase `lenis` references plus the full inlined library with `data-lenis-prevent*` attributes, instantiated through a `window.lenis` singleton guard — with `ScrollSmoother` present three times, atop GSAP `(winner-verified)`. Exo Ape rolls its own **custom lerp** (`lerp(` plus a rAF loop, `Raf(` ×3) with `lenis` and `locomotive` both at zero, so the scroll value drives the scene directly. Igloo scroll-scrubs the simulation itself `(shipped)`.
- **The quiet SaaS register does not smooth the wheel.** Granola ships **no smoothing library**; the only `SmoothScroll` token in the bundle is a `handleSmoothScroll` anchor helper using `scrollIntoView()` and `window.scrollTo`. The wheel is native and the mid-page motion comes from native `scroll()` and `view()` timelines instead `(winner-verified)`. Arc is a client-rendered SPA with no smoothing library in the critical shell.

Portfolio and experience builds reach for Lenis or a bespoke lerp; productivity and marketing builds stay native. An un-smoothed wheel is *not* an anti-signal in this line the way it is in immersive — native `animation-timeline` works on the raw scroll position regardless. The real tell runs the other way: a quiet spatial-organic build that bolts Lenis on and then does all its motion with JS ScrollTrigger has imported the immersive stack instead of the archetype's native one.

### Tier anti-signals — what the winners do not do mid-page

- **No scroll-linked emphasis-fill on prose.** The per-word dim→bright accent sweep that carries editorial copy is an editorial and minimalist signature, absent here.
- **No bespoke hover on non-link text.** Text motion is scroll-linked or idle-looped, never pointer-driven, on non-link registers.
- **No per-char SplitText confetti as the reveal.** Exo uses `type:"lines"`; Cyd's current theme dropped SplitText entirely.
- **No JS-only decor where native fits.** A build that ignores native scroll-driven animation is off-archetype for spatial-organic specifically.
- **No frozen middle.** The idle band never stops. A section that goes fully static between inputs breaks the archetype's atmosphere.

---

## Refuted

- **"Cyd's blog cards reveal through `--card-0/1/2` view-timelines"** — false: in the cited stylesheet and bundle version, `timeline-scope` is **absent from the CSS** (its only occurrence is a JS `setProperty` on the document element, set to `--page-title, --footer-page-title`), `--card-0` / `--card-1` / `--card-2` sit at **zero occurrences** anywhere, and `view-timeline-name` is declared exactly four times, none of them a card. No blog or journal rule carries any timeline. The channel's finding survives on the confirmed variable-font morph; the card artifact and its selectors are struck.
- **"Cyd opts into View Transitions with the `@view-transition` at-rule"** — false: the at-rule has zero occurrences across the theme CSS and JS. The mechanism is the JS API, `document.startViewTransition(...)`, plus 63 `::view-transition-old` / `-new` / `-group` pseudo-element rules. The dedicated stylesheet, the `.work-thumb` shared-element morph, and `--thumb-radius: 50%` are confirmed verbatim.
- **"Cyd ships a 40-entry ease table"** — false: **30** unique `--ease-*: cubic-bezier(...)` definitions, 32 counting the named aliases.
- **"Cyd's hero sticker retimes on `view-timeline: --page-title`"** — false: the declaration is `animation-timeline: --page-title`, consuming a named timeline. `view-timeline: --page-title` is not a valid declaration and a verbatim copy breaks. The `view-timeline-name` defined on the header is `--homepage-header`. The range `entry 100lvh entry 150lvh` and both keyframe animations are correct.
- **"Cyd's `--color-accent` is terracotta `#D9533F`"** — unsettled, and dated: three reads across 9–13 July returned terracotta `#D9533F` with a periwinkle secondary `#8082F8`, then a computed `#d9533f` from `:root`, then `--color-accent: #111111` verbatim from `main.css?v=3303`. The site changed between reads. The most recent verified value is `#111111`; anything hardcoding an accent should re-read it. The footer CTA-pill shadow inherits whichever value is live.
- **"Igloo's body is 220 characters with zero text nodes"** — unsupported at winner-verified, downgraded to observed. One browser read measured `body.innerHTML.length` at exactly 220 with `innerText` empty; a re-measure is impossible without executing the WebGL runtime, and the static shell renders zero characters of server-side body text. The qualitative finding — Igloo ships essentially no mid-page prose and the middle is a scroll-scrubbed WebGL world — is well supported; the precise figure is single-source.
- **"Igloo Inc won Site of the Year 2025"** — false: Igloo's Awwwards entry is SOTD 23 July 2024 with Site of the Year **2024**, confirmed through the developer studio's own announcement. The site page shows no SOTY badge.
- **"Aristide's hero carries a vertical stacked `A R I S T I D E` wordmark"** — false: at initial render the hero wordmark is **horizontal**, top-left. The DOM does contain per-character letters near the About and Close menu, the likely source of the confusion.
- **"Aristide Benoist won SOTM June 2021"** — withdrawn as a refutation: Portfolio 2021 holds **SOTD 24 June 2021** at overall 8.01 **and** SOTM June 2021, the latter carried by a dedicated Awwwards announcement page ([`../winners/studio-unseen-benoist.md`](../winners/studio-unseen-benoist.md)). What survives is the entry mismatch — the entry scored here is a different, earlier one, SOTD 11 October 2017 at 7.37.
- **"obys.agency holds an Awwwards SOTM"** — false: the studio-site entry is **SOTD 04 May 2026 plus a Developer Award**, and the only Obys SOTM in this corpus belongs to `aim.obys.agency`, January 2024 — a different site on a Webflow stack ([`../winners/studio-obys.md`](../winners/studio-obys.md), corroborated by [`../analysis/studio-variance.md`](../analysis/studio-variance.md)). Both readings come from a summarized rendering of the Awwwards profile rather than the individual project pages, a limit that source records itself.
- **"Obys holds CSSDA Studio of the Year ×3"** — false: the count is **4** — 2020, 2021, 2023 and 2024, alongside Awwwards Studio of the Year 2023 ([`../analysis/jury-evidence.md`](../analysis/jury-evidence.md)).
- **"Cyd instantiates Lenis with `new Lenis`"** — false as a literal token: instantiation runs through a `window.lenis` singleton guard inside the bundled minified library. The 28-reference count and the smoothing claim are fully confirmed.
- **"Sculpting Harmony's real-time intro sketch is documented in the cited source"** — false citation, true claim: the cited source does not describe the intro sketch. The Brand Identity does, verbatim — "the introductory page… opens to a sketch of Gehry's coming to life in real-time." The 3D-model tilt and pan is only partly supported: the models are named, the interactivity is not explicit.
- **"Exo Ape's `--font-s-h0: 25.6vw` computes to 208px"** — false as a pairing: both values are real but never at the same viewport. `25.6vw` is the authored base; at desktop the token is overridden to `17.3611vw`, which is where the 208.333px computed size lands.
- **Three quoted strings are formatting reconstructions, not literal substrings.** Exo Ape's footer address renders across three lines rather than one comma-joined string. Aristide's `01 / 30 house of Gucci` is a visual reconstruction — the DOM holds separated numbers and per-character letters with no ` / ` substring, and the final letter is a capital `I`. Cyd's `CYD STUMPEL` is CSS-uppercased from a DOM source case of "Cyd Stumpel", and its stickers are outlined-SVG graphics rather than DOM text.
