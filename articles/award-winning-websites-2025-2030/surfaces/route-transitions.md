---
title: "Route Transitions on Winners — JS-Orchestrated, Never the Native API"
date: "2026-07-30"
author: "Coroboros"
tags: ["route-transitions", "page-transitions", "pjax", "barba", "taxi", "gsap", "gsap-flip", "view-transitions", "nuxt", "nextjs", "webgl", "accessibility", "awwwards"]
sources:
  - "https://cuberto.com/"
  - "https://locomotive.ca"
  - "https://immersive-g.com"
  - "https://truekindskincare.com"
  - "https://siena.film"
  - "https://terminal-industries.com"
  - "https://landonorris.com"
  - "https://dennissnellenberg.com"
  - "https://robin-noguier.com"
  - "https://stefanvitasovic.dev"
  - "https://gabrielcontassot.com"
  - "https://matvoyce.tv"
  - "https://ponpon-mania.com"
  - "https://eloyb.design"
  - "https://activetheory.net"
  - "https://taxi.js.org"
  - "https://github.com/craftedbygc/taxi"
  - "https://barbajs.org"
  - "https://developer.mozilla.org/en-US/docs/Web/API/History/scrollRestoration"
  - "https://gsap.com/docs/v3/Plugins/Flip/"
  - "https://web.dev/baseline/2025"
  - "https://developer.chrome.com/blog/view-transitions-in-2025"
  - "https://www.awwwards.com/sites/cuberto"
  - "https://www.awwwards.com/sites/siena-film-foundation"
  - "https://www.awwwards.com/sites/terminal-industries"
  - "https://www.awwwards.com/sites/lando-norris"
  - "https://www.awwwards.com/annual-awards/winners"
  - "https://www.awwwards.com/sites/stefan-vitasovic-portfolio25"
  - "https://www.awwwards.com/sites/mat-voyce"
  - "https://thefwa.com/cases/mat-voyce"
---

# Route Transitions on Winners — JS-Orchestrated, Never the Native API

Not one of the fifteen sites read live ships the native View Transitions API as its route transition: every route transition in this census is JS-orchestrated. This is the full page recipe for route and page transitions across multi-page award winners: the choreography that plays when the URL changes, distinct from the intro loader (arrival) and from in-page scroll reveals. Archetypes and their canonical winners live in [the parent reference](../award-winning-websites-2025-2030.md).

**Corpus.** Fifteen sites read live: twelve award-verified, three studio exemplars (Locomotive, Immersive Garden, Active Theory) carried for their route machinery. HTML plus linked CSS by `curl`, two JS bundles decompiled by grep, Active Theory driven in a real browser.

Award lines (award, date, score) live in the linked archetype corpus tables.

