---
title: "Preloaders on Winners — Archetype-Conditional, and Every Loader Hands Off"
date: "2026-07-30"
author: "Coroboros"
tags: ["preloaders", "page-load", "core-web-vitals", "lcp", "webgl", "gsap", "prefers-reduced-motion", "awwwards", "design-archetypes", "anti-patterns"]
sources:
  - "https://terminal-industries.com"
  - "https://gabrielcontassot.com"
  - "https://stefanvitasovic.dev"
  - "https://eloyb.design"
  - "https://ponpon-mania.com"
  - "https://matvoyce.tv"
  - "https://exat.hottype.co"
  - "https://siena.film"
  - "https://truekindskincare.com"
  - "https://www.anthropic.com"
  - "https://landonorris.com"
  - "https://bruno-simon.com"
  - "https://sondaven.com/en"
  - "https://depoluxe.xyz"
  - "https://animejs.com"
  - "https://vercel.com"
  - "https://flowfest.co.uk"
  - "https://www.delvaux.com"
  - "https://www.awwwards.com/sites/terminal-industries"
  - "https://www.awwwards.com/sites/stefan-vitasovic-portfolio25"
  - "https://www.awwwards.com/sites/mat-voyce"
  - "https://thefwa.com/cases/mat-voyce"
  - "https://www.awwwards.com/sites/exat-typeface"
  - "https://www.cssdesignawards.com/sites/exat-typeface/47246"
  - "https://thefwa.com/cases/exat-typeface-p2"
  - "https://www.awwwards.com/sites/siena-film-foundation"
  - "https://www.awwwards.com/sites/lando-norris"
  - "https://www.awwwards.com/annual-awards/winners"
  - "https://www.awwwards.com/sites/son-daven"
  - "https://www.awwwards.com/sites/delvaux-digital-flagship-store"
  - "https://www.awwwards.com/sites/igloo-inc"
  - "https://www.awwwards.com/sites/cartier-watches-wonders-2025"
  - "https://www.awwwards.com/websites/sites_of_the_month/"
---

# Preloaders on Winners — Archetype-Conditional, and Every Loader Hands Off

Preloaders are archetype-conditional, not default: 6 of the 19 sites read live ship none, and for their archetype that is the correct move. A cross-archetype read of the preloader, from 30 assessed winners. Archetypes and their canonical winners live in [the parent reference](../award-winning-websites-2025-2030.md).

**Corpus.**

| Evidence tier | Sites | Method |
|---|---|---|
| Read live (19): 16 winners plus 3 design controls | Terminal Industries, Gabriel Contassot, Stefan Vitasović, Eloy Benoffi, Ponpon Mania, Mat Voyce, Exat, Truekind, Siena Film Foundation, Anime.js, FlowFest, Delvaux, Lando Norris, Bruno Simon, Son Daven, Depo Luxe; controls Anthropic, Vercel, Arc | CSS and DOM byte-read: `curl` raw HTML plus stylesheets, cross-checked against Awwwards winner pages for award, date, and score; no browser opened |
| SPA/WebGL shells observed, not read (5) | Active Theory, Aristide Benoist, Messenger, Granola, Apple | shell fetch only |
| Case studies or secondary sources (6, plus two `steps(n)` references) | Igloo Inc, Cartier Watches & Wonders 2025, Sui Overflow, Bisous, Dondre Green, Naya; GT America and Black Messiah | not read live |

**Every verified loader carries a handoff.** Of the 19 read live, 16 are award-verified and 3 are design controls (Anthropic, Vercel, Arc). 3 of the 16 winners ship no preloader; the 3 controls also ship none. The remaining **13 ship one and earn it**, and each one hands off into the hero: curtain retract, counter recolor, logo Flip, clip-path reveal, narrative continuation. A loader with no handoff appears in zero winners examined.

Of the two patterns the design literature pushes, one is absent from every winner read at depth, a `prefers-reduced-motion` loader path. The other ships: Son Daven's `initPreloader` branches on `sessionStorage.hasVisited`, running the full intro on a first visit and a short version afterwards, so the repeat-visit branch is award record, not technique ([Son Daven live read](../winners/son-daven.md)).

