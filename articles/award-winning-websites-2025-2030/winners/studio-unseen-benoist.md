---
title: "Unseen Studio / Aristide Benoist — Skeletons Vary, Device Grammar Repeats"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "studio-skeleton", "page-structure", "unseen-studio", "aristide-benoist", "webgl", "scrollytelling", "custom-cursor", "typography"]
sources:
  - "https://www.awwwards.com/unseenstudio/"
  - "https://www.awwwards.com/sites/unseen-studio-2025-wrapped"
  - "https://www.awwwards.com/AristideBenoist/"
  - "https://www.awwwards.com/sites/aristide-portfolio-2021"
  - "https://www.awwwards.com/sites/in-cognita"
  - "https://www.awwwards.com/aristide-benoist-portfolio-2021-wins-site-of-the-month-june-2021.html"
  - "https://unseen.co"
  - "https://2025.unseen.co"
  - "https://symphonyofvines.com"
  - "https://blueyard.com"
  - "https://2025.oceanx.org"
  - "https://aristidebenoist.com"
  - "https://in-cognita-corp.com"
  - "https://arocksworld.com"
---

# Unseen Studio / Aristide Benoist — Skeletons Vary, Device Grammar Repeats

No two of Unseen Studio's five winners share a section order, and Aristide Benoist's three rebuild the page skeleton per subject over one unchanging architecture. What repeats in both bodies of work is the device layer: serial numbering under a HUD counter or selector, mono and bracketed data strips, and contact handled in an overlay or a final section rather than a footer. No `<footer>` element exists on the three sites verified mechanically, the remaining five follow the same pattern in their reads, and the section-order read covers eight live winners from two serial Awwwards authors, as structural evidence behind the archetypes. Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

## Sites inspected

### Unseen Studio

