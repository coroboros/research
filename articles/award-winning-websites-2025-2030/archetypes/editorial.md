---
title: "Editorial — Effect Palette, Page Recipe, Aliveness, Type-as-Image"
date: "2026-07-30"
author: "Coroboros"
tags: ["web-design", "awwwards", "editorial", "type-as-image", "motion-design"]
sources:
  - "https://www.awwwards.com/sites/siena-film-foundation"
  - "https://www.awwwards.com/siena-film-foundation-case-study.html"
  - "https://www.awwwards.com/sites/truekind-skincare"
  - "https://www.awwwards.com/sites/bisous"
  - "https://www.awwwards.com/sites/typography-principles"
  - "https://www.awwwards.com/behind-the-scenes-designing-and-building-365-a-year-of-cartier.html"
  - "https://www.awwwards.com/websites/Editorial%20New/"
  - "https://www.awwwards.com/websites/magazine-newspaper-blog/"
  - "https://siena.film"
  - "https://siena-film-foundation.vercel.app/styles/main.css"
  - "https://siena-film-foundation.vercel.app/app.js"
  - "https://www.truekindskincare.com/"
  - "https://truekindskincare.com/_nuxt/entry.Dzz2DK-7.css"
  - "https://www.anthropic.com/"
  - "https://tympanus.net/codrops/2026/06/29/inside-bisous-designing-an-editorial-experience-for-cinematic-cgi/"
  - "https://tympanus.net/codrops/2026/04/10/the-exat-microsite-pushing-a-typography-showcase-to-new-creative-extremes/"
  - "https://tympanus.net/codrops/2025/06/25/designing-truekind-a-skincare-brands-journey-through-moodboards-motion-and-meaning/"
  - "https://tympanus.net/codrops/2025/03/05/case-study-stefan-vitasovic-portfolio-2025/"
  - "https://tympanus.net/codrops/2025/01/07/case-study-dondre-green/"
  - "https://github.com/undercasetype/Fraunces"
  - "https://pixelambacht.nl/2021/optical-size-hidden-superpower/"
  - "https://developer.mozilla.org/en-US/docs/Web/CSS/font-optical-sizing"
  - "https://web.dev/articles/variable-fonts"
  - "https://eyeondesign.aiga.org/making-rules-breaking-rules-the-art-of-magazine-typography/"
  - "https://www.todaymade.com/blog/bad-typography-examples"
---

# Editorial — Effect Palette, Page Recipe, Aliveness, Type-as-Image

The editorial line's verified Awwwards peak is Siena Film Foundation at 7.9, and reading-first work caps there because the jury's Creativity and Animation axes reward spectacle the archetype refuses. Build-level evidence for the Editorial archetype: the effect recipes read off live winners' stylesheets, the page anatomy behind three named shapes, what keeps the middle of a reading page alive at that ceiling, and how the display type becomes the image rather than a well-picked serif. Parent reference: `../award-winning-websites-2025-2030.md`.

## Effect palette

### Corpus

| Site | Award / source | Register | Read |
|---|---|---|---|
| **Siena Film Foundation** · `siena.film` | Awwwards Site of the Day (SOTD) 18 Mar 2025, Site of the Month (SOTM) March 2025 — **7.9** (Design 7.99 / Usability 7.61 / Creativity 8.13 / Content 8.00), Developer Award 7.51 (Animations 8.60) | dark cinematic poster | live DOM + raw HTML + `main.css` + `out.css` + `app.js` |
| **Truekind Skincare** · `truekindskincare.com` | Awwwards Site of the Day 29 Apr 2025 — **7.47** (Design 7.71 / Usability 7.35 / Creativity 7.27 / Content 7.29), Developer Award 7.85 (Animations 8.80 — *contested attribution*) | warm magazine | live DOM + SSR HTML + CSS chunks + driven-scroll test + full `:hover` enumeration |
| **Anthropic** · `anthropic.com` | brand site, named light-editorial peer — a recognised build, not a jury award in this window; used as the light-register control | light editorial | live HTML + `ant-brand.shared.30cd2d119.min.css` |
| **Bisous (Bisous Production)** | Awwwards Honorable Mention; Codrops "Inside Bisous: Designing an Editorial Experience for Cinematic CGI", Jun 2026 | editorial / cinematic CGI | studio description only |
| **Exat microsite** | Codrops typography case study, Apr 2026 | kinetic type microsite | studio description + stated params |
| **365 — A Year of Cartier** | Awwwards "Behind the Scenes" feature — digital yearbook of the print annual | editorial magazine | studio description only |
| **Dondre Green** (Blackpepper Studio) | Codrops case study, Jan 2025 | serif/sans editorial portfolio | studio description only |
| **Stefan Vitasović — Portfolio 2025** | Codrops case study, Mar 2025; author is an Awwwards jury member | editorial portfolio | studio description with stated numbers |
| **Obys — Typography Principles** | Awwwards Site of the Day, Webby nominee | kinetic type microsite | studio description only |

Registers: dark cinematic poster (Siena, Bisous, Dondre lean here), warm magazine (Truekind, Cartier), light editorial (Anthropic). Page shape rhymes across registers; the substrate colour is the expression choice. Patterns holding across registers are the durable ones; register-specific ones are labelled.

Studio prose covers loaders, sliders and scroll choreography; hover states and nav-surface behaviour are almost never documented, so the button, link and nav mechanics below are lifted from `siena-work-space.webflow.min.css`, `ant-brand.shared.min.css` and `truekindskincare/_nuxt/entry.css`.

### The score reality

The line's verified Awwwards peak is **Siena Film Foundation at 7.9** — Design 7.99, Usability 7.61, Creativity 8.13, Content 8.00; Developer Award 7.51, Animations 8.60. The second canonical winner, **Truekind Skincare, scored 7.47** — Design 7.71, Usability 7.35, Creativity 7.27, Content 7.29; Developer Award 7.85, Animations 8.80 (*contested attribution*: the identical 8.80 animations figure is carried for Terminal Industries in [`../winners/site-of-the-year-contenders.md`](../winners/site-of-the-year-contenders.md) and for Stefan Vitasović in [`minimalist.md`](./minimalist.md), so at most one of the three readings is the site's own — see [`../foundations/interaction-architecture.md`](../foundations/interaction-architecture.md)). Two good-faith searches of the editorial and magazine categories surfaced no reading-first site at or above 8.0 in the 2023–2026 window; the corpus's highest whole-site score is Lusion's 8.25 ([`experimental.md`](./experimental.md)). Scores **verified** from the Awwwards site pages; the ceiling is **observed**, **single-source on the negative**.

The 8.5+ tier is dominated by WebGL, immersive and experimental work; **reading-first editorial caps around 7.9 because the jury's Creativity and Animation axes reward spectacle the archetype refuses.** The archetype's own ceiling ships very little mid-prose animation, and that restraint is not what caps it — over-writing and thin identity are.

### Hover and micro-interaction

**AI-default cliché.** One pale, low-opacity tint fill applied to *every* button on hover (`background: rgba(accent, 0.08)`), a `text-decoration: underline` snap on every link, a frosted `backdrop-filter: blur()` bar with a contrasting `border-bottom` under the nav. One trick, repeated on every element class.

**What the winners do instead.** They fill with the **full token** and invert the label — never a washed-out tint — and give each element class a *different* mechanism tied together by a shared easing and palette. Across Siena, Truekind and Anthropic, no button hover uses a pale or low-alpha tint: the fill is always a solid brand value with the text inverting.

#### Buttons and CTAs

- **Full-fill + text inversion (primary/secondary CTA).** Outline or light button fills a solid brand value, text flips to the opposite ink. Truekind `.btn.outline:hover { background:#3b3b3b; color:#fff }` (**verified**, live computed `background:rgb(59,59,59); color:rgb(255,255,255)`). Siena `.all-work-cta-w:hover { background:#000; color:#fff }` with the nested arrow inverting the opposite way (`background:#fff; color:#000`), `transition: .5s` on `--easeOutQuint` = `cubic-bezier(.23,1,.32,1)` (**verified**). Anthropic `.video_player_play_btn:hover { background: theme-text; color: theme-background }`, `.2s` (**verified**). The pick for the main CTA — 3 sites.
- **Two-layer text roll on a filling shape (signature CTA).** Siena's primary `[data-btn=explore]`: an SVG background shape fills transparent→`#fff` (`fill var(--duration) var(--ease)`), the outline stroke goes →`#000`, and the *label rolls* — the visible copy `[data-x]` slides `translate(100%)` out while a duplicate `[data-after]` positioned 150% below rolls `translateY(-150%)` into place, both recolouring to `#000`, staggered `.1s`. `--duration: .8s`, `--ease: var(--easeOutQuint)` (**verified**). The loud hero-CTA move: fill *and* kinetic label, not a colour swap. **single-source** for the exact two-layer roll; the kinetic-label-on-hover idea is corroborated by Truekind's marquee.
- **Kinetic marquee label on hover.** Truekind `.btn`: the static label `.marquee-parent` fades to `opacity:0` while `.marquee__inner` starts its animation (`animation-play-state: running; opacity:1; transition-duration:.4s`) — the button's word begins scrolling as a marquee on hover (**verified**, `@keyframes marquee` on `translate3d`). **Where it fits.** Buttons whose label itself carries the life.
- **Accent-token fill (nav CTA / pill).** Anthropic `.btn_main_wrap.is-nav:hover { background: var(--swatch--clay) }` — the nav CTA fills the full terracotta/clay accent, not a tint, text swapping via `-hover` tokens, `transition: border-color .2s, color .2s, background-color .2s` (**verified**). Truekind's `.navbar-cta` is a charcoal `#333` pill, `transition: background 1s cubic-bezier(.18,.71,.11,1)` (**verified**). The persistent-header pick — 2 sites.
- **Neutral one-step (secondary/utility button only).** The only near-tint the winners allow is a single neutral step reserved for secondary and code buttons, never the primary: Anthropic `.terminal_cta:hover { background: var(--swatch--cloud-light) }` / `.cc-result:hover { cloud-dark }` (**verified**). Never the universal default. **single-source.**