**Archetype record and stack for the sites quoted below.** Award lines (award, date, score) live in the linked archetype corpus tables.

| Winner | Archetype record | Stack |
|---|---|---|
| Terminal Industries — `terminal-industries.com` | [minimalist](../archetypes/minimalist.md#corpus) | Nuxt |
| Gabriel Contassot — `gabrielcontassot.com` | [minimalist](../archetypes/minimalist.md#corpus) | Astro |
| Stefan Vitasović — `stefanvitasovic.dev` | [minimalist](../archetypes/minimalist.md#corpus) | Next |
| Eloy Benoffi — `eloyb.design` | [brutalist](../archetypes/brutalist.md#corpus), bold-maximal register | Webflow, GSAP (SplitText, ScrambleText, ScrollTrigger, Observer) + Lenis |
| Ponpon Mania — `ponpon-mania.com` | [bold maximal](../archetypes/bold-maximal.md#corpus) | Nuxt |
| Mat Voyce — `matvoyce.tv` | [bold maximal](../archetypes/bold-maximal.md#corpus) | Next |
| Exat — `exat.hottype.co` | [bold maximal](../archetypes/bold-maximal.md#corpus), type specimen | — |
| Siena Film Foundation — `siena.film` | [editorial](../archetypes/editorial.md#corpus), dark cinematic | Webflow |
| Truekind — `truekindskincare.com` | [editorial](../archetypes/editorial.md#corpus), light | Nuxt |
| Anthropic — `anthropic.com` | [editorial](../archetypes/editorial.md#corpus), light; brand control, not a winner | — |
| Lando Norris — `landonorris.com` | [immersive cinematic](../archetypes/immersive-cinematic.md#corpus) | Webflow, by OFF+BRAND |
| Bruno Simon — `bruno-simon.com` | [experimental](../archetypes/experimental.md#corpus) | — |
| Son Daven — `sondaven.com/en` | [corporate luxury](../archetypes/corporate-luxury.md#corpus) | Webflow + GSAP + WebGL |
| Depo Luxe — `depoluxe.xyz` | [corporate luxury](../archetypes/corporate-luxury.md#corpus) | 11ty |
| Delvaux — `delvaux.com` | [corporate luxury](../archetypes/corporate-luxury.md#corpus) | — |
| Anime.js — `animejs.com` | [bento / card](../archetypes/bento-card.md#corpus) | — |
| FlowFest — `flowfest.co.uk` | [brutalist](../archetypes/brutalist.md#corpus) | Barba.js + GSAP |
| Igloo Inc | [spatial organic](../archetypes/spatial-organic.md#corpus), experimental | case study, not read live |
| Cartier Watches & Wonders 2025 | [corporate luxury](../archetypes/corporate-luxury.md#corpus) | case study, not read live |

## Loader families

Six families. Durations are the loader's own timeline, not LCP. The handoff is the exit move and the craft lever.

### 1. Numeric counter (`1→100` / `0→100`)

| Beat | What shows | Value | Source |
|---|---|---|---|
| Count | Rolling odometer digits, mono | Terminal `.odometer{--font-size:.8125rem; font-family:var(--font-mono); font-weight:600; letter-spacing:.14625rem}`, `.digit-column{overflow:hidden}`, `.digit,.digit-stack{will-change:transform}` | Terminal, winner-verified (`PaddedCounter.D_9jWspQ.css`) |
| Recolor | Numerals shift through the accent as they climb | `@keyframes color-transition{0%{color:var(--c-light-light-gray)} 30%{color:var(--c-lime)} to{color:var(--c-dark-green)}}` — the live keyframe name carries a scope suffix (`color-transition-dfc3204d`) | Terminal, winner-verified, byte-exact |
| Complete → handoff | Curtain retracts over a pre-composed hero | see split-curtain | Terminal, winner-verified |

Variants:

- **Bare accelerating `1→100`.** No curtain; the counter *is* the intro. Gabriel Contassot (technique; the live route-curtain is winner-verified, the counter is not visible in the live DOM). The minimalist floor form.
- **Asset-gated diegetic ratio.** Bruno Simon: `.global-progress .ratio{color:#ffceca; font-weight:700}` climbs, then `.global-progress.is-achieved .ratio{color:#d5ff95}` recolors to lime **and** prints elapsed time via `.is-achieved .time{display:inline; font-weight:700}` with `.time:before{content:"in "; opacity:.65}`. The counter reports the real load, not a timer. Off-screen font preload sits at `.fonts-loader{position:fixed; top:calc(100% + 1px)}`. (winner-verified)
- **Roman numerals are index micro-type, not a loader counter.** Depo Luxe `.counter-roman{text-align:right; width:50%}`, `span{display:inline-block}`, `.progress .line .counter-roman{opacity:.4}` are read from `main.b0b97476….css`, but they number the works index rather than load progress: the [Depo Luxe live read](../winners/depo-luxe.md) finds `#Preloader` to be an SVG logo build plus a `video-preloader` with no numeric percent element, and the roman numbering runs off `counter(roman-counter, upper-roman)` on the works rows. The luxury register holds; the loader is not where it lives.
- **`steps(n)` concept numerals.** Naya (countdown preloader plus custom cursor), GT America / Black Messiah. Numerals carry the brand, asset-gated. (technique / single-source, not read live)

### 2. Split-curtain

| Beat | What shows | Value | Source |
|---|---|---|---|
| Cover | Full-screen fixed panels over the fold | Terminal `.app-loader{position:fixed; inset:0; z-index:999; pointer-events:none}`, `.loader{display:flex; flex-direction:column; justify-content:space-between; overflow:hidden}` | Terminal, winner-verified (`entry.Bdya6FOo.css`) |
| Split | Two `50svh` panels, top and bottom | `.top` / `.bottom` in loader scope, both `height:50svh` | Terminal, winner-verified |
| Retract | Panels pull apart to uncover an already-painted hero | JS/GSAP-driven; `.app-loader` carries no CSS transition or animation | Terminal, mechanism winner-verified |

- **Single-panel wipe.** Gabriel Contassot's route curtain: `fixed w-screen h-screen bg-grey pointer-events-none z-50 origin-bottom scale-y-0`, scaling vertically from the bottom, plus a black intro overlay `fixed bg-black overflow-clip z-[100]`. Reused for both intro and route change. (winner-verified DOM)

### 3. Wordmark / logo assembly

| Beat | What shows | Value | Source |
|---|---|---|---|
| Build | Logo draws in as progress advances | Depo Luxe `.preloader__logo figure>svg path{opacity:0}` → paths fill; `svg{fill:var(--color)}`; figure absolute-centered | Depo Luxe, winner-verified (`main.b0b97476….css`) |
| Drive | Progress line scales behind the mark | `.progress .line:after{background-color:currentColor; transform:scaleY(var(--progress)); transform-origin:0 0}` — `--progress` is data-driven | Depo Luxe, rule winner-verified; its placement **inside** the loader is contested — the [Depo Luxe live read](../winners/depo-luxe.md) finds only the logo build and the video inside `#Preloader` |
| Handoff | Assembled mark Flips into the persistent header or footer logo | Son Daven `.preloader_logo{position:absolute; bottom:0; left/right:var(--_units---u-16)}` → `header_logo`; Depo shares one `__logo` class across preloader, header, and footer | Son Daven, Depo Luxe — position winner-verified, Flip observed |

- **Brand-object assembly (3D / Rive).** Lando Norris builds the helmet in `<canvas class="gl">` plus Rive canvases (`data-rive-ln4`, `data-rive-primary`, `data-rive-mob-landscape`), then reveals via a top-anchored clip-path.
- **Letter-grid → wordmark.** Dondre Green: a grid of letters resolves into the hero wordmark. (technique, case study)

### 4. Progress-as-brand-element

| Form | Mechanism | Value | Source |
|---|---|---|---|
| Hero top-bar → nav | Thin bar pinned to the hero top, primary fill | Eloy `.hero-loader{position:absolute; inset:-1px -1px auto; height:calc(1rem + 1px); z-index:99999; pointer-events:none; display:none}`, `.hero-loader_bar{background-color:var(--color--primary); position:absolute; inset:0%; border-radius:0 var(--borders--border-radius) var(--borders--border-radius)}` | Eloy — bar winner-verified; "becomes navbar" single-source, morph not confirmed in CSS |
| WebGL scene meter | Progress gates on real 3D scene readiness | Son Daven `.preloader_bg_scene{mix-blend-mode:lighten}` renders while assets stream; descriptor columns `.preloader_desc-l`, `.preloader_desc-r`, `.preloader_top_desc` | Son Daven — structure winner-verified, `Promise.all` gate observed |
| Circular SVG + bar | SVG stroke ring plus a `scaleX` bar | Ponpon `.preloader__svg-progress{stroke:#ffcc8e}`, `.preloader__bar-progress{background:#dbdbdb; transform:scaleX(0); transform-origin:left}` | Ponpon, winner-verified |
| Diegetic ratio | Real elapsed load, printed | see Bruno above | winner-verified |

### 5. Phrase cycle / narrative scene-one

The loader is the story's first frame, not a gate in front of it.

| Winner | What plays | Value |
|---|---|---|
| Ponpon Mania | The sheep mascot is scene one, entering scaled and rotated | `.preloader{background:#fff6f0; cursor:wait; position:fixed; inset:0; z-index:14; display:flex; align-items:center; justify-content:center; pointer-events:none}`, `.preloader__ponpon-container{transform:scale(0) rotate(-120deg); width:20vh}`, `.preloader__logo{animation:logo 1s ease-in-out infinite alternate; fill:#0000000a}` |
| Siena Film Foundation | Full-bleed video plus a slide-up enter button | `.preloader-w{position:fixed; inset:0; z-index:99999999; background-color:var(--black); display:none}` with `.show{display:flex}`; `.preloader-video{height:50svh}` desktop, `.preloader-video.mobile` `100svh`; `.preloader-btn{transform:translateY(200%); font-family:Neue Brucke}`, `.preloader-btn-w{visibility:hidden; overflow:clip}` |
| Truekind | Progress-tracked full-screen loader | `.preloader{color:#fff; height:100dvh; position:fixed; inset:0; z-index:9999}`, `.preloader__inner`; DOM carries `<div class="preloader">` plus `reveal-waitpreloader` (×2); the bundle carries `$sstatePreloadProgress`, `$sstatePreloadDone`, `$sstatePreloaderItems` |
| Depo Luxe | `video-preloader` medium under the logo build | class present, winner-verified; palette `#fff`/`#000` shipped-tier, unverified |
| Mat Voyce | Full-screen intro overlay plus a route `simplePageLoader` | `.styles_intro__bHn10{position:absolute; inset:0; width:100%; height:100%; z-index:3}` |
| Exat | `preloader` plus `intro-frame` / `intro-part` / `enter-part` | classes present in DOM; rules live in an inline `<style>` and were not extracted |
| FlowFest | An in-character chat conversation types itself, then hands off to the hero | `.loading-screen` → `{autoAlpha:0, duration:0.3, ease:"none", delay:0.1}`; the cloud types `"..."` → `"Hi Friends!"` → `"We are back..."` → the hero's resident text (GSAP TextPlugin, all `ease none`), `lenis.stop()` for the duration; the handoff drops the nav from `yPercent -102` and staggers the H1 spans in ([brutalist](../archetypes/brutalist.md), from `initLoader`) |
| Bisous | Cinematic loader becomes the homepage slider | technique, case study |

All winner-verified except Bisous (technique) and the Depo palette (shipped, unverified).

### 6. None / instant

No preloader element in the DOM; the entrance is carried by first paint plus reveals. Verified absence unless noted; the three design controls are marked.

| Site | Archetype | What carries the entrance |
|---|---|---|
| Anthropic (design control) | editorial (light) | zero loader classes, zero preload-state tokens |
| Stefan Vitasović | minimalist | `Reveal_mask` / `Reveal_item` / `HomeHero_reveal` per-char scroll masks |
| Anime.js | bento | `home-progress-card` is a demo tile, not a page loader |
| Vercel (design control) | bento / minimalist | zero loader classes |
| Arc (design control) | spatial-organic | zero loader classes; `animation-timeline: view()` reveals (secondary source) |
| Delvaux | corporate-luxury | `.loader` classes are `cart-modal__*` async spinners plus a `value-input__loading > .loader` micro-spinner — no page preloader |
| Granola / Apple | spatial / bento | instant paint (observed, shells not read live) |
| Sui Overflow | brutalist | near-instant, no ceremony — secondary source here and **contested**: the archetype read of the same line records no zero-intro winner in it ([brutalist](../archetypes/brutalist.md)) |

**Case-study and technique references, not read live.**

| Site | Intro, as reported | Evidence |
|---|---|---|
| Active Theory | a WebGL intro dissolving into navigation, progress-as-narrative | observed |
| Messenger | a Three.js miniature-planet intro | observed |
| Aristide Benoist | a solo WebGL intro | observed |
| Igloo Inc | a real-time in-engine shader intro folding into the experience | single-source |
| Cartier Watches & Wonders 2025 | a WebGL pavilion with a real-progress counter and a logo Flip gated on `Promise.all` | technique |
| Bisous | a cinematic loader becoming the homepage slider | technique, case study |
| Dondre Green | a letter grid resolving into the hero wordmark | technique, case study |
| Naya | a countdown preloader with a custom cursor | single-source, Awwwards inspiration media |
| GT America, Black Messiah | asset-gated `0→100` with `steps(n)` concept numerals | technique |

## The handoff patterns

1. **Curtain retract over a pre-composed fold.** The hero is painted *behind* the curtain, so retracting reveals a finished frame rather than a masked slow-load. Terminal (`50svh` panels), Gabriel (`scale-y-0` wipe).
2. **Counter recolors into the accent.** The numerals resolve on the palette's hero color, pre-stating it. Terminal gray → lime → dark-green (the 30% keyframe is lime); Bruno pink `#ffceca` → lime `#d5ff95` on `.is-achieved`.
3. **Loader element morphs into persistent UI.** Son Daven's bottom-pinned `preloader_logo` becomes `header_logo` by Flip; Depo Luxe shares one `__logo` class across preloader, header, and footer; Eloy's hero top-bar becomes the nav (single-source). The element the visitor watched load never disappears; it becomes furniture.
4. **Clip-path reveal wipe over the live hero.** Lando `clip-path: ellipse(100% 120% at 50% 0%)`, top-anchored and verbatim in the served DOM, opens the WebGL/Rive hero from the top edge with no hard cut. The DOM also carries `ellipse(100% 50% at 50% 50%)` and `ellipse(80% 50% at 50% 50%)`.
5. **Logo assembly into the hero.** Depo's `svg path{opacity:0}` fills the mark, then the mark seats into the hero.
6. **Narrative continuation.** The loader's subject persists into section one: Ponpon's mascot into the homepage, Siena's video into the first section, FlowFest's chat cloud typing back to the hero's own resident text, Bisous's loader into the slider.

**Anti-signal by construction:** a full-screen counter or splash that fades to `opacity: 0` with no morph, recolor, or reveal geometry: a curtain dropped in front of an unrelated page. Found in zero winners examined.

## Repeat-visit, reduced motion, LCP

### Repeat-visit branch — one winner ships it

Son Daven does: `initPreloader` runs `animatePreloaederIntro` when `sessionStorage.hasVisited` is unset and a short version for returning visitors ([Son Daven live read](../winners/son-daven.md)). It shortens rather than skips, and one winner shipping the gate is enough to make the pattern award record.

Ponpon's 2.3 MB bundle uses `localStorage` for `cookies-status`, `lang`, `last-chapter`, and per-chapter page state, and `sessionStorage` only for Nuxt-internal `nuxt:reload*`; its "Visited" tokens are `chapterVisited` and `sceneVisited`, and the `Preloader` component gates on no storage at all, a bundle-depth negative. No `hasVisited`, `skipPreloader`, `introSeen`, or `preloader-done` token appears in the served HTML of Truekind, Depo Luxe, Son Daven, Siena, or Eloy; Son Daven's flag lives in the shipped JS instead. For the other four the negative is HTML-scope, not proof the loader replays.

The shape for a build adopting it (reasonable for repeat-visit polish) is a flag plus a shortened replay, Son Daven's move, or a full skip beyond it. Son Daven is the record for the gate.

### Reduced motion — a real gap in the record

**No winner read ships a loader-specific `prefers-reduced-motion` path.** Across nine stylesheets the count is: Terminal 1, targeting scroll reveals only (`.reveal-y-enter-active/leave-active{transition:opacity .15s ease}`); Ponpon, Bruno, Depo Luxe, Eloy, Siena, Son Daven, and Truekind all zero.

This is an award-record gap builds should not copy. Under `prefers-reduced-motion: reduce`, cut the ceremony: paint the hero immediately and drop the curtain, counter, or assembly to a sub-200ms opacity fade or nothing.

### LCP — honest gating versus fixed-duration theater

The performance trace separates the two. LCP firing late with an idle network is theater; LCP gated behind real asset requests is honest.

- **Honest asset-gating**, where a heavy hero justifies the wait: Bruno prints the true elapsed time; Depo's asset loader tracks `itemsLoaded`/`itemsTotal` and reads out through the logo path fill, with the `--progress` bar rule measured but not confirmed inside `#Preloader`; Son Daven gates on real asset progress, `Promise.all([framesPromise, globalSceneManager.ready(), document.fonts.ready])` covering WebGL scenes, scroll-video frames, and fonts ([Son Daven live read](../winners/son-daven.md)); Lando waits on `canvas.gl` plus Rive; Active Theory on the WebGL boot. These heroes stream by necessity, so the loader overlaps the streaming rather than inventing latency.
- **The pre-composed-fold trick**, for a light hero with no LCP penalty: Terminal paints the hero *under* the curtain, so the LCP element renders behind `.app-loader` while the odometer counts. Retract just uncovers it, and the counter costs zero LCP.
- **The lie the trace catches:** a fixed-duration counter or splash over a DOM-only hero with no WebGL and no video, delaying LCP for theater. This is the bold-maximal, minimalist, and bento anti-pattern; those archetypes ship instant paint or the pre-composed-fold curtain instead.

## Archetype-fit map

| Archetype | Fitting loader family | Named record |
|---|---|---|
| **Minimalist** | Bare `1→100` counter, split-curtain over a pre-composed fold, or instant plus reveals | Terminal (curtain + odometer), Gabriel (counter), Stefan (none) |
| **Brutalist** | A deliberate in-character intro, with Barba route transitions carrying the motion after it; the line's wider intro record — stepped counter, loader-to-navbar expansion — sits in [brutalist](../archetypes/brutalist.md) | FlowFest (chat-cloud loader; Barba.js `@barba/core@2.10.3`, `data-barba="wrapper"`, plus GSAP for the routes); Sui Overflow's near-instant entry is contested, see above |
| **Editorial** | Register split — dark cinematic ships a video or narrative loader; light editorial splits both ways | Siena (video), Bisous and Dondre (narrative), Truekind (progress-tracked loader), Anthropic (none) |
| **Bold / maximal** | Narrative scene-one, progress-as-brand (bar → nav), asset-gated `steps(n)` counter, or intro overlay. Never a decorative counter over a static hero | Ponpon (narrative), Eloy (bar → nav), Naya and GT America (counter), Mat Voyce and Exat (overlay) |
| **Immersive / cinematic** | Asset-gated WebGL intro; clip-path reveal into the live hero | Lando (helmet + ellipse), Active Theory, Messenger |
| **Experimental** | In-engine intro — the concept booting; the start button doubles as an audio unlock | Igloo (shader), Bruno (`global-progress` + audio gate) |
| **Corporate-luxury** | Content-gated real-progress counter plus logo Flip or SVG-path fill, or instant editorial | Son Daven (Flip, palette `#A89474` / `#2C2824`), Depo Luxe (SVG fill, no counter), Cartier (Flip, case study); Delvaux (none) |
| **Bento / card** | None — the card stagger *is* the entrance (`opacity 0→1` plus a short `translateY`, 40–80ms per tile). A blocking counter is an anti-signal | Anime.js alone carries the winner record: Vercel is a design control and Apple was observed, not read |
| **Spatial-organic** | Fold the intro into the WebGL scene, or instant plus `animation-timeline: view()` reveals | Igloo (in-engine), Arc and Granola (none) |

## Anti-signals

Absent from every winner examined. A build that ships one drops below the award bar.

1. **Spinner.** A rotating throbber. Zero winners. The single clearest tell of a non-designed loader.
2. **Blocking brand-color splash with no handoff.** A full-screen logo card that fades to reveal an unrelated page.
3. **Ceremony beyond ~3s.** Anything longer than a couple of seconds must be genuinely asset-gated and should report real progress, as Bruno does. No ceiling was measured (see Refuted).
4. **Decorative counter over a static hero.** A `0→100` gate in front of a light DOM hero that needed no loading. Delays LCP for theater.
5. **Loader with no handoff choreography.** The disqualifier. No curtain retract, no recolor, no Flip, no clip-path reveal, no narrative carry, regardless of how the loader itself looks.
6. **Roman, `steps(n)`, or decorative numerals untethered from the concept.** Numerals must carry the brand (odometer palette, roman for luxury, `steps(n)` for a type specimen), not decorate.
7. **Fixed-duration theater masking a slow LCP.** The trace catches it: late LCP plus an idle network. Gate on `Promise.all([assets, scenes, fonts.ready])` or paint under the curtain.
8. **No `prefers-reduced-motion` loader path.** Build-side, not winner-copied: every winner read omits one, and a build should add it.

## Refuted

- **Truekind ships no preloader (winner-verified absence).** False: Truekind ships a progress-tracked full-screen preloader, confirmed in CSS, DOM, and bundle state; in the archetype map only Anthropic is the light-editorial "none."
- **Fixed-duration loaders stay ≤2.8s (winner-verified synthesis).** Unsupported: no loader CSS carries a duration and every retract is JS/GSAP-driven, so no ceiling was measured.
- **FlowFest ships no preloader (winner-verified absence).** False: its own `initLoader` runs a full chat-cloud typing loader before the hero handoff, and internal Barba navigations run a shortened `initLoaderShort` echo of it ([brutalist](../archetypes/brutalist.md)); the live-read census is **6 none / 13 loader**, and the brutalist default is a deliberate in-character intro.
- **No winner read at depth skips its preloader on revisit.** False: Son Daven's `initPreloader` branches on `sessionStorage.hasVisited`, full intro on the first visit, short version after ([Son Daven live read](../winners/son-daven.md)).
- **Depo Luxe's roman numerals are the loader's counter.** False: `#Preloader` holds the SVG logo build plus a `video-preloader` and no numeric percent element, and `counter(roman-counter, upper-roman)` indexes the works list instead ([Depo Luxe live read](../winners/depo-luxe.md), [corporate-luxury](../archetypes/corporate-luxury.md)). The `.counter-roman` and `.progress .line` rules are read from the site's CSS; neither sits inside the loader.
- **Cartier Watches & Wonders 2025 is Site of the Day only, so SOTM Aug 2025 is false.** False: the monthly listing carries Aug 2025 ([corporate-luxury corpus](../archetypes/corporate-luxury.md#corpus)).
- **Siena Film Foundation holds SOTM Apr 2025.** False: March 2025 ([editorial](../archetypes/editorial.md#refuted)).

## Could not verify

- Exat's `preloader`, `intro-frame`, `intro-part`, and `enter-part` rules live in an inline `<style>` that was not extracted.
- Eloy's hero top-bar "becomes the navbar": the bar is winner-verified, the morph is single-source and unconfirmed in CSS.
- Depo Luxe: whether the `--progress` line rule sits inside `#Preloader` (the Depo Luxe live read finds only the logo build and the video), and the `#fff`/`#000` loader palette, shipped-tier only.
- Truekind's loader handoff: not examined; its `reveal-waitpreloader` gating implies one.
- Sui Overflow's near-instant entry: secondary source, contested by the brutalist read.
- Loader durations: no browser was opened and every retract is JS-driven, so no duration was measured.
- The five shells (Active Theory, Aristide Benoist, Messenger, Granola, Apple) and the case-study sites (Igloo Inc, Cartier Watches & Wonders 2025, Sui Overflow, Bisous, Dondre Green, Naya, GT America, Black Messiah): intros observed or reported, not read.
- Repeat-visit flags on Truekind, Depo Luxe, Siena, and Eloy: the negative is HTML-scope only; the shipped JS was not read.