Bristol, UK. Profile [awwwards.com/unseenstudio](https://www.awwwards.com/unseenstudio/): 35 Sites of the Day (SOTD), 3 Sites of the Month (SOTM), 49 Honorable Mentions (HM).

| Site | Award | Evidence source |
|---|---|---|
| unseen.co | SOTM Feb 2023 + Developer Award | Live (curl, full HTML) |
| 2025.unseen.co ("2025 Wrapped") | [SOTD 24 Mar 2026 + Dev Award](https://www.awwwards.com/sites/unseen-studio-2025-wrapped) | Live (curl) |
| symphonyofvines.com | SOTD 15 Aug 2025 + Dev Award | Live (curl); page itself states "brought to you by Unseen Studio" |
| blueyard.com | SOTD 22 May 2025 (earlier version SOTD 8 Jan 2022) | Live (curl) |
| 2025.oceanx.org | SOTD 23 Feb 2026 | Live (curl) |

### Aristide Benoist

Profile [awwwards.com/AristideBenoist](https://www.awwwards.com/AristideBenoist/): 38 SOTD, 5 SOTM, 45 HM.

| Site | Award | Evidence source |
|---|---|---|
| aristidebenoist.com | ["Portfolio 2021": SOTD 24 Jun 2021](https://www.awwwards.com/sites/aristide-portfolio-2021) + [SOTM Jun 2021](https://www.awwwards.com/aristide-benoist-portfolio-2021-wins-site-of-the-month-june-2021.html) (earlier versions: SOTD 11 Oct 2017; SOTD 30 May 2018) | Live: full app DOM served by its own XHR endpoint (`/?xhr=true&device=d`) |
| in-cognita-corp.com | [SOTD + Developer Award, 11 Mar 2025 (score 7.53)](https://www.awwwards.com/sites/in-cognita) | Live (curl; app is one 134KB inline JS; structure read from code tokens) |
| arocksworld.com | SOTD + Developer Award, 20 May 2024 | Live: full DOM of every route served by the XHR endpoint |

Aristide's sites are client-side rendered (server body = loader only), but his hand-rolled framework exposes `<route>?xhr=true&device=d&webp=false` returning the complete app DOM as JSON, so the portfolio and AROCK skeletons below are primary evidence (actual markup), not inference. Fetched 17 Jul 2026.

## Per-site skeletons

### Unseen Studio

**unseen.co** (WordPress + house utility CSS `t-*/js-*/w-1/1`)
- Slots: loader-gate ("Enter" / "Enter without audio") → fixed nav (01 Index, 02 Projects, 03 Contact, 04 World + socials) → `main[data-router-view="homeContact"]`: WebGL world hero ("Unseen World | Drag to explore our world", Click & Hold, Toggle Sound, "Our 2025 Wrapped" banner) → "Selected Projects" filterable index (All/Branding/Digital/Motion/Experiment) → contact close h2 "Say hello" with New Business/General toggle (`div[data-content="general"|"new-business"]`) + Bristol/London addresses. No `<footer>`; the body template is literally `page-template-home-contact`.
- Hero: WebGL environment, drag + click-and-hold + audio. Close: contact section. Devices: custom cursor system (`data-cursor="navWrapper|navItem|hide"`), numbered nav, audio-gated entry, filter index.

**2025.unseen.co (Wrapped)**: `main.scroll-container--horizontal`, a horizontal 12-month story: `h1.story__intro__title` → repeating `story__section` variants (`story__text-illus`, `story__central-text`, `story__full-image`, `story__colored`) with giant split-letter month names and bracketed data strips (`[US_01_25]`, `[motion] [jan_25]`, `[SCROLL]`, `Open [+]`) → close: "Stay Tuned" end-card + socials + "[Start a project with us]" + HUD strip "1st | Unseen Studio® | [00%]". No footer.

**symphonyofvines.com**: header (fixed, gold mono kickers) → `section.world-apart-intro` (fixed 100lvh title card "The | Symphony of Vines", "Enter experience") → 4 chapter title-cards each with an instruction line ("Use your cursor to carve a glacial path", "…conduct the power of tidal rivers", etc.) → fixed `chapter-selector` HUD (numbers 1-4 + titles) → `story__end`: "The END" + credits + `projects@unseen.co` + "Restart Experience". WebGL journey; DOM is title-cards + HUD only.

**blueyard.com** (Vue/Nuxt): `section[aria-label="Introduction"][data-webgl-section="landing"]` with h1 "Will it be Utopia, or Oblivion?" → four thesis sections (Computing / Engineering / Biology / Crypto), each `data-webgl-section` with a mono uppercase h2 kicker → index table of portfolio companies (name / one-liner / "Visit site") → "Who We Are" team roster → "Back to top" + `aside` HUD counter "0 0 1 2 3 4 5 / 05". No `<footer>`.

**2025.oceanx.org** (Vue/Nuxt): fixed chapter menu (7 h2/h3 pairs) → main: split title "A Year of | Discovery" → `section#chapter-0`…`#chapter-6` (UNOC3, Around Africa Expedition, Cabo Verde, Monsoon Rise, Timor Passage, Hackathon, Summit 2025) → close "Share the | Journey". No `<footer>`.

### Aristide Benoist

**aristidebenoist.com**: a single 100KB payload serves every route (`/`, `/about`, 30 work URLs). DOM: `canvas#gl` + `canvas#c2d` → `ul#li` of 30 `<a>` project rows, each carrying a HUD data strip: pagination "01/30" (gold, rgb(204,153,51)), split-per-letter title, labeled rows "A COMPLETED <date> / B TYPE / C ROLE / D CLIENT" + two-line description + "EXPLORE" → `div#w` (work-detail container) → `div#a` about overlay (bio, socials, `#a-design` credit → jonway.studio, rights) → `nav#nav` (logo, about/index toggle, email). **No hero, no manifesto section, no footer, no journal: the home IS the index.** About is an overlay state, not a page (same payload, `_A.is.about` flag).

**arocksworld.com**: persistent `canvas#r` + `main#_` on every route. Home = cinematic gate: "PLAY THE FILM" (`/video/introduction`) + "CREATOR | CURATOR | NEW YORK | LOS ANGELES", a permanent dock `a#d` → `/story-extended`, `nav#n` = logo / MENU / CLOSE only. Route map (28 routes): `/index` = full-screen menu holding the entire "footer" content (ABOUT/STORY/PROJECTS/RELEASES in split letters + FOLLOW (IG/YouTube) + LISTEN (Spotify/Mixcloud) + GET IN TOUCH + San Diego and LA addresses); `/story` = bio manifesto + day-timeline HUD (6AM→2AM); `/projects` = "PROJECTS (5)" list; `/releases` = DJ-set index tables ("TRACKS | START TIME | END TIME" with timestamps); `/video/*` player routes; `/story-zoom`.

**in-cognita-corp.com**: single route (`ho` + 404 only), French, entire app in one 134KB inline script over the same `R` micro-framework as the portfolio (identical helper names `R.Lerp`, `R.Fetch`, `R.Raf`). Code tokens ground: numbered home sections (`ho-s2-timer-line-pr`, a timer with progress line; `ho-s4-slider`, `ho-s4-txt-link`), a horizontal-scroll gallery (`hor-i` items, `hor-pag` pagination), CTA component system (`cta-border/icon/txt`), burger menu with contact + legal (`n-menu-contact`, `n-menu-law`), and a multi-step Stripe-backed checkout form (`form-step`, `form-cta-next/prev/submit`). Grid overlay `#g_` drawn over the viewport. No footer.

## Pairwise comparison

### Unseen Studio: identical vs divergent
**Identical across sites:**
- Chaptered/serial storytelling with a HUD selector or counter: Symphony (chapter-selector 1-4), OceanX (chapter-0..6 + fixed chapter menu), Wrapped (12 months), BlueYard (aside "0…5 / 05"), unseen.co (numbered nav 01-04).
- Data-strip/mono-kicker grammar: Wrapped's bracketed codes `[US_01_25]`, BlueYard's `font-mono uppercase` section kickers, Symphony's gold mono labels.
- Entry gates: unseen.co "Enter / Enter without audio", Symphony "Enter experience".
- Close pattern: contact-or-CTA as final section, never a traditional footer. No `<footer>` element on any of the five ("Say hello" / "Start a project with us" / "The END + email" / "Share the Journey" / back-to-top), three of them confirmed against raw HTML (unseen.co, blueyard.com, 2025.unseen.co).
- Same house utility-CSS system on WP builds (`t-sans`, `w-1/1`, `js-*` hooks on unseen.co, Symphony, Wrapped).

**Divergent:** section order/type varies by genre: hub (unseen.co: world hero → index → contact), linear story (Symphony, OceanX, Wrapped), thesis landing (BlueYard: manifesto hero → 4 category sections → index table → team). Scroll axis flips (Wrapped horizontal, rest vertical). Stack splits (WP+utility CSS for their own properties and Symphony vs Vue/Nuxt for BlueYard/OceanX).

### Aristide Benoist: identical vs divergent
**Identical across sites (architecture-level DNA, unusually deep):**
- CSR shell: server body = `#lo` loader only; device-split assets (`/static/css/{d,m}.css`); config object with route map + `psd` design-canvas dimensions; same `R` framework; same "Please enable JavaScript" fallback markup.
- Persistent WebGL canvas as app root (`#gl`, `#r`).
- Ultra-terse id grammar (`#n`, `#a`, `#w`, `#d`, `ho-s*`) and split-per-letter typography on all titles/menus.
- HUD data strips: portfolio "01/30" + COMPLETED/TYPE/ROLE/CLIENT rows; AROCK releases tables + 6AM→2AM story timeline; In Cognita `hor-pag` + s2 timer.
- No footer ever; contact/socials live inside an overlay (portfolio about panel; AROCK index menu; In Cognita burger menu).
- 2-3 item nav maximum.

**Divergent:** the page-level skeleton flexes per project. Portfolio: index-first, zero hero, about-as-overlay; AROCK: film-gate hero, index demoted to a menu route, deep multi-route IA (story/projects/releases/videos); In Cognita: one-page sectioned product site with a payment funnel. Content devices differ (video player routes, DJ tables, Stripe form).

## What repeats

**Unseen Studio: skeleton varies, device grammar repeats.** No two of the five winners share a section order. What is constant, and verifiable in markup, is the device layer: serial numbering with a HUD counter/selector on every site, mono/bracketed data strips, audio- or click-gated entries, custom cursor hooks, and a hard rule of contact-as-close with no `<footer>` element anywhere. They re-skeleton per brief and re-use the same instrument panel.

**Aristide Benoist: one architecture, three skeletons.** His repetition sits a level deeper than sections: all three winners are the same machine (CSR shell + XHR full-DOM payloads + persistent canvas + terse-id grammar + split-letter type + overlay-based nav/contact + no footer + data-strip HUDs), while the visible page skeleton is rebuilt per subject: index-as-homepage portfolio, cinema-gate AROCK, single-page funnel In Cognita. None of his sites contains the standard hero → manifesto → catalog → contact marketing skeleton at all; the portfolio has no hero, AROCK's "footer" is a menu route, In Cognita has one route total.

## Could not verify

- **"The Fabricant"**: no Awwwards evidence linking it to Aristide Benoist surfaced in profile or targeted searches; the attribution is unconfirmed.
- **"EPIC agency"**: the real record is **Epicurrence No.8** (SOTD, 28 Jul 2018 per search-result snippet, secondary); epicurrence.com is unreachable today (empty curl response), so its skeleton could not be inspected; it survives only as `/epicurrence-8` in his portfolio index.
- **Live portfolio = awarded artifact**: the live aristidebenoist.com matches the awarded "Portfolio 2021" (designer credit Jon Way in the DOM equals the Awwwards author listing), but work items dated to Apr 2022 show post-award content updates; bit-identity with the June 2021 jury version can't be proven.
- **In Cognita rendered copy**: the French page copy is generated/obfuscated inside the inline script; sections are grounded on code tokens (`ho-s2`, `ho-s4`, `hor-*`, `form-step`), not rendered text.
- **Hero media internals of OceanX/BlueYard** (canvas vs video behind sections): DOM attributes only (`data-webgl-section` implies WebGL backdrops); no browser execution was used.
- Awwwards dates/scores for In Cognita, AROCK, and Wrapped come from Awwwards pages and search snippets (secondary but official).