#### Text links

- **Underline draw from the left (`scaleX`).** Truekind `.link:hover:before { transform: scaleX(1); transform-origin:0 50% }`, retracting to the right when already active (`.link.active:hover:before { transform: scaleX(0); transform-origin:100% 100% }`), base rule `.link:before { background:#3b3b3b; height:1px; left:0; top:100%; width:100% }` (**verified**; the sheet uses single-colon `:before`). A drawn line, not a snap — the inline/editorial pick.
- **Underline via decoration-color fade.** Anthropic sets links to `text-decoration: underline` with `text-decoration-color: transparent` at rest and transitions `text-decoration-color .2s` to the ink on hover, with a `text-underline-offset` that *varies by context* — `.2em` nav, `.18em` dropdown, `.25em` footer (single read; see Could not verify). The underline appears in place rather than drawing. Same intent as Truekind, different mechanism → 2 independent sites for "underline materialises on hover", and the varied offset is itself a coherence tell.
- **Card-triggered title underline.** Truekind `.blog__feed-item:hover .blog__title { text-decoration: underline }` — hovering the card underlines its title; the whole card is the target, the title is the feedback (**verified**). **single-source** as a mechanism, but the dominant text-hover across the line (see Mid-page aliveness).

#### Images and cards

- **Contained zoom.** Siena `.previousnext-item:hover .full-img-w { transform: scale(1.1) }` (**verified**). The image scales inside a fixed frame; the parent needs `overflow:hidden`. Baseline, present everywhere.
- **Crossfade swap on two stacked stills.** Truekind `.product__card:hover .product__card-img { opacity:0 }` + `.product__card-img2 { opacity:1 }`, base image sitting at rest `transform: scale(1.2)` inside `overflow:hidden` (computed `matrix(1.2,0,0,1.2,0,0)`) (**verified**).
- **Settle-zoom (inverse of the zoom-in).** Truekind `.journal__card:hover img { transform: scale(1) }` — the image sits above 1 at rest and *relaxes* to 1 on hover (**verified**).
- **Focus / defocus siblings.** The distinctive editorial image-hover: the hovered item sharpens while its neighbours blur and dim, so attention is *directed*. Dondre Green stories page — "hovering elements sharpen while surrounding items gently blur and fade" (**stated**; the behaviour is in the case study, the WebGL-displacement mechanism is not named in it). Corroborated in spirit by Siena's link-group dim. **Where it fits.** Galleries and indexes where one item wins the eye.

#### Nav items

- **Dim-the-siblings, not underline-the-target.** Siena `[data-hover=mainlinkgroup]`: when any link in the group is hovered, *all* links drop to `opacity: 70%` and the hovered one holds `100%`, `transition: opacity .2s` (**verified**; live `[data-hover]` values are `["bggrow","mainlinkgroup","mainlink"]`). The menu reacts as a set. Pairs with Dondre's sibling-blur → 2 sites for "hovering one item quiets the rest."
- **Indicator swap.** Siena `.menu-film-item:hover`: a leading `.dot` scales to `0` while a direct-link arrow fades and scales in (`opacity:1; transform:scale(1)`), `.2s ease-out` (**verified**). Menu rows trade a passive marker for an actionable affordance. **single-source.**

#### The nav bar itself

**None of the three inspected winners frosts the bar or hangs a contrasting-colour `border-bottom` under it.** Three deliberate treatments:

- **Transparent + gradient scrim + ink inversion by section (dark cinematic).** Siena `.nav-w`: `position:fixed`, `pointer-events:none` (only the children are clickable; `pointer-events:none` appears ×4 in `main.css`), full-width, no background *bar*. Legibility comes from `.nav-w.home { background-image: linear-gradient(#000,#fff0) }` — a top-down black→transparent scrim, not a solid fill. A scroll/section-driven class flips ink: `.nav-w.on-dark .logo { color:#000 }` — cream over dark sections, black over light. No `backdrop-filter`, no `border-bottom` anywhere on the nav (**verified**).
- **Solid theme-background bar + same-family hairline (light editorial).** Anthropic `.nav_wrap { background: var(--_color-theme---background) }` (solid ivory), the hairline living on the menu panel as a `border-top` in `--swatch--ivory-medium` — a *same-family* hairline, never a contrasting accent line under the bar. Nav links are set in `--_typography---font--display-serif-family`: the chrome itself carries the editorial serif voice (**verified**).
- **Transparent bar + charcoal pill CTA + full-screen overlay menu (warm magazine).** Truekind `.navbar { position:relative; padding:1rem 0 }` transparent; the only weight is the `.navbar-cta` charcoal `#333` pill; the menu is a full-viewport `background:#fff` panel sliding in on `transform .8s cubic-bezier(.18,.71,.11,1)`; hamburger lines flip `#fff`→`#333` on `.navbar.active`. No border-bottom (**verified**).

Shared rule: the nav is either transparent-with-a-scrim or a solid same-register fill; contrast comes from **ink-colour inversion tied to the section behind it**, not from a frosted panel or a decorative underline.

### Motion and scroll

**AI-default cliché.** Every element `opacity 0→1 + translateY(30px)`, one duration (~0.6s), one easing (`ease-out` or a generic `power2`), fired once on a `top 90%` trigger and never reversible, plus decorative background parallax carrying no content.

**What the winners do instead.** Smooth scroll almost universally; larger custom cubic-bezier eases; **reversible, scroll-position-as-state** panels; motion that *pauses off-screen*. Parallax is reserved for hero photography and figure treatment, not sprinkled.