| Site | Award record | Router / stack | Read |
|---|---|---|---|
| **Cuberto** — cuberto.com | [bold maximal](../archetypes/bold-maximal.md#corpus) | custom SPA (`bundle.js?v=5.5.0b8`) | DOM + CSS |
| **Locomotive** — locomotive.ca | studio exemplar, not award-verified | Barba.js + Locomotive Scroll | DOM + CSS + JS |
| **Immersive Garden** — immersive-g.com | studio exemplar, not award-verified | Nuxt native `pageTransition` | DOM + CSS |
| **Truekind Skincare** — truekindskincare.com | [editorial](../archetypes/editorial.md#corpus) | Nuxt + GSAP Flip | DOM + CSS |
| **Siena Film Foundation** — siena.film | [editorial](../archetypes/editorial.md#corpus) | Taxi.js + GSAP on a Webflow base | DOM + JS |
| **Terminal Industries** — terminal-industries.com | [minimalist](../archetypes/minimalist.md#corpus) | Nuxt native app/page transition | DOM + CSS |
| **Lando Norris** — landonorris.com | [immersive cinematic](../archetypes/immersive-cinematic.md#corpus) | Taxi.js + Rive on a Webflow base | DOM |
| **Dennis Snellenberg** — dennissnellenberg.com | Dev Award, multi-SOTD | Barba.js + Locomotive Scroll | DOM + CSS |
| **Robin Noguier** — robin-noguier.com | portfolio, multi-award | Next.js (pages router) | DOM |
| **Stefan Vitasović** — stefanvitasovic.dev | [minimalist](../archetypes/minimalist.md#corpus) | Next.js | DOM |
| **Gabriel Contassot** — gabrielcontassot.com | [minimalist](../archetypes/minimalist.md#corpus) | Taxi.js | DOM |
| **Mat Voyce** — matvoyce.tv | [bold maximal](../archetypes/bold-maximal.md#corpus) | Next.js, custom wipe | DOM + CSS |
| **Ponpon Mania** — ponpon-mania.com | [bold maximal](../archetypes/bold-maximal.md#corpus) | Nuxt, narrative loader | DOM |
| **Eloy Benoffi** — eloyb.design | [brutalist](../archetypes/brutalist.md#corpus) | custom GSAP | DOM |
| **Active Theory** — activetheory.net | studio exemplar, not award-verified | custom WebGL SPA (Hydra) + History API | browser-observed |

Not verified: **Cartier Watches & Wonders** (`cartier-waw-0225.dev.60fps.fr`, a 975-byte shell) and **Resn** (`resn.co.nz`, a 4 KB shell on a legacy Modernizr build). Both are single-experience WebGL sites; neither exposed route machinery to a fetch.

Rules are quoted as shipped, with two renderings: `inset: 0` stands in where a live rule enumerates `left:0; top:0; width:100%; height:100vh|100%` with no explicit right or bottom (Truekind's `.clone-transition`, Terminal's `.app-transition`), and Siena's `onLeave` and Mat Voyce's background-loop keyframe are readable renderings of minified and CSS-module-hashed source whose literal values (`B.pages.transitionOut`, `10s linear infinite`, `wght 1000`) match byte for byte.

Router split: **Taxi.js ×3** (Siena, Lando, Contassot) · **Barba.js ×2** (Locomotive, Dennis) · **Nuxt-native ×4** (Immersive Garden, Truekind, Terminal, Ponpon) · **Next.js ×3** (Robin, Stefan, Mat Voyce) · **custom SPA ×3** (Cuberto, Eloy, Active Theory). **Zero of these 15 ship the native View Transitions API as their route transition.**

## Transition forms

Six forms recur. A seventh, the hard cut, appears only as an anti-signal.

### Form 1 — curtain / cover

A fixed panel slides or fades over the viewport to mask the DOM swap, then retreats to reveal the new page. The default MPA and SPA move.

| Beat | Cuberto | Terminal Industries | Truekind |
|---|---|---|---|
| 0 rest | `.cb-loader` fixed, `height:100lvh`, `z-index:999`, `overflow:hidden`, idle | `.app-transition` fixed `inset:0`, `z-index:999`, `opacity:0; visibility:hidden; overflow:clip` | `.base-overlay-transition` fixed `inset:0`, `#fff`, `opacity:0`, `z-index:98`, `pointer-events:none` |
| 1 cover-in | `.cb-loader-fill` (`background:#fff`) fills the viewport; `.cb-loader-backdrop` `rgba(0,0,0,.3)` dims underneath (JS-driven, observed) | overlay becomes `.active`, `opacity` → 1 over the swap (GSAP, observed); the [minimalist](../archetypes/minimalist.md) CSS read gives the *visible* cover as `.app-loader`'s dark `.overlay` variant instead — see below | `opacity` → 1, white sheet in (JS, observed) |
| 2 swap | DOM replaced behind the fill | route DOM replaced behind the overlay | new page mounts behind the sheet |
| 3 uncover | fill retreats, new page revealed | `opacity` → 0, overlay hidden | `opacity` → 0, sheet out |

Cover panels are the page ground, never a neutral gray: Cuberto `#fff`, Truekind `#fff`. Terminal is the exception: the [minimalist](../archetypes/minimalist.md) CSS read of the same build gives the route-change form as `.app-loader`'s dark variant, `.overlay[data-v-068da249]{background:rgba(0,0,0,0.7)}` = `#000000b3`, a dark cover over the cream site rather than a light one. Z-index is a decisive `998–999` so nothing bleeds through. Cuberto's stylesheet carries two `.cb-loader` height rules (`100vh` then `100lvh`); the effective value is `100lvh`.

### Form 2 — shared-element morph

The thumbnail the user clicked becomes the hero of the next page: it is cloned into a fixed layer and the clone's box animates to fullscreen while the real page swaps underneath. **GSAP Flip is the shipped engine**, and `data-flip-id` is its signature attribute.

| Beat | Truekind (winner-verified DOM + CSS) |
|---|---|
| 0 rest | `.clone-transition` `display:none`, fixed `inset:0`, `height:100vh`, `background:#fff`, `z-index:998`, carrying `data-flip-id="fullscreen"` |
| 1 clone | the source image is cloned into `.is--cloned` (Flip records first and last state), `.clone-transition.active{display:block}`, `cursor:wait` |
| 2 flip | the clone animates to `height:100%!important; width:100%!important; margin:0!important`; a split variant `.is--cloned2{height:50vh!important}` serves two-up layouts |
| 3 settle | destination page mounted, clone removed, and the Form 1 white sheet covers the hand-off seam |

This is the mechanism behind Truekind's product-color page transitions: the product still image itself carries continuity across the route.

### Form 3 — cross-fade

The framework-native default. Award-grade winners make it **asymmetric and overlapping**, never a symmetric dip to nothing.

| Beat | Immersive Garden — Nuxt (live-read CSS) |
|---|---|
| 0 | `.page-default-transition-leave-active{transition:opacity 0s linear}` — the outgoing page disappears instantly |
| 1 | `.page-default-transition-enter-active{transition:opacity .7s cubic-bezier(.445,.05,.55,.95)}` from `opacity:0` — the incoming page fades in over 0.7s |
| overlap | `.fade-global-successive-enter-active{position:absolute; inset:0; transition-delay:.4s}` stacks the incoming page over the outgoing during the dissolve rather than laying it out after |

The named ease `cubic-bezier(.445,.05,.55,.95)` is the published ease-in-out-sine. The craft is the asymmetry: instant out, 0.7s in. A symmetric 0.3s fade-both is the generic default; the winner biases the whole budget into the entrance. The same ease family carries lighter layers: `.fade-global` at `opacity .3s` and `.fade-global-over` at `opacity .6s`, each with a matching `-leave-active` rule. One ease, three durations.

### Form 4 — wipe-with-wordmark

The transition panel is itself a typographic moment showing the destination.

| Beat | Mat Voyce — Next.js (winner-verified CSS) | Dennis Snellenberg — Barba |
|---|---|---|
| 0 rest | `.styles_transition` fixed `z-index:99`, `100vw × 100dvh` (`--h:100dvh`), `background:#bcf3ff`, masked by `mask-image:linear-gradient(0deg, rgba(6,40,53,0) var(--bottom), #062835 var(--bottom), #062835 var(--top), rgba(6,40,53,0) var(--top))` with `--top:0%; --bottom:0%` | `data-barba-namespace` selects the transition per route type |
| 1 wipe-in | `--top` and `--bottom` animate the gradient mask open; `transform:translateZ(0); backface-visibility:hidden` for GPU | a full-viewport colored panel wipes in |
| 2 name | `.styles_transition_heading` giant kinetic pill — `font-size:min(16.6666666667vh,9.375vw)`, F37 variable font (`font-family:var(--font-f37)`) at `font-variation-settings:"wght" 1000,"wdth" 60,"slnt" 500`, per-char `.styles_char`; `.styles_transition_bg` loops a texture at `10s linear infinite` (keyframe `translateX(0)` → `98%`) with `transition:opacity 1s var(--easeInOutQuart)` | the project title renders on the panel |
| 3 wipe-out | mask closes, new page revealed | panel retreats to the new page |

Mat Voyce's panel is a *designed screen*, not a blank cover: color `#bcf3ff`, a scrolling background texture, and the page name set in the same dancing F37 widths as the site's hero. Dennis's router is winner-verified via `data-barba="wrapper"` / `data-barba="container"` / `data-barba-namespace="home"`; the title wipe itself is observed. That the panel names the *destination* is per-route JS text, observed rather than read.

### Form 5 — router-managed custom

Not a distinct visual form so much as the plumbing under Forms 1 and 4: a PJAX router or SPA framework fetches the next route, swaps a subtree, and hands the timeline to GSAP or a Rive state machine. The dominant award pattern.

| Winner | Beat recipe | Evidence |
|---|---|---|
| **Siena** | Taxi.js `onLeave({from, trigger, done}){ B.pages.transitionOut(from).then(() => done()) }` → GSAP `transitionOut` runs, `done()` fires, `onEnter` runs `transitionIn`; content lives in `data-taxi` / `data-taxi-view` / `data-page="home"`. Named eases on chrome and panels: `--easeOutQuint: cubic-bezier(.23, 1, .32, 1)`, `--customEase: cubic-bezier(.19, 1, .22, 1)` | winner-verified JS — `Renderer`, `Transition`, `addRoute`, `onEnter`/`onLeave`/`onEnterCompleted`/`onLeaveCompleted`; eases winner-verified CSS |
| **Lando Norris** | Taxi.js swaps `data-taxi-view`; the transition overlay is a **Rive** animation — `.transition-rive`, `.transition-w`, `.transition-btn` | winner-verified DOM |
| **Gabriel Contassot** | Taxi.js `data-taxi` subtree swap on a monochrome portfolio | winner-verified DOM |
| **Locomotive** | Barba.js PJAX + Locomotive Scroll; `c-preloader` grid intro; the route swap fetches HTML and GSAP runs the transition | live-read JS — `@barba/core`, `pushState`/`popstate`, `x-barba` header, `prefix:"data-barba"`. Barba is configured in JS, so the static homepage HTML carries no `data-barba` attributes |
| **Dennis Snellenberg** | Barba.js v2 + Locomotive Scroll | winner-verified DOM |

### Form 6 — persistent-canvas morph

The immersive form. There is no DOM page to swap: a single `<canvas>` renders every "page," so the route change is a WebGL scene transition while the canvas element persists and `pushState` updates the URL.

| Beat | Active Theory (live-read, browser-observed) |
|---|---|
| 0 rest | one `<canvas>` in `.Container`; nav links are `href="#"` intercepted by JS; the only real `href` is an external privacy link |
| 1 click | "Work" click dispatched; the same canvas node persists (`canvasCount` stays 1, the tagged node is unchanged) |
| 2 morph | the WebGL scene animates ~1s while the URL updates `/` → `/work` via the History API |
| 3 back | `history.back()` returns to `/`, popstate reverses the scene, and the canvas is still the same node — no reload, no broken-back tell |

Measured in-browser: the URL flipped between the 500ms and 1000ms samples, and node identity held across both the forward and back navigations. The ~1s morph duration was not frame-timed. The observed 2400×1260 canvas size is a device-dependent render size, not a build value.

### Form 7 — none / hard cut

No winner in this corpus ships a deliberate hard cut between routes. It is an anti-signal, not a form; see below.

## Tech paths

### A. PJAX routers — Taxi.js and Barba.js, the award default

Small vanilla libraries that intercept link clicks, `fetch()` the target URL's HTML, swap a marked container, and run a JS transition.

**Taxi.js** (`@unseenco/taxi`): mark the persistent parent `data-taxi` and the swapped element `data-taxi-view`. Its own docs state it is "designed as a drop-in replacement (with enhancements) for Highway.js, which is sadly no longer maintained", so do not reach for Highway. URL-based routing, response caching, preload. **Barba.js**: `data-barba="wrapper"` / `"container"` plus `data-barba-namespace` to pick a transition per route type.

Who ships it: Taxi on Siena, Lando Norris, and Gabriel Contassot; Barba on Locomotive and Dennis Snellenberg.

What it costs:

- **Back button.** Works. Both use the History API, so real URLs and back/forward behave.
- **SSR and SEO.** Friendly. They fetch server-rendered HTML per route, so the initial page and every fetched page are real documents. This is why they pair with Webflow and static builds.
- **Scroll restoration.** The documented pain point. `history.scrollRestoration` defaults to `"auto"`, which restores position and fights a JS transition; winners set it `"manual"` and restore by hand. Barba carries open issues on back-button scroll (#423 "Manage previous scroll position with back/forward browser buttons", #133 "Back button scroll transition issues"). A build that forgets this lands the reader at the wrong position on back.
- **The continuity trick.** Only the `data-taxi-view` / `data-barba="container"` subtree swaps. The nav, the Locomotive Scroll shell, a WebGL canvas *outside* the container, and an audio player all survive the transition. That persistence is how an MPA fakes SPA smoothness.

### B. Framework-native transitions

**Nuxt** drives route changes through Vue `<Transition>` with named CSS classes (`*-enter-active` / `*-leave-to`) set by `definePageMeta({ pageTransition })`. Verified on Immersive Garden (`page-default-transition`, `fade-global*`), Terminal Industries (`app-transition` overlay plus `app-loader`, scoped `data-v-*`), Truekind, and Ponpon Mania. **Next.js** winners drive transitions in client components: Mat Voyce's `styles_transition*` module is a hand-built overlay, not a framework primitive.

The cost is hydration and a JS-owned scroll (`scrollBehavior` / `scrollRestoration` config, or a smooth-scroll layer). The router owns forward and back symmetrically, but the initial-load and SSR story belongs to the framework. Nuxt's asymmetric `leave: 0s / enter: .7s` is the craft move that keeps a framework fade from reading generic.

### C. Native View Transitions — absent from the 15-site census

`@view-transition { navigation: auto }` (cross-document) and `document.startViewTransition()` (same-document) are the platform's own route transition. **None of the 15 censused sites ships either**; no other named SOTD or SOTM ships it. The one corpus-wide exception is Cyd Stumpel's verified `startViewTransition` shared-element route ([`../archetypes/spatial-organic.md`](../archetypes/spatial-organic.md)). Active Theory's runtime *supports* `document.startViewTransition` (the feature is present) but hand-rolls the WebGL morph instead.

Why the award tier skips it, grounded on Baseline status:

- Same-document View Transitions reached Baseline Newly available around October 2025 via Firefox 144: progressive enhancement only, feature-detect `startViewTransition`. Cross-document View Transitions are still absent in Firefox as of mid-2026, so not Baseline.
- The default is a **cross-fade** that takes two CSS lines, which is exactly the transition winners out-design with GSAP-timed cover panels, Rive overlays, Flip morphs, and kinetic wipes. It gives less timeline control than GSAP over a Taxi or Barba swap.
- It is the right tool for a content or editorial site that wants tasteful morphs cheaply: a named-element morph via `view-transition-name` on a thumbnail-to-hero pair. That is the progressive-enhancement floor, not the signature.

**Net.** For an award-grade route transition, reach for a PJAX router (Taxi for MPA, Webflow, or static; Barba for per-namespace transitions) or the framework's own `<Transition>` with an asymmetric ease.

## The loader-coherence rule

**Verified: the route transition rhymes with the intro loader, one arrival language per site.** Four sites show the loader and the route transition sharing a component, a color, or an ease:

- **Terminal Industries.** `.app-loader`, its dark `.overlay` variant, and `.app-transition` are all fixed, full-viewport, `z-index: 999` overlays in the same Vue component family, and the [minimalist](../archetypes/minimalist.md) CSS read goes further: the route change reuses `.app-loader` itself, one curtain at two amplitudes. A winner-verified negative on the same site: "highway" appears only in body copy ("seamlessly connecting highway to warehouse"), never as the Highway.js router. (See Refuted for the exact scope.)
- **Cuberto.** One `.cb-loader` white-fill curtain is the site's only full-viewport panel; intro and SPA route cover read as the same `#fff` fill over an `rgba(0,0,0,.3)` backdrop. Reuse is inferred from the single-curtain DOM, so single-source.
- **Truekind.** `.preloader` (white, `z-index: 9999`, with a growing 1px `.preloader__inner .line{background:#fff9; transform:translate(-50%) scaleY(0); transform-origin:top; width:1px}`), `.base-overlay-transition` (white sheet), and `.clone-transition` (white) form one **white arrival family**. Every hand-off is a white moment.
- **Immersive Garden.** The intro loader and the page transitions both live on the `cubic-bezier(.445,.05,.55,.95)` ease family. One timing voice from arrival through navigation.

The rule for a build: whatever the loader's gesture (a fill, a wipe, a color, an ease), the route transition uses the same gesture. A site that arrives on a white curtain and then cross-fades between routes has two arrival languages.

## MPA and SPA notes

**How SPA winners avoid the broken-back-button tell.** The classic failure is a transition that animates forward but blanks or jumps on back.

- **Active Theory**, verified in-browser: `history.back()` from `/work` returned to `/` with the same canvas node and a reversed scene. Popstate is handled, nothing reloads.
- **Framework routers** own forward and back symmetrically; transition classes fire on both enter and leave regardless of direction.
- The discipline: drive the transition off the router's navigation event, which also fires on popstate, never off the click handler alone. A click-only transition is the one that breaks on back.

**Focus and reduced motion.** A blocking cover held beyond a beat traps focus and keyboard users behind it. The panel must go `pointer-events: none` once it stops masking (Terminal `.app-transition.active{pointer-events:none}`, Mat Voyce `.styles_transition{pointer-events:none}`, both winner-verified), and focus must move to the new page's top. Under `prefers-reduced-motion: reduce`, the transition collapses to an instant swap or a ≤150ms opacity, never a 1s wipe.

## Archetype-fit map

| Archetype | Default route form | Verified site(s) | Note |
|---|---|---|---|
| **Minimalist** | quiet cover in the page ground, or an asymmetric cross-fade | Terminal Industries (cover overlay), Gabriel Contassot (Taxi swap) | fast (≤500ms), no wordmark theatrics; the panel is the page color or its inverse — Terminal covers its cream ground with `rgba(0,0,0,0.7)` |
| **Editorial** | cross-fade or a named wipe; shared-element morph for thumbnail-to-hero | Siena (Taxi + GSAP), Truekind (Flip morph) | the morph carries reading continuity; `view-transition-name` is the cheap editorial option |
| **Corporate luxury** | slow asymmetric cross-fade, one ease family | Immersive Garden (Nuxt, 0.7s enter) | restraint — instant leave, slow enter, never a busy wipe |
| **Bold / maximal** | wipe-with-wordmark: the transition is a designed screen | Mat Voyce (kinetic F37 pill wipe), Ponpon Mania (narrative loader) | the panel shows the destination name in the site's display face |
| **Immersive / cinematic** | persistent-canvas morph, or Taxi + Rive over a media hero | Active Theory (WebGL persist), Lando Norris (Taxi + Rive) | the canvas never unmounts; the scene *is* the transition |
| **Experimental** | bespoke — the route change is part of the world metaphor | Eloy Benoffi (custom GSAP), Active Theory | the transition obeys the site's invented physics, with a real URL underneath |
| **Brutalist** | hard swap or instant color cover, deliberately un-eased | none verified at route level | the one archetype where a near-cut is on-brand rather than a tell; archetype-reference claim, not winner-verified |
| **Bento / card** | none or instant; the layout *is* the continuity | Anime.js ships no preloader | shared-element `layoutId` for tile re-order, not a page cover; archetype-reference claim |
| **Spatial organic** | soft cross-fade or shared-element depth morph | — | matches the depth-and-blur register |

## Anti-signals

1. **A hard cut on a site that choreographs everything else.** A page that eases every scroll reveal and hover, then blanks and repaints on navigation, breaks its own contract. Only brutalist earns a near-cut. No verified winner does this.
2. **A 1.5s blocking wipe on every click.** The transition is a tax paid on *every* navigation. Immersive Garden's incoming is 0.7s, Active Theory's morph ~1s, and the leave is often instant. Budget the motion into the entrance and make the exit cheap.
3. **Breaking scroll restoration.** A PJAX router left on `history.scrollRestoration = "auto"`, or an SPA with no `scrollBehavior`, lands the reader at the wrong position on back or forward. This is *the* PJAX tell.
4. **Breaking the back button.** An SPA transition wired to the click handler instead of the router's navigation event animates forward but blanks or jumps on popstate.
5. **Trapping focus behind the cover.** A panel left `pointer-events: auto` and focusable after it stops masking strands keyboard users.
6. **A route transition that does not rhyme with the loader.** Two arrival languages on one site: a wipe on arrival, a cross-fade between routes.
7. **Reaching for native cross-document View Transitions as the signature.** Not Baseline, and its default cross-fade is exactly what the award tier out-designs.
8. **A wordmark wipe that names the wrong thing.** The wipe works because the panel shows the *destination*; a panel showing the site logo on every click says nothing and just delays the reader.

## Refuted

- **Terminal's loader and route transition share the Vue component scope `data-v-2a5cb2b0` with identical full-viewport geometry.** Imprecise: the *rendered* `.app-loader` element is scoped `data-v-068da249`, and its full-viewport geometry (`height:100%; width:100%; left:0; top:0`) resolves through that scope. A co-located `.app-loader[data-v-2a5cb2b0]{position:fixed; z-index:999}` rule does exist, so the sharing is real but narrower than stated. The coherence conclusion (loader and transition are both fixed, `z-index: 999`, full-viewport overlays) stands.
- **Terminal's route cover is a light overlay over its cream site.** False: the [minimalist](../archetypes/minimalist.md) CSS read of the same build gives `.overlay[data-v-068da249]{background:rgba(0,0,0,0.7)}` = `#000000b3` as the route-change form, a dark cover, and attributes it to a reuse of `.app-loader` rather than to `.app-transition` alone. The `.app-transition` rules quoted above stay as read (the element exists and carries an `.active` state), but the cover's ground was wrong and the element painting it is contested.
- **Siena Film Foundation holds SOTM Apr 2025.** False: March 2025 ([editorial](../archetypes/editorial.md#refuted)).

## Could not verify

Cartier Watches & Wonders and Resn route machinery (empty WebGL shells, two fetch attempts each). Robin Noguier's and Stefan Vitasović's route-transition *mechanism*: the framework is verified, the client-side transition code was never decompiled. Cuberto's reuse of `cb-loader` for the route, as opposed to the intro only, is inferred from the single-curtain DOM.