- **Custom easing set, not the defaults.** Siena ships and reuses a small named ease library: `--easeOut: cubic-bezier(.77,0,.175,1)`, `--easeOutBack: cubic-bezier(.175,0,.77,1)`, `--easeOutQuint: cubic-bezier(.23,1,.32,1)`, `--customEase: cubic-bezier(.19,1,.22,1)`; durations `--duration` in the `.6s`–`1.1s` band with `--halfDuration: .55s/.7s`, `--durationShort: .15s/.4s`, panel transitions `.9s` (**verified**, all four eases verbatim). Truekind's recurring ease is `cubic-bezier(.18,.71,.11,1)` at `.8s`–`1s` (**verified**, across link, button and animation transitions in `entry.Dzz2DK-7.css`). Two sites converge on slow expo-style out-eases around `.8–1.1s` for signature motion — well above the AI-default `0.6s`/`power2`.
- **Lenis as the smoothing substrate, in both animated registers.** Truekind runs Lenis (`document.documentElement.className === "lenis"`). Siena runs it too — `window.lenisVersion === "1.1.16"` and `<html class="w-mod-js lenis">` are both live (**verified** by browser read; `window.Lenis` / `window.lenis` are module-scoped and undefined, which is why a globals-only check reads as "bespoke, not Lenis"). GSAP, ScrollTrigger, SplitText, ScrollSmoother and Locomotive globals are all undefined on Siena, and its `app.js` is a custom **OGL**-based WebGL renderer (OGL's signature error string `gl not passed as first argument to Geometry` plus `createShader`/`shaderSource`/`compileShader`) — so the case-study line about GSAP and Three.js does not survive a live read. Dondre (GSAP ScrollTrigger + Lenis), Exat (GSAP + ScrollTrigger + SplitText + Lenis) and Bisous (GSAP) are **stated**. Smooth scroll is table stakes, not the effect.
- **Reversible scroll-pinned panels — scroll position is state.** Exat: panels replace vertically inside a pinned section, internal animations trigger only when the panel is visible, "fully reversible on backward scroll" (**stated**). The anti-cliché to fire-once reveals. **Where it fits.** Chaptered features.
- **Bespoke scroll-driven article components.** Cartier 365 authors one scroll interaction per article — *Venice Film Festival* "mimics the look and movement of a film reel", *In Time is an Illusion* "splits in two and reverses itself as you scroll", *Creative Alchemy* reveals jewellery steps on scroll (**stated**). Siena's homepage and work sliders drive a directional post-processing blur plus saturation whose intensity tracks slider speed — horizontal blur on work pages, vertical on home (**stated**). The signature is *one scroll mechanic authored per story*, not a global reveal.
- **Content-position-driven image transforms.** Dondre: "images resize, fade, and blur based on their position within the viewport"; the hero headline shifts to the top-left and becomes the logo as the page scrolls (**stated**). Photography animated by where it sits in the frame.
- **Continuous / infinite scroll as pacing.** Cartier (endless article auto-load), Bisous (bidirectional infinite slider — "the site continuously unfolds from one project to another"), Dondre (horizontal scroll on the works page) — all **stated**. 3 sites → a durable editorial-index pattern, not decoration.
- **Reveal choreography.** The quiet baseline — `opacity` + `translateY(12px)`, `0.6–0.8s`, `cubic-bezier(.16,1,.3,1)`, masked word splits — is sound. Winners push signature reveals slower (`.8–1.1s`) on the custom eases above, and mask by line or word so type wipes rather than fades.
- **Subtle parallax on hero photography.** Siena's WebGL filmstrip carries "a subtle parallax effect that dynamically conveys depth" (**stated**); a 5–10% differential on hero photography holds. Mid-page, parallax survives only as figure treatment (see Mid-page aliveness), never on the reading text.
- **Page transitions.** Stefan: opacity fade `0→1` / `1→0`, **0.5s**, easing **`easeQuadInOut`** via Motion `AnimatePresence`, with `onAnimationStart`/`Complete` orchestrating scroll state (**stated**). Dondre: a camera-shutter mask that reshapes in sync with the animation (**stated**). Siena: smooth page transitions over a hybrid HTML/CSS plus progressive-WebGL layer (**stated**). The concrete light-editorial SPA pick: `0.5s` quad-in-out fade with scroll-state handoff (**single-source** for the exact numbers).

### Text effects

**AI-default cliché.** `SplitText` every heading into a `y:40, stagger:0.05` fade-up and call it typographic. Same reveal on every headline, no variable-axis motion, display type a *picked* retail font rather than an image.

**What the winners do instead.** Entrance reveals are the *supporting* layer; the *signature* is variable-font axis morphing and type-as-image scale, plus kinetic labels on interactive elements.

**Signature moves.**

- **Variable-font axis morph.** Exat: real-time weight and width transitions on hover over style names, "smooth and continuous", restricted to a single text block and single axis at a time for clarity; plus a proximity glyph grid where cursor distance drives per-glyph weight (200–900) and colour (`#0000cb`→`#FF0B00`) across seven "rings of influence", with a static fallback on touch (**stated**). **single-source** for the live implementation. Anthropic ships `font-variation-settings: "opsz" 50` on its base `.button` (single read; see Could not verify) — variable optical size in production chrome.
- **Scroll-driven 3D type rotation, used sparingly.** Exat: large typographic statements rotate on the X-axis as they enter the viewport, then "settle into place", reserved to "punctuate the experience" (**stated**). Peak accent, not a global treatment.
- **Type-as-image / masthead scale.** One display word owning the frame at 20–40vw — Brody's *The Face* move — is the register-agnostic peak; Siena's vintage-poster masthead over cinematic stills is the dark-register expression of it (**stated**). Full treatment in Type-as-image signature below.

**Supporting moves.**

- **Per-char / per-word assemble.** Stefan: words split into characters that "come together through motion", offset by index and string length, masked for a "glass-like parallax", duration **`1.25 + index*0.025`s**, stagger **`0.025`s**, easing **`easeExpOut`** (**stated**, params confirmed verbatim against the case study). The rare fully-specified char reveal.
- **Letter-by-letter opacity, restrained.** Bisous: a custom letter-by-letter opacity transition "intentionally restrained yet organic, echoing the imperfections and procedural nature of 3D rendering" (**stated**). Slower and organic, not a snappy fade-up.
- **Randomised-letter hover.** Bisous: menu and link hover states use "subtle randomized letter transformations", with hidden Easter-egg letters (**stated**). A restrained scramble — the editorial cousin of the terminal glitch.
- **Looping old-lettering rollover.** Siena: a looping rollover evoking "nostalgic theater signage" on the contact page and homepage slider (**stated**). Register-specific.
- **Preloader letter-grid resolve.** Dondre: GSAP Flip animates a scattered grid of letters that resolves into the `DONDRE GREEN` hero wordmark (**stated**) — doubles as the loader.

Rule of thumb: **one signature type move per site** — Exat is axis morph, Siena is poster masthead, Stefan is character assembly — everything else is quiet entrance reveal. Two stacked kinetic-type signatures read as a demo.

### Cursor and pointer

**AI-default cliché.** A large circular `mix-blend-mode: difference` follower with springy lag on *every* page, scaling up on every hover — the portfolio-template cursor, now a slop tell.

**The editorial default is the real system cursor.** Read live, Siena, Truekind and Anthropic all use standard cursors: `cursor: pointer` on interactive elements, `cursor: grab` on sliders and draggables, `auto`/`default` elsewhere — no custom cursor sprite in any of their CSS (**verified**, 3 sites). Siena's only pointer-driven text handler is a lens toggle that *hides* its own cursor rather than styling text: `e.onmouseover=()=>this.el.classList.add("hide"),e.onmouseout=()=>this.el.classList.remove("hide")` (**verified**, quoted character-for-character from `app.js`).

When a winner does touch the pointer, it is **content-driven, not a follower**:

- **Cursor position drives a reveal.** Dondre 404: cursor movement progressively "unblurs" sharp text — the pointer is a lens, there is no drawn cursor object (**stated**). Exat glyph grid: cursor *proximity* drives per-glyph weight and colour, touch gets a static fallback (**stated**). 2 sites → "the cursor modulates content" beats "the cursor is a decorated circle."
- **`grab`/`grabbing` on draggable media** is the one explicit cursor change worth keeping (Siena, Truekind sliders — **verified**).

The observed order: the default system cursor first, and where a custom pointer appears it *does work* (lens, proximity), never a blend-mode follower.

### Composition — how variety coheres

How a site varies its interactions across element classes (button ≠ link ≠ image ≠ nav) yet reads as one voice. Two models, one per register.

#### A. Siena — unity by shared easing, palette, and a single verb

Every element class gets a **different mechanism**; three things are held constant.

1. **The same 3–4 named eases and one duration band.** Everything runs on `--easeOutQuint (.23,1,.32,1)`, `--customEase (.19,1,.22,1)`, or `--easeOut (.77,0,.175,1)`; quiet feedback at `~.2s`, signature moves at `.5–.8s` (**verified**). Timing is the connective tissue.
2. **A two-ink inversion palette plus one red accent.** Cream `--white: #faf7ef` / `#fff` ↔ black `--black: black`, red reserved for emphasis (`.review-slide-cont:hover → color:red`) (**verified**).
3. **One shared verb — something rolls, swaps, or inverts.** The mechanism differs; the *gesture* rhymes.

Mapped across classes (all **verified** from CSS):

| element class | mechanism | loudness | timing |
|---|---|---|---|
| Nav links | siblings dim to `opacity 70%`, target holds `100%` | quietest | `.2s` |
| Menu rows | `.dot` shrinks to `0`, direct-link arrow scales in | quiet | `.2s` |
| Primary CTA (`explore`) | outline shape fills white, two-layer label roll | loudest | `.8s`, stagger `.1s` |
| Secondary CTA (`all-work`) | full black-fill inversion, nested arrow inverting opposite | medium | `.5s` |
| Slides | text recolours to the red accent | medium | — |
| Images | contained `scale(1.1)` | quiet | — |
| Footer links | `opacity` + arrow `rotate(-135deg)` | medium | `.8s` |

Variety lives in mechanism and loudness — dim, swap, roll, invert, zoom, rotate; unity lives in easing, palette, and the roll/invert verb. That is why seven different hovers read as one hand.

#### B. Anthropic — unity by token discipline, one timing, and serif chrome

Fewer moving parts; coherence enforced by a **token system** where every hover swaps to a `-hover` token on one shared transition.

1. **One transition signature everywhere:** `transition: border-color .2s, color .2s, background-color .2s` on buttons, `text-decoration-color .2s` on links (single read; see Could not verify). Every element animates on `.2s`.
2. **Every hover is a swap to a `*-hover` token**, so state changes are systemic, never ad-hoc (single read; see Could not verify).
3. **The serif voice reaches into the chrome** — nav links use the display-serif family, `.button` carries `font-variation-settings: "opsz" 50` (single read; see Could not verify).

Mapped across classes (single read; see Could not verify): primary CTA fills the full clay accent with token-inverted text; secondary/code CTA takes the one restrained neutral step (`cloud-light`); play button does a full background↔text inversion; links materialise an underline via `text-decoration-color: transparent → ink` with the offset varying by context (`.2em` nav / `.18em` dropdown / `.25em` footer); the nav is a solid ivory bar with a same-family hairline and serif links.

Variety lives in *which property changes* — background, decoration-color, border; unity lives in the shared `.2s` timing, the token system, and the serif carried into the nav.

**The transferable rule:** cohere on **easing + palette + one gesture** (Siena) or on **a token system + one timing + a type voice in the chrome** (Anthropic), then let each element class use a *different* mechanism. The common failure is the inverse — identical mechanism everywhere, no shared connective grammar underneath.

### Anti-signals — absent from every winner examined

- **A pale or low-opacity accent-tint fill on button hover.** Zero occurrences across Siena, Truekind, Anthropic. Winners fill the *full* token and invert the label; the only near-tint is Anthropic's single neutral step on secondary and code buttons.
- **A frosted `backdrop-filter: blur()` nav bar with a contrasting `border-bottom`.** None of the three inspected navs frosts or hangs a contrasting underline.
- **The `mix-blend-mode: difference` circular cursor-follower.** No custom cursor sprite in any inspected CSS.
- **Uniform fire-once `y:30, 0.6s, ease-out` reveals on everything.** Winners use slower custom eases (`.8–1.1s`, expo/quint), mask by line or word, keep panels reversible, and author a bespoke scroll mechanic per story.
- **A generic percentage-counter preloader.** The intro either *is* the first section unfolding, tracks real load state behind a plain sheet (Truekind), or is absent (Anthropic) — never a count to 100 over a page that needed no loading.
- **The same interaction mechanism cloned across button, link, image and nav.** The defining editorial move is a different mechanism per element class held together by shared easing, palette and timing.
- **`text-decoration: underline` snapping on instantly.** When links underline it is *drawn* (`scaleX` from origin-left, Truekind) or *faded* (`text-decoration-color` transparent→ink with a tuned offset, Anthropic) — never an instant toggle.

---

## Page recipe

### Per-winner scroll-throughs

Intensity is a comparative 1–10 estimate of attention load (defined in `../winners/composition-chains.md`).

**Siena Film Foundation** — a gated single-page immersive reel, not a vertical scroll.

1. **ENTER gate + onboarding overlay** — attention — a fixed full-viewport black panel (`.preloader-w`, `background-color:var(--black)`) carrying a `50svh` video, the instruction strings, and a slide-up ENTER button; intensity 6; seam: the gate dismisses into the reel.
2. **Featured-film masthead** — attention — oversized display title over a full-bleed treated still + metadata stamp (`SAVOY / DOCUMENTARY / 2022 / MIN.77`); intensity 9; seam: hold-and-drag into the filmstrip.
3. **Horizontal filmstrip of 8 works** — understanding/proof — each film a treated still with a jury pull-quote; `Savoy → Moon in the 12th House → Taboo → Kafka's Last Trial → My Project X → Ana Maxim → Outsider Freud → By Any Means`; intensity 8; seam: `EXPLORE` opens a case-study detail.
4. **Case-study detail** (per film) — proof — parallax photo-driven story; intensity 7.
5. **Contact / footer close** — close — `LET'S TALK`, `EMAIL US`, oversized wordmark; intensity 6.

Totals: ~8 films behind one gate; length is lateral (drag), not a tall scroll; climax at the masthead, rest inside case studies. Structure **verified** from the raw HTML — no `<h1>` (count 0), `<h2 class="roll-cont-he home">Savoy`, 8 film items, EXPLORE → case study, footer contact. Only `SAVOY` is DOM-confirmed live; the other seven titles render inside the WebGL canvas and are **observed** from the source HTML rather than the rendered page.

**Truekind Skincare** — one long warm-magazine scroll, ~14–16 movements, `scrollHeight` **8998px** (**verified** live).

1. Type-pledge hero (`True to Oneself kind to Nature`) — attention — 9.
2. `Clean, Conscious, Performance skincare.` — understanding — 6.
3–5. Value chapters: `Clean, Beyond Reproach` / `Radical Transparency` / `Potent & Multi Tasking` / `Conscious & Responsible` — proof — floating product stills — 7.
6. `Explore pure potency` → product index (`Pure Brilliance`, `Varnaya Blends`) — proof/close — 7.
7. `Radical Transparency. Hide Nothing.` → `100% Transparent Formulas` / `Only Verified Ingredients` — proof — 6. The second line is unadjudicated between `Only Verified Ingredients` and `Only proven Ingredients`.
8. `Exciting offers awaits` / `clean Journal` (journal teaser) — understanding — 5.
9. `Connect With Us` / `on instagram` (social grid) → footer — close — 6.

Totals: ~14 viewport-heights; climax at hero and product reveal; rest in the journal teaser. Section list and hero **verified**; the value-chapter headings and product names above are separately confirmed present.

**Anthropic** — a light-editorial multi-page standfirst stack.

1. Statement-serif hero (`AI research and products that put safety at the frontier`) + standfirst — attention — 8.
2. `Anthropic is built on hard questions.` — belief section, 5 h3 links (`Core views on AI safety`, `Anthropic’s Responsible Scaling Policy`, `Anthropic Academy: Build and Learn with Claude`, `Anthropic’s Economic Index`, `Claude’s Constitution`) — understanding — 6.
3. `Latest releases` — card index (`Redeploying Fable 5`, `Introducing Sonnet 5`, `Announcing Claude Science`) — proof — 6.
4. `At Anthropic, we build AI to serve humanity’s long-term well-being.` — mission close — close — 6.
5. Deep tabular footer (9 columns) — close/chrome — 4.

Totals: ~6 sections, ~7 viewport-heights; even intensity, no spectacle peak — reading-first. All headings and footer columns **verified**. The release-card titles are confirmed present but **volatile** — the homepage rotates them, so no single set of names is stable.

### Named page shapes

1. **The Reel Index** (Siena; dark cinematic) — a gated body-of-work exploration. An ENTER gate opens onto a single owned featured work at full bleed with a metadata stamp; the body is a horizontal, hold-and-drag filmstrip of treated stills, each stamped with a title and a jury pull-quote; a left work-index menu quick-jumps, a right menu holds About and Contact; the close is a contact reprise under an oversized wordmark. Skeleton: `gate → featured masthead → horizontal work-strip → per-work detail → contact close`. Fits film foundations, festivals, studios and agencies with a reel, cultural institutions, portfolios with a real body of work.
2. **The Standfirst Stack** (Anthropic; light editorial) — a reading-first multi-page. A serif statement H1 with a sans standfirst, a belief section of linked essays, a "latest releases" card index, a mission-statement close, a deep tabular footer. No preloader, no spectacle peak; the chrome carries the serif voice. Skeleton: `serif-statement hero → belief index → release cards → mission close → tabular footer`. Fits research orgs, institutions, publishers, mission-driven companies, long-form brands.
3. **The Floating Editorial Scroll** (Truekind; warm magazine) — a single long scroll of alternating value chapters. A type-led pledge hero, then transparency, potency and responsibility chapters carrying floating product photography, a product index, a journal teaser, a social-grid connect close. Lenis smooth scroll throughout. Skeleton: `type-pledge hero → value chapters w/ floating product → product index → journal teaser → connect/social close`. Fits fashion, lifestyle and luxury e-commerce with story content, brand-story commerce, coffee-table digital companions. The Codrops study documents "a floating layout"; the parallax differential is **observed, implementation unverified** at the hero — live mid-page image parallax is separately verified (see Mid-page aliveness).

### Hero architectures

#### 1. Featured-work masthead (Siena; dark cinematic)

No H1 tag — the first fold **is** the featured film. Skeleton: oversized display title (**Neue Brucke**) at the optical centre over a full-bleed treated still; metadata stamp beside it in **P22 Parrish Roman**; nav is a `pointer-events:none` scrim, no bar; one `EXPLORE` CTA. Entrance is the **two-layer kinetic label roll** — each headline character is doubled, the visible copy slides out while the duplicate rolls in, recolouring to ink. The bundle carries its own `SplitText` + `cloneNode` + `duplicate` path (**verified** by grep of `app.js`); GSAP's plugin globals are absent from the live page, so the splitting is the site's own code, not the GSAP plugin.

| element | order | transform | duration | easing |
|---|---|---|---|---|
| headline chars (visible) | 1 | `translate(100%)` out | `.8s` | `--easeOutQuint` `cubic-bezier(.23,1,.32,1)` |
| headline chars (duplicate) | 1 (stagger `.1s`) | `translateY(-150%)` in | `.8s` | `--easeOutQuint` |
| panels / stills | 2 | clip/scale reveal | `--panels-duration .9s` | `--customEase` `cubic-bezier(.19,1,.22,1)` |

Structure, `pointer-events:none` scrim, metadata stamp, eases and `--panels-duration: .9s` **verified**; the doubled-char literal DOM is **observed** (mechanism corroborated in the bundle, not read on the rendered page).

#### 2. Statement-serif split (Anthropic; light editorial)

Serif H1 owning the reading measure, sans standfirst directly below, restrained or absent hero image, a persistent accent-token nav CTA (`Try Claude`) filling the full clay swatch. Reading-first; the display face is the custom `'Anthropic Serif'` — `var(--_typography---font--display-serif-family, 'Anthropic Serif'), Georgia, serif` verbatim. The site is Webflow-hosted (`cdn.prod.website-files.com/67ce28cfec624e2b733f8a52`, ×36 in the document). Entrance is a quiet line-mask reveal, no spectacle (**verified**).

#### 3. Type-pledge + floating product (Truekind; warm magazine)

A short pledge headline (`True to Oneself kind to Nature`) set in `font-family: Editorial New, serif` display over `font-family: PP Mori, sans-serif` body — both declared in the SSR HTML, foundry Pangram Pangram confirmed by the case study (which spells the display face "Editorial Neue"; the live declaration is `Editorial New`, and the live value is the one to build against). Product photography floats in cream negative space; a scroll cue rather than a hard CTA (**verified** for H1 and fonts).

**Character-assembly variant** (Stefan, supporting) — chars slide in along x with masked glass-like parallax, `duration 1.25 + index*0.025`s, stagger `.025`, `easeExpOut`; positions `left: (index/total)*100%`, `width: 100/total+0.01%` (**stated**, params verbatim from the case study; **single-source**).

### Loader and intro

One intro per register: dark cinematic **seeds the first frame**, warm editorial ships a progress-tracked sheet, and the light control **paints instantly**.

- **Gate-into-fold** (Siena) — the gate is its own fixed full-viewport panel, not a layer over the featured still: `.preloader-w{position:fixed; inset:0; z-index:99999999; background-color:var(--black); display:none}` with `.show{display:flex}`, carrying a `.preloader-video{height:50svh}` (`100svh` on mobile) and a `.preloader-btn{transform:translateY(200%); font-family:Neue Brucke}` that slides up into place (**verified** CSS, [`../surfaces/preloaders.md`](../surfaces/preloaders.md)). Onboarding strings, CSS-uppercased on render: `Hold and drag to navigate the content` · `Scroll to unlock the immersive film experience` · `Click on left-side menu to Quick navigate Films` · `Use the right menu for seamless navigation`. A ticket-stub metaphor stamps `SIENA ADMIT ONE 004`. The gate dismisses **into** the composed masthead — the neo-romanesque intro stripes resolve into the first film. All four onboarding strings **verified** verbatim in the HTML (live DOM shows the uppercased render, e.g. `HOLD AND DRAG TO NAVIGATE THE CONTENT`); the admit-one stamp and stripe handoff are **observed**.
- **Instant paint** (Anthropic) — no preloader layer; reading starts on load and the scroll reveals are the intro. Zero loader classes and zero preload-state tokens across the light-editorial control (**verified** absence, [`../surfaces/preloaders.md`](../surfaces/preloaders.md)). A page-level pattern, not an absence of craft.
- **Progress-tracked sheet** (Truekind) — `.preloader{color:#fff; height:100dvh; position:fixed; inset:0; z-index:9999}` plus `.preloader__inner`; the DOM ships `<div class="preloader">` and `reveal-waitpreloader` (×2), and the bundle carries `$sstatePreloadProgress`, `$sstatePreloadDone`, `$sstatePreloaderItems` (**verified** CSS, DOM and bundle, [`../surfaces/preloaders.md`](../surfaces/preloaders.md)). The case study describes no loader; the shipped build carries one, and it sits in the same white arrival family as `.base-overlay-transition` and `.clone-transition` ([`../surfaces/route-transitions.md`](../surfaces/route-transitions.md)).
- **Grid-flip-into-wordmark** (Dondre) — a grid of random letters carries `DONDRE GREEN` overlaid; the letters reserved for the hero text sharpen and fade in while the rest blur and fade out; **GSAP Flip** transitions the reserved letters into the hero wordmark (**stated**). The cleanest loader→hero handoff in the corpus.
- **Loader-into-slider** (Bisous) — "A succession of carefully curated visuals appears during the loading phase… this sequence also serves as the foundation for the homepage slider, creating continuity between the loading experience and the main navigation flow." No cross-fade, no curtain — the loader's frames **are** the slider's first frames (**stated**, quoted verbatim).

### Route transitions

- **Product-colour flood** (Truekind) — the transition to a product view "uses a solid color from the product background, expands it to full screen, and then switches the page seamlessly" (**stated**, case-study author quote, confirmed verbatim). The shipped transition layers read white, not product-coloured: `.base-overlay-transition` and `.clone-transition` are both `#fff`, and `.preloader` joins them in one white arrival family in the served CSS ([`../surfaces/route-transitions.md`](../surfaces/route-transitions.md)). No product colour appears in the transition rules read, so the flood stands as case-study prose against a measured white default.
- **Camera-shutter mask** (Dondre) — Barba.js; a dynamic mask reshapes into "the motion of a shutter closing inward and expanding outward", a cinematic metaphor rhyming with the subject (**stated**).
- **Cross-fade** (Stefan) — Motion `AnimatePresence mode="wait"`; `initial opacity:0 → animate opacity:1 → exit opacity:0`, `duration:0.5, ease:easeQuadInOut` (**stated**, **single-source**). The quiet default.
- **Continuous unfold** (Bisous) — no discrete route change; the transition is "almost imperceptible, as if the website itself continuously unfolds from one project to another" (**stated**, verbatim).
- **Classic MPA, no scripted transition** (Anthropic) — separate documents, browser paint; the language is quietness itself (**observed**; the page loads GSAP but claims no route-transition scripting).
- **In-SPA film→case-study** (Siena) — `EXPLORE` opens the detail within the immersive shell; the transition language rhymes with the drag and the filmstrip (**observed**).

Rhyme rule: the route transition echoes the loader's language and the subject matter — a shutter for a photographer, a colour flood for a product, an unfold for a continuous reel.

### Copy voice

Verbatim strings, character-for-character from live DOM or raw HTML.

**Siena Film Foundation** (**verified**)

- Film titles (h2): `Savoy` · `Moon in the 12th House` · `Taboo` · `Kafka's Last Trial` · `My Project X` · `Ana Maxim` · `Outsider Freud` · `By Any Means` — 7 appear literally in the HTML; `Kafka&#x27;s Last Trial` is the entity form of a straight apostrophe.
- Jury pull-quotes (h3): `"Fast-paced and engrossing"` · `"History through a heroine"` · `"Brave, poetic, liberated"` · `"BreathtakiNg cinematography"` · `"Delicate and moving"` · `"Pure cinematic beauty"` — the odd casing in `BreathtakiNg` is verbatim.
- Metadata stamp: `SAVOY / DOCUMENTARY / 2022 / MIN.77`.
- Onboarding: the four strings above, plus `CLICK 'EXPLORE' TO VIEW DETAILED CASE STUDIES`.
- Nav: `WORK` · `About` · `Contact` · `COOKIE` · `TERMS` · `PRIVACY`.
- CTAs: `EXPLORE` (×17 in the document) · `SEE CASE` (×8) · `EMAIL US` (×1). The per-film label a reader sees is `EXPLORE`, driven by `[data-btn=explore]`; the `SEE CASE` strings are present in the raw HTML but do not surface in the live DOM, where the reel renders to canvas.
- Footer: `©2024. SIENA FILM FOUNDATION.` · `lee@siena.film` · `LET'S TALK` (`LET&#x27;S TALK` in source).

**Anthropic** (**verified**)

- H1: `AI research and products that put safety at the frontier`
- Subhead: `AI will have a vast impact on the world. Anthropic is a public benefit corporation dedicated to securing its benefits and mitigating its risks.`
- Section headings: `Anthropic is built on hard questions.` · `Latest releases` · `At Anthropic, we build AI to serve humanity’s long-term well-being.`
- Belief-index links: `Core views on AI safety` · `Anthropic’s Responsible Scaling Policy` · `Anthropic Academy: Build and Learn with Claude` · `Anthropic’s Economic Index` · `Claude’s Constitution`
- CTA: `Try Claude`
- Footer copyright: `© 2026 Anthropic PBC`

**Truekind Skincare** (**verified**)

- H1: `True to Oneself kind to Nature` — read from the rendered DOM; the SSR markup splits it across tags (`True<tag> to Oneself`), so a contiguous grep of the source misses it.
- Section headings: `Clean, Conscious, Performance skincare.` · `Radical Transparency. Hide Nothing.` · `Explore pure potency` · `Connect With Us` · `on instagram`
- Value chapters and products: `Clean, Beyond Reproach` · `Potent & Multi Tasking` · `Conscious & Responsible` · `Pure Brilliance` · `Varnaya Blends` · `clean Journal`
- CTAs: `Explore All Products` · `Shop Now`
- Footer: `© 2025 TrueKind, All Rights Reserved` · `Website By:` (credit line)
- The hero subhead is left unquoted: two sources disagree on its first word (`Unreservedly…` vs `Undeservedly honest products that truly work, be kind to skin and the planet`).

**Apostrophe fidelity.** Straight versus curly differs by site and a rebuild must copy each per its source glyph: Siena entity-encodes a **straight** `'` (`&#x27;` — `Kafka's Last Trial`, `LET'S TALK`); Anthropic uses a **curly** `’` (U+2019, raw UTF-8 — `humanity’s`, `Claude’s`, `Anthropic’s`).

#### Voice formula per register

- **Dark cinematic (Siena)** — third-person and impersonal, the institution speaking as curator. Fragmentary sentence length: titles, stamps, two-word jury quotes; verbs live in the imperative onboarding (`Hold and drag`, `Scroll to unlock`). Punctuation signature: the terminal period on the wordmark (`©2024. SIENA FILM FOUNDATION.`), quotation marks around every jury line. Refuses adjectives about itself, self-description, any "a film foundation dedicated to…". Proof is borrowed from the jury, never claimed.
- **Light editorial (Anthropic)** — first-person plural institution (`we build`, `Anthropic is`). A declarative H1 fragment, then full standfirst sentences. Cool mission verbs (`securing`, `mitigating`, `serve`). Full stops on section headings turn them into statements (`built on hard questions.`). Refuses hype adjectives, exclamation, feature-listing in the hero.
- **Warm magazine (Truekind)** — brand-to-reader pledge, second person implied. A compressed poetic hero (`True to Oneself kind to Nature` — no comma, deliberate), then plain-spoken value headings. Sentence-fragment headings with terminal periods (`Performance skincare.`, `Hide Nothing.`); lower-case affectations (`clean Journal`, `on instagram`). Refuses clinical ingredient-speak in display copy, keeping chemistry to the transparency chapters.

Shared refusal across the line: **the site never narrates or credits itself in body copy** — no "a feature on…", no listing its own typefaces; the only self-credit is a discreet footer line (`Website By:`).

### Imagery art direction

One treatment held page-wide per site; photography earns full bleed while text keeps its measure.

- **Siena** — cinematic film stills, treated (desaturated, high-contrast, duotone-leaning), full-bleed, with vintage-poster display type overlaid. Wide edge-to-edge crops, cinematic source light kept, near-black substrate with cream type (`--white: #faf7ef`). One treatment, dark.
- **Truekind** — product-as-still-life floating in cream negative space; warm soft light, clean colour; the product is the hero, never a lifestyle stock frame (**stated** + **observed**).
- **Anthropic** — not photography-led; terracotta and clay accents on cream and ivory, restrained brand graphics and illustration; warmth carries the editorial read (**observed**).
- **Dondre** — narrative photography revealed on interaction, serif and sans contrast guiding the eye; treated, never raw (**stated**; the reveal behaviour is documented, the WebGL-displacement mechanism is not named in the study).

Formula: **subject owned, not stock; one grade page-wide; treated, not raw; full bleed for image, protected measure for text.** Stock photography is the fastest fail per the line's own DNA.

### Footer

1. **Wordmark-contact-close** (Siena) — a designed moment: the institution wordmark oversized, `©2024. SIENA FILM FOUNDATION.`, contact reprise (`LET'S TALK`, `EMAIL US`, `lee@siena.film`), ticket-stub metaphor. Close-first, not chrome (**verified** copy).
2. **Tabular index** (Anthropic) — 9 column headings: `Products` · `Models` · `Solutions` · `Claude Platform` · `Resources` · `Programs` · `Help and security` · `Company` · `Terms and policies`; `© 2026 Anthropic PBC`; LinkedIn / X / YouTube. CSS recipe: the footer wrap `background` is the theme-background ivory, the section boundary is a **same-family hairline** (`border-top` in `--swatch--ivory-medium`) never a contrasting rule, and the links are set in the display serif so the chrome carries the editorial voice (columns **verified**; CSS recipe **stated**).
3. **Social-grid functional-plus** (Truekind) — `Connect With Us` / `on instagram` Instagram grid, `© 2025 TrueKind, All Rights Reserved`, contact email and phone, `Disclaimer` / `Credits`, `Website By:` credit (**verified** copy).

### Spectacle menu — the passage a judge replays

- **Siena — the hold-and-drag filmstrip.** Trigger: grab the reel (`grab` cursor) after the ENTER gate. Beats: drag horizontally → treated stills slide past → each film title rolls in via the two-layer kinetic label (doubled chars, `--easeOutQuint`, `.8s`) → `EXPLORE` opens the case study. Payoff: the site behaves like a physical reel threaded by hand. Replayable because it is a tactile metaphor, not a scroll (eases **verified**, choreography **observed**).
- **Truekind — the product-colour flood.** Trigger: click a product. Beats: the product's background colour floods to full-screen → the page swaps beneath it → the new view resolves in that colour. Payoff: a colour-matched page change — the case-study author's proudest moment (**stated**; the shipped cover layers measure white, see Route transitions above).
- **Dondre — focus/defocus gallery plus cinematic reel.** Trigger: hover a story thumbnail. Beats: the hovered figure sharpens while siblings blur and dim → the works page scrolls **horizontally** like a film reel → the 404 unblurs a lens under the cursor. Payoff: attention is physically directed (**stated**).
- **Bisous — the continuous unfold.** Trigger: keep scrolling the vertical slider, infinite in both directions. Beats: projects unfold into one another with no navigation break. Payoff: the whole site reads as one uncut take (**stated**).
- **Stefan — character-assembly entrance.** Trigger: page or hero enter. Beats: chars slide in masked with glass parallax, `duration 1.25+index*0.025`, stagger `.025`, `easeExpOut`. Payoff: type that assembles itself (**stated**, **single-source**).

### Named values

Committable by name, all **verified** off the site's own assets.

| value | site | source |
|---|---|---|
| `--easeOut: cubic-bezier(.77, 0, .175, 1)` | Siena | `main.css` |
| `--easeOutBack: cubic-bezier(.175, 0, .77, 1)` | Siena | `main.css` |
| `--easeOutQuint: cubic-bezier(.23, 1, .32, 1)` | Siena | `main.css` |
| `--customEase: cubic-bezier(.19, 1, .22, 1)` | Siena | `main.css` |
| `--panels-duration: .9s` | Siena | `main.css` |
| Substrate `#000000` via `:root{--black:black}` + `body{background-color:var(--black)}`; secondary `#0e0e0e`; cream `--white:#faf7ef` | Siena | Webflow CSS — `#000000` ×20, `#0e0e0e` ×10 |
| Body/nav `NB International` (`NB International Regular.ttf`); display `Neue Brucke` (`NeueBrucke-Regular.ttf`) on `.roll-cont-item`, `.top-m-film-title`, `.menu-film-title`; vintage-poster metadata eyebrow `P22 Parrish Roman` (`P22 Parrish Roman.ttf`) on `.roll-cont-eyeb.parish` | Siena | site assets |
| State hooks: `[data-a]` values `y` and `line` (49 nodes), `[data-hover]` values `["bggrow","mainlinkgroup","mainlink"]`, `[data-menu]` ×65, `[data-btn]` = `["explore"]` | Siena | live DOM |
| `var(--_typography---font--display-serif-family, 'Anthropic Serif'), Georgia, serif`; Webflow CDN `cdn.prod.website-files.com/67ce28cfec624e2b733f8a52` | Anthropic | raw HTML |
| `font-family: PP Mori, sans-serif` (body) + `font-family: Editorial New, serif` (display), foundry Pangram Pangram | Truekind | SSR HTML + case study |
| Unified ease `cubic-bezier(.18,.71,.11,1)` | Truekind | `entry.Dzz2DK-7.css` |
| `scrollHeight` 8998px | Truekind | live DOM |

### Anti-signals — page-level absences

No winner in this line, across registers, does any of the following:

- **No card-grid opener.** The first fold is a single owned thing — a featured film, a serif statement, a type pledge — never a gallery of tiles or a "featured posts" grid.
- **No generic percentage-counter preloader.** Loaders either seed the first frame (gate-into-fold, grid-flip-into-wordmark, loader-into-slider), track real load state behind a plain sheet (Truekind), or are absent (Anthropic). None counts to 100 over a page that needed no loading.
- **No hero carousel or rotating banner.** Horizontal motion, when present, is a hand-dragged reel or an infinite slider that *is* the content.
- **No centered-hero-with-generic-headline plus twin-CTA template.** Heroes are asymmetric statements or featured works.
- **No frosted nav bar with a contrasting `border-bottom`.** Contrast comes from ink inversion tied to the section behind.
- **No wall of poured text.** Sections alternate media and rest; dense passages break for a pull-quote or a full bleed. Reading-*first*, never text-*dense*.
- **No self-narration in body copy.** The page never describes its own construction or lists its typefaces.
- **No raw stock photography.** One treated grade holds page-wide.
- **No mixed copy register.** One voice per page — an editorial standfirst and a technical HUD readout do not co-exist.

---

## Mid-page aliveness

What keeps the zone between hero and footer alive at the line's ceiling — the zone where editorial builds routinely land at 7.2–7.4 with praised heroes and image reveals and prose sections that read dead.

### Why the dead middle is not a text-effect problem

A dead middle is not fixed by mid-prose text effects, because the higher tier does not ship them. It is fixed by the four carriers below.

### Register strategies — the two registers solve the dead middle by opposite means

#### Siena (7.9, dark cinematic) — eliminate the prose middle

Siena has **no tall prose zone at all.** `document.documentElement.scrollHeight === window.innerHeight` — the document never grows. The absolute figure is whatever the viewport measures — `676px` here, `630px` in [`immersive-cinematic.md`](./immersive-cinematic.md); the finding is the equality, not the number. "Scroll" is a **virtual scroller**: input drives a `transform: translateY()` on `.menu-w` (measured live at `matrix(1,0,0,1,0,-206)`, translateY −206px exact), synced to a full-viewport WebGL `<canvas>` of 2880×1352 device pixels (CSS 1440×676 at DPR 2). Lenis supplies the input smoothing (`window.lenisVersion === "1.1.16"`); the WebGL layer is a custom OGL renderer in `app.js`, and the sync between them is the site's own code (**verified**).

The middle is therefore an **interaction, not a passage**: the hold-and-drag filmstrip of 8 films, each with an `EXPLORE` CTA. Aliveness comes from the user's own hand dragging the reel, from the WebGL treatment passing over the stills, and from `[data-a=y]` attribute-driven title reveals. There is nothing to keep alive because there is no reading pause — the film titles are the content and they move when grabbed.

The dark-cinematic answer to dead prose is to **not ship prose walls**: convert the middle into one hand-driven spectacle.

#### Truekind (7.47, warm magazine) — keep the prose, carry it on four thin channels

Truekind is a real 8998px vertical scroll with a genuine prose middle (`Clean, Conscious, Performance skincare` → `Explore pure potency` → `Radical Transparency.` → `Only proven Ingredients`). Its middle stays alive on exactly four channels, none of them a mid-prose text effect:

1. **Lenis smooth-scroll inertia** (`html.lenis` live). The whole passage feels driven because the wheel is eased; the primary aliveness carrier, and it costs one library (**verified**).
2. **Headline line and word-split reveal, fire-once.** Headings split into `.line` (24 instances) and `.word` (4). Each line rides a `translateY` resolving as the heading enters — measured on "Explore": `translateY(71.3px)` off-screen → `1.67px` at centre → `0` past it, reproducible to the decimal at `71.28` → `1.65` → `0`. Opacity holds at 1 throughout: a **masked translate reveal, not an opacity fade** (**verified**).
3. **Hover life on the interactives that punctuate the prose** — the link underline draw, the CTA fill-inversion, the marquee label, the product-card crossfade. Prose is dotted with buttons, links and cards, and *those* respond; the paragraphs do not.
4. **Contained image treatment** — product stills sit at rest `scale(1.2)` inside `overflow:hidden`, crossfading to a second image on hover; section imagery reveals on scroll via a fade/clip class.

Mid-page idle motion is **absent on the current deployment**: zero infinite animations run across all elements, and the only keyframes in the loaded CSS are `spin-…`, `marquee` and `fadeIn-…` (**verified** live). The current deployment (Nuxt payload `prerenderedAt` ≈ 24 Jun 2025) ships no always-running scroll cues at section edges, and no decorative ambient loop lives inside the reading column.

#### Anthropic (control, light editorial) — even intensity, reveal-only

The standfirst stack quoted above under Page recipe carries all four headings **verified** on the rendered page. Instant paint, `opacity` + `translateY(12px)` reveals at 0.6–0.8s, token-swap accents at `.2s` (**corpus** — not read off Anthropic). Reading-first, no scrubbed decor.

**Inventory synthesis.** The alive-middle inventory at this tier is short — smooth scroll, one masked-translate reveal per heading, hover on the interactive punctuation, treated imagery. The reader's *eye cadence* is the effect; the prose itself carries almost no animation.

### Hover on text specifically

**The tier ships almost none on the reading register.**

A full enumeration across `document.styleSheets` on Truekind returns **41 hover rules on the homepage and 50 on a product page** (53 raw `:hover` occurrences) — the count is chunk- and page-dependent. Every text-touching rule among them is one of four:

- `.blog__feed-item:hover .blog__title { text-decoration: underline }` — a plain underline on a card title, triggered by hovering the **card**, not the text.
- `#p-detail .p-detail__recommend-item-wrapper:hover h3 { text-decoration: underline }` — the same card-triggered pattern.
- `.cart-drawer__item-title:hover { text-decoration: underline }` — UI chrome, not prose.
- `#p-slider .p-slider__tab ul li:hover { color: rgb(120,120,120) }` — a tab-strip item dims; nav, not reading copy.

**Zero rules hover-respond on body prose, in-flow headings, numerals, or reading list-rows.** No colour sweep along text, no per-char rise, no weight or optical-size shift on hover, no background highlight. The register's entire text-hover vocabulary is `text-decoration: underline` on titles when their container is hovered (**verified**, full enumeration).

Siena is barer still: `main.css` carries 24 `:hover` occurrences and none is on a text element; `out.css` carries 0. The only pointer-driven text handler in `app.js` is the cursor-lens toggle, which hides the custom cursor rather than styling the text (**verified**).

Where the tier does put hover craft is on the **interactives sitting inside prose** — the actual mid-page life:

```css
/* Truekind — origin-left underline draw on links; the sheet uses single-colon `:before` */
.link:before { background:#3b3b3b; height:1px; left:0; top:100%; width:100%; }
.link.active:before, .link:hover:before { transform:scaleX(1); transform-origin:0 50%; }
.link.active:hover:before { transform:scaleX(0); transform-origin:100% 100%; } /* retracts rightward when already active */

/* full-fill ink inversion, never a pale tint */
.btn.outline:hover { background:rgb(59,59,59); color:rgb(255,255,255); }

/* kinetic marquee label */
.btn:hover > .marquee-parent { opacity:0; }
.btn:hover .marquee__inner { animation-play-state:running; opacity:1; transition-duration:.4s; }

/* product image crossfade-swap (two stacked stills) */
.product__card:hover .product__card-img  { opacity:0; }
.product__card:hover .product__card-img2 { opacity:1; }

/* settle-zoom: journal image sits >1 at rest, relaxes to 1 on hover */
.journal__card:hover img { transform:scale(1); }
```

All **verified** from the live sheets. The coherence tell: every hover is a variant of one gesture — something fills, draws, or swaps — welded to the shared ease `cubic-bezier(.18,.71,.11,1)`.

Adding hover colour-sweeps to headings and prose to fight a dead middle invents a register the 7.9 tier does not ship. The tier's hover budget goes entirely to links, CTAs and figures. Prose stays still by design.

### Re-fire behavior — what replays versus what fires once

- **Content reveals fire once and persist.** Truekind's heading line-reveal was driven repeatedly: `translateY 71.3 → 0` on first entry, then **stayed at 0** when scrolled past, scrolled back to centre, and scrolled to the top — all reading `matrix(1,0,0,1,0,0)`, opacity 1. It never re-displaced, across a four-stage driven-scroll test (**verified**).
- **The reading text is never scroll-scrubbed, but figures can be.** Sampling 400 mid-page elements at scrollY 1400 / 2200 / back-to-1400, **6** vary with scroll and return — classed `parallax-scroll` / `parallax-image` / `ingredients__image parallax` in the ingredients section, e.g. `ingredients__image` at translateY `−62.3` @1400 → `0` @2200 → `−62.3` on return (**verified** by browser read). None touches `.line`, `.word` or prose text. Corrected scope: prose *text* is never scrubbed; *figures* are.
- **The re-playing channels are input-driven.** Siena's filmstrip re-plays every time it is dragged; the marquee label re-plays every hover. Neither is welded to scroll position. Siena's scroll is virtual (a transform on `.menu-w`), and the reveals it triggers are `[data-a]` one-shots, not scrubbed loops (**verified**).

"Effects that re-play on scroll" describes a mechanic the editorial tier avoids in prose. What re-plays here re-plays on *hand input* — drag, hover — not on scroll passes. Content persists; a scroll-scrubbed text effect welded to the prose middle diverges from the line rather than matching it.

### Smooth scroll

**Near-universal at the top of the line, and the mechanism is Lenis in both animated registers:**

- **Warm magazine (Truekind): Lenis** — `document.documentElement.className` is exactly `"lenis"`. The instance config is sealed in Nuxt module scope and unreachable from `window`, but the class is Lenis's own signature (**verified**).
- **Dark cinematic (Siena): Lenis plus a custom WebGL sync layer** — `window.lenisVersion === "1.1.16"` and `<html class="w-mod-js lenis">` are live. GSAP, ScrollTrigger, SplitText, ScrollSmoother and Locomotive globals are all undefined and `app.js` contains no `lenis` string, so Lenis arrives through a separate module while `app.js` handles a custom OGL renderer and the `.menu-w` transform. Undefined globals are a module-scoped build, not an absent library — GSAP SplitText strings do ship in the bundle (`immersive-cinematic.md`). Lenis is the engine; the virtual-scroll behaviour and the canvas sync are the site's own (**verified**).
- **Light editorial (Anthropic): native scroll** — no smooth-scroll signal in any read; reading-first with default scroll behaviour (**observed**).

"Add Lenis" is the correct default for both the warm-magazine and the cinematic build; only the pure light-editorial register is plausibly native. The cinematic build earns a custom sync layer only if it also runs a canvas.

### Anti-signals at this tier

- **No hover effects on prose or in-flow headings** — no colour sweep, per-char rise, weight morph, or highlight on reading copy. Text-hover is `text-decoration:underline` on card titles, full stop.
- **No scroll-scrubbed text in the reading column** — nothing re-fires under the reader on scroll passes; content reveals are one-shot-persist. Mid-page parallax exists but sits on figures.
- **No decorative ambient loop inside the prose** — the current top-of-line deployment runs zero infinite animations at all.
- **No pale-tint hover fills** — outline controls fill the *solid* value and invert the label (`.btn.outline:hover{background:rgb(59,59,59);color:#fff}`), never a low-opacity accent wash.
- **No mid-prose aliveness theatre** — the tier does not compensate for reading pauses with animation; it trusts smooth scroll, treated imagery and one masked-translate reveal per heading to carry the passage, and puts its motion budget into the hero and the hand-driven spectacle.
- **Dark cinematic refuses the prose middle entirely** — Siena ships no tall reading zone, so the dead-prose failure mode cannot occur.

---

## Type-as-image signature

Editorial winners do not pick a serif well — they treat the display type as the composition. Either a genuinely bespoke or commissioned face, or a retail variable face pushed past its defaults (extreme optical size, custom axis instances) and set as a full-bleed, oversized, art-directed object. The strongest lever available without commissioning a typeface is **optical-size (`opsz`) instancing on a display variable serif** plus **treating the masthead wordmark as drawn SVG art**, not a text node.

### The levers, ranked

1. **Push the optical-size axis to a custom display instance** — the biggest win, zero commission. `opsz` is the only axis that redraws glyph outlines for size; at large values a display serif gains contrast and refinement a static font cannot. Fraunces exposes `opsz 9–144`, `wght 100–900`, plus `SOFT 0–100` and `WONK 0/1` (leaning and bulbous alternates) — an Old Style face explicitly built for art direction at display scale. How: `font-variation-settings: 'opsz' 144, 'wght' 340, 'WONK' 1;` on the masthead, decoupled from `font-size`. Sources: [github.com/undercasetype/Fraunces](https://github.com/undercasetype/Fraunces), [pixelambacht.nl/2021/optical-size-hidden-superpower](https://pixelambacht.nl/2021/optical-size-hidden-superpower/), [MDN font-optical-sizing](https://developer.mozilla.org/en-US/docs/Web/CSS/font-optical-sizing).
2. **Treat the masthead as drawn lettering / SVG, not a text node.** The exclusivity read juries reward comes from letterforms that behave "like photography does — both as flat color and dimensional" (Sawdust's bespoke *Wired* alphabet). Drawing a *single* wordmark as SVG paths — custom ligature, spliced counter, bespoke ampersand or numeral — gets roughly 80% of that read. How: hand-set the one hero word as `<svg>` outlines; body stays retail. Source: [eyeondesign.aiga.org — Type as Image / Lettering as Message](https://eyeondesign.aiga.org/making-rules-breaking-rules-the-art-of-magazine-typography/).
3. **Compose type AS the image — full-bleed, oversized, one word owns the frame.** Neville Brody's core move at *The Face*: "typography was also about image-making" — alternate a large word on a page against near-empty spreads so scale, not decoration, carries the peak. How: peak section is one display word at 20–40vw, tight negative leading, deliberate overlap or collage of a second layer. Source: the same Eye on Design piece.
4. **Animate an axis on scroll or interaction for a kinetic masthead — as accent, not as the whole idea.** Obys *Typography Principles* (Awwwards Site of the Day, Webby nominee) is a WebGL + GSAP horizontal-scroll type microsite where the type is the subject. How: interpolate `wght`/`opsz`/`slnt` on scroll via `font-variation-settings` keyframes, pausing off-screen with IntersectionObserver. Sources: [awwwards.com/sites/typography-principles](https://www.awwwards.com/sites/typography-principles), [web.dev/articles/variable-fonts](https://web.dev/articles/variable-fonts).
5. **Use the GRAD axis for hover and scroll weight shifts that do not reflow.** Grade "changes the weight without changing the widths, so line breaks do not change" — the masthead can breathe or darken on interaction with zero layout jump. How: `font-variation-settings: 'GRAD' var(--grad);` animating `--grad` from `-200` to `150`. Source: [web.dev/articles/variable-fonts](https://web.dev/articles/variable-fonts).

### The climax — composed still versus on-scroll component

The sustained climax is a composed peak spread where the type is the image **at rest**. The verified interactive winners build their climax as an *on-scroll* component instead: Siena Film Foundation (7.9, credited to Niccolò Miranda) peaks on a WebGL cinematic-filmstrip slider plus a looping rollover; Cartier *365* peaks on scroll-reactive article components — jewellery step-by-step, film reel, mirror/backwards split. Neither reads as a dominant still. The still-that-reads-as-climax comes from magazine art direction, not from a cited web-award technique: design the peak so a scrubbed frame is already the payoff — oversized type plus one hero image locked in composition — and make motion decorative on top, never load-bearing. Sources: [awwwards.com/sites/siena-film-foundation](https://www.awwwards.com/sites/siena-film-foundation), [awwwards.com — Behind the Scenes: 365 A Year of Cartier](https://www.awwwards.com/behind-the-scenes-designing-and-building-365-a-year-of-cartier.html), Eye on Design (above).

### Buildable without a commission

- **`opsz` custom instancing** on Fraunces or any `opsz`-bearing variable face — a verified free option.
- **Custom axis instances** — `GRAD`, `SOFT`, `WONK`, `slnt`, `wdth` set via `font-variation-settings`, animated on scroll.
- **One-off SVG or drawn masthead** — the single hero word hand-set as outlines with a bespoke ligature, ampersand or numeral. The strongest bespoke cheat: it reads as commissioned without a commissioned face.
- **Layout-as-composition** — extreme scale, tight negative leading, overlap and collage, type as full-bleed hero.

**Genuinely needs a bespoke face:** a *consistent commissioned alphabet used site-wide*, the Sawdust/*Wired* model. Levers 1–3 carry most of the winning read; only a full custom alphabet — every glyph, every surface — requires the commission.

### Type anti-slop

- **Retail editorial faces overexposed to the point of reading as default.** "Editorial New" (Pangram Pangram, with Locomotive) and **Bodoni Moda** are common enough on Awwwards that "Editorial New" has its own [collection page of sites using it](https://www.awwwards.com/websites/Editorial%20New/). A high-contrast Didone at default `opsz` is the jury's obvious answer. Overexposure verified via the collection page; the Bodoni-as-default read is inference from that pattern, not a cited jury quote.
- **The movie-font and academic defaults** — Trajan (dubbed "the movie font"), Papyrus, Palatino: an instant unoriginal signal. Source: [todaymade.com/blog/bad-typography-examples](https://www.todaymade.com/blog/bad-typography-examples).
- **Font left at its defaults** — no `opsz` push, no custom instance, no drawn wordmark, three or more competing families. The masthead is a text node in a picked font, not an art-directed object.
- **Motion doing the work the composition should do** — if the still frame is flat and only the interaction saves it, the climax fails a jury scrub.

---

## Could not verify

- **Anthropic's interaction CSS** — `text-decoration-color` at `.2s`, the per-context `text-underline-offset`, `font-variation-settings: "opsz" 50`, and the token-swap timings rest on a single stylesheet read. The site now serves a blank shell to automated browsers and text-only fetches return rendered text rather than the sheet, so the values stand on that one read, neither confirmed nor refuted.
- **Typeface names for Cartier** — the case study describes "grotesque visual art direction" and a "magazine editorial feeling" but does not name the faces; custom versus retail is unconfirmed. Siena's own faces were resolved from its assets (Neue Brucke, P22 Parrish Roman, NB International) — the "vintage poster typography" the case study describes is P22 Parrish Roman on the metadata eyebrow.
- **"Dominant still climax" as a named award technique** — no case study frames its climax as a sustained still; the verified winners peak on interaction. The principle is sourced from magazine design theory and applied by inference.
- **Bodoni Moda's own `opsz` range** — not independently verified; Fraunces is the recommendation where the axis ranges are confirmed.
- **Aparey** as a second free `opsz` option — named by Pixelambacht, specimen not opened, axis ranges unconfirmed.

## Refuted

- **"Siena won Site of the Month for April 2025"** — false: Site of the Day 18 Mar 2025 and Site of the Month for **March** 2025. The 7.9 and every sub-score are exact.
- **"Siena's substrate is `#141413` (`html` computes `rgb(20,20,20)`)"** — false: `#141413` / `#141414` / `rgb(20,20,20)` appear **zero** times in the site's HTML, CSS and JS. Webflow CSS sets `:root{--black:black}` and `body{background-color:var(--black)}`, so the substrate is `#000000` (×20 in assets), with `#0e0e0e` (×10) as the secondary dark.
- **"Siena's display face is `TNY`"** — false: `TNY` appears **zero** times in 700KB+ of assets. The display faces are `Neue Brucke` for titles and `P22 Parrish Roman` for the vintage-poster metadata eyebrow. Body/nav `NB International` stands.
- **"Siena runs a bespoke scroller, not Lenis"** — false: `window.lenisVersion === "1.1.16"` and `document.documentElement.className === "w-mod-js lenis"` are both live. A globals-only check reaches for the module-scoped `window.Lenis` / `window.lenis` and misses it.
- **"Siena's stack is GSAP + Lenis + Three.js (per case-study prose)"** — false on Three.js: the WebGL in `app.js` is OGL-based (`gl not passed as first argument to Geometry`). The Three.js attribution also travels through [`../analysis/scrub-fidelity-floor.md`](../analysis/scrub-fidelity-floor.md), which describes the filmstrip slider as Three.js; the `app.js` read supersedes it. The GSAP half is narrower than the globals suggest — GSAP, ScrollTrigger, SplitText, ScrollSmoother and Locomotive are all undefined as live globals, but a module-scoped build hides globals, and `linesClass:"split-line-move"` ×1, `type:"lines"` ×2 and `toggleActions:"play"` ×1 do ship in the same bundle (`immersive-cinematic.md`). Undefined globals refute the case study's *phrasing*, not GSAP's presence; the same trap produced the Gabriel/Lenis error recorded in `minimalist.md`.
- **"Siena's per-film CTA reads `SEE CASE STUDY`"** — false: the label is `EXPLORE` (`[data-btn=explore]`, instruction copy `CLICK 'EXPLORE' TO VIEW DETAILED CASE STUDIES`). `SEE CASE` exists ×8 in the raw HTML but never surfaces in the live DOM.
- **"Siena is credited to G-NS Studio"** — uncorroborated: two independent reads credit **Niccolò Miranda** ([`immersive-cinematic.md`](./immersive-cinematic.md), [`../analysis/scrub-fidelity-floor.md`](../analysis/scrub-fidelity-floor.md)) and nothing else in the corpus carries G-NS. The Miranda credit is adopted; G-NS stands unsupported rather than deleted, since neither reading was taken from the award page's credit block directly.
- **"The 8 Siena film titles are winner-verified from the rendered page"** — unsupported: only `SAVOY` is DOM-confirmed. The other seven render inside the WebGL canvas and are not confirmed by dragging the reel.
- **"Truekind ships zero reversible scroll-scrubbed transforms mid-page — 0 of 400 sampled elements"** — false: 6 of 400 vary with scroll and return, classed `parallax-scroll` / `parallax-image` / `ingredients__image parallax`, e.g. translateY `−62.3` @1400 → `0` @2200 → `−62.3` on return.
- **"Parallax in this line is hero-only"** — false: the same six mid-page ingredient figures carry it. Only the reading text is un-scrubbed.
- **"Truekind runs two idle scroll-cue loops, `.end-bottom-arrow` (`arrow-animation` 3s infinite) and a `CONTINUE TO SCROLL` label (`text-animation` 3s infinite, `translate3d(0,1.5em,0)` bob)"** — false on the current deployment: zero infinite animations run, both keyframes are absent from loaded CSS, and neither element exists in the DOM. The deployment prerendered ≈ 24 Jun 2025, after the award.
- **"Truekind's stylesheets contain 47 `:hover` rules total"** — false: the count is chunk- and page-dependent — 41 on the homepage, 50 on a product page (53 raw `:hover` occurrences). The substance, zero text-hovers on prose, holds exactly.
- **"Truekind's floating product photography carries a parallax differential, per the Codrops study"** — unsupported: the study documents "a floating layout" and no parallax. The hero parallax attribution drops to observed, implementation unverified.
- **"Dondre's focus/defocus reveal is driven by WebGL displacement"** — unsupported: the case study documents the behaviours (sharpen, blur, fade, 404 unblur) but never names the mechanism.
- **"Truekind paints instantly — no preloader layer, a verified page-level pattern"** — false: the shipped build carries `.preloader{color:#fff; height:100dvh; position:fixed; inset:0; z-index:9999}` plus `.preloader__inner`, a `<div class="preloader">` node with `reveal-waitpreloader` ×2, and `$sstatePreloadProgress` / `$sstatePreloadDone` / `$sstatePreloaderItems` in the bundle ([`../surfaces/preloaders.md`](../surfaces/preloaders.md)). Anthropic alone holds the instant-paint absence in this line.
- **"Siena's ENTER button sits over the featured still"** — false: the gate is its own fixed full-viewport panel, `.preloader-w{position:fixed; inset:0; z-index:99999999; background-color:var(--black)}`, carrying a `50svh` video and a slide-up `.preloader-btn` ([`../surfaces/preloaders.md`](../surfaces/preloaders.md)). The featured still is behind the panel, not under a translucent overlay.
