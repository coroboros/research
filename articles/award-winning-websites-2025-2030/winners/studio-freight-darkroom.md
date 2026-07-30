---
title: "Studio Freight / Darkroom Engineering — One Skeleton Repeats, Device Layer Varies"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "studio-skeleton", "page-structure", "studio-freight", "darkroom-engineering", "lenis", "smooth-scroll", "webgl", "typography"]
sources:
  - "https://www.awwwards.com/studiofreight/"
  - "https://www.awwwards.com/sites/scrib3"
  - "https://www.awwwards.com/sites/dragonfly"
  - "https://www.awwwards.com/sites/dragonfly-redux"
  - "https://www.facebook.com/awwwards/posts/todays-sotd-goes-to-studio-freight-for-hyperbolic-hyperbolic-unites-global-compu/1008632694719582/"
  - "https://www.instagram.com/studio.freight/reel/CoLXGIaASmf/"
  - "https://darkroom.engineering"
  - "https://www.lenis.dev"
  - "https://scrib3.co"
  - "https://www.dragonfly.xyz"
  - "https://www.hyperbolic.ai"
  - "https://studiofreight.com"
---

# Studio Freight / Darkroom Engineering — One Skeleton Repeats, Device Layer Varies

The studio now trading as Darkroom Engineering repeats one section skeleton and re-skins it. The Dragonfly pair is the proof: four years apart, on a different framework, a different theme system and different heading semantics, the section sequence is unchanged. What varies between winners is the device layer, one signature apiece. Section-order read of six sites — structural evidence behind the archetypes. Parent reference: [Award-Winning Websites — 2025–2030 Reference](../award-winning-websites-2025-2030.md).

## Sites inspected and evidence

All claims are grounded in HTML fetched via `curl` on 2026-07-17, Wayback snapshots, or Awwwards project pages — each labeled below.

Profile verified at [awwwards.com/studiofreight](https://www.awwwards.com/studiofreight/): **16 Sites of the Day (SOTD), 29 Honorable Mentions (HM), 31 works** (client projects: Lenis, SCRIB3, Dragonfly, Dragonfly Redux, Hyperbolic, Easol, Lunchbox, Death Chef, DeSo, Drive, Evmos, Wyre, Repeat, Dola, Path Robotics, BOOST, Bad Boys…).

| # | Site | Award (verification) | Evidence source |
|---|------|----------------------|-----------------|
| 1 | **SCRIB3** — scrib3.co | SOTD + Dev Award, Apr 29 2024, 7.55/7.69, credited "Studio Freight + darkroom.engineering" ([awwwards.com/sites/scrib3](https://www.awwwards.com/sites/scrib3)) | **Live HTML** (curl). Live = awarded build: footer JSON still carries SF placeholders `"Alan, Studio Freight"` / `alan@studiofreight.com` |
| 2 | **Dragonfly Redux** — www.dragonfly.xyz | Honorable Mention, Jun 19 2026, Studio Freight, URL confirmed ([awwwards.com/sites/dragonfly-redux](https://www.awwwards.com/sites/dragonfly-redux)) | **Live HTML** (curl); Lenis fingerprint x3 in bundle |
| 3 | **Dragonfly (original)** — dragonfly.xyz | SOTD, Sep 19 2022, 7.5, Studio Freight ([awwwards.com/sites/dragonfly](https://www.awwwards.com/sites/dragonfly)) | **SECONDARY: Wayback snapshot 2022-11-15** (curl) |
| 4 | **Lenis** — now www.lenis.dev (redirect from lenis.darkroom.engineering) | SOTD + Dev Award, Feb 2 2023 — from the studio profile + studio's own [Instagram announcement](https://www.instagram.com/studio.freight/reel/CoLXGIaASmf/); the `/sites/lenis` slug 404s | **Live HTML** of current lenis.dev + **SECONDARY: Wayback snapshot Feb 2023 of lenis.studiofreight.com** (the awarded build) |
| 5 | **Hyperbolic** — awarded on hyperbolic.xyz | SOTD May 14 2025 ([Awwwards Facebook announcement](https://www.facebook.com/awwwards/posts/todays-sotd-goes-to-studio-freight-for-hyperbolic-hyperbolic-unites-global-compu/1008632694719582/); slug is `/sites/hyperbolic-site` — note `/sites/hyperbolic` is a *different* project by Handmade Digital, HM 2023) | **SECONDARY: Wayback snapshot May 2025 of hyperbolic.xyz** (title "Hyperbolic – The Open-Access AI Cloud", Lenis fingerprint). Live www.hyperbolic.ai is a **rebuild** — entirely different section-class scheme, zero SF/darkroom/Lenis fingerprints — used only as contrast |
| 6 | **darkroom.engineering** | studio's own current site (context; not itself on the verified award list) | **Live HTML** (curl) |

studiofreight.com is still live but reduced to a legacy gallery: `main.page-index` → h1 "Moving Missions Forward" → one `section.layout-home-gallery` → footer. deathchef.com (SOTD Jan 2024) is **dead** — 114-byte parked page redirecting to `/lander`.

## Per-site skeletons (observed section order, quoted from markup)

**SCRIB3 (live, SOTD 2024)** — dark one-pager, anchored nav:
`header` (+ separate mobile header) → `section.hero` (h1 "WEB3 MARKETING FOR WEB3 BUILDERS", intro "We build + grow crypto brands") → `section.logo-marquee` ("We Work With" + partners numbered `(01)…(08)`) → `section.services#services` → `section.press#press` (press names as giant h2s: Forbes, Blockworks, CNBC…) → `section.cases#cases` (case index: Mantle, Gains, Axelar) → `section.team#team` → `footer` with **contact form** + "2025 SCRIB3 • ALL RIGHTS RESERVED / THE CRYPTO CREATIVE AGENCY".
Devices: **342 `frame_corner` HUD-bracket elements**, 172 marquee refs, parenthesized numbering. Hero is typographic (no SSR canvas). Close = form-in-footer.

**Dragonfly 2022 (archive, SOTD)**:
`header theme-dark` → `#home` hero (h1 "Dragonfly backs your favorite crypto projects", h2 "GLOBAL FROM DAY ONE") → `#about` ("About 关于") → `#research` (essay list + "Follow Along") → `#team` (theme-light) → `#portfolio` (theme-dark) → `#careers` → `footer`.
Devices: bilingual EN/中文 headings, per-section theme inversion, id-anchored one-pager.

**Dragonfly Redux 2026 (live, HM)** — Nuxt/Vue + Sanity:
`header`/`site-nav` → `section.home-hero#hero` (100dvh, giant char-split "Dragonfly" wordmark in NON Natural Grotesk) → `section.home-about#about` ("**01 About**", aria "ETHOS") → `section.home-large-text` ("Global Since Day 1") → `section.home-writing#writing` ("**02 Writing**") → `section.home-team#team` ("**03 Team**") → `section.home-portfolio#portfolio` ("**04 Portfolio**", aria "TENET") → `section.home-careers#careers` ("**05 Careers**") → `section.site-pre-footer` (a **WebGL object** `__webgl` aspect 351/442 + Sections nav + Connect) → `footer.site-footer` (giant glyphs + "Ⓒ Dragonfly Capital 2026").

**Lenis** — awarded Feb 2023 build (archive): `home_hero` (h2 "Smooth Scroll" + "© 2023 Studio Freight" in-hero + h1 "A new smooth scroll library fresh out of the Studio Freight Darkroom") → `home_why` (3 feature asides) → `home_rethink` → `home_solution` → `home_featuring` (theme-light) → `home_in-use` → `footer` (theme-light).
Current lenis.dev (live): hero (SVG-drawn wordmark intro + h1 "The smooth scroll library by darkroom.engineering") → "Why smooth scroll?" (4 asides, near-identical copy: "Create more immersive interfaces", "Make your animations flawless") → narrative sections ("so we built web scrolling" / "Enter Lenis" / "As it should be") → feature-cards → dark footer ("Lenis is Open source, open to features and sponsors" + Become a sponsor + GitHub/X/LinkedIn/Mail). 14 `<video>` demos.

**Hyperbolic May 2025 (archive, awarded build)**:
`hero` (h1 "The Open / Access AI Cloud" + persona cards) → `testimonials` (name list duplicated in markup = **marquee loop**) → `services` ("Hyperbolic makes building and running AI hyper simple") → `why` ("Compute you can count on": Reliable / Scalable / Hardware-agnostic / Secure / Equitable) → `updates` ("Latest updates") → `prefooter` ("This page has ended, but the possibilities remain endless.") → `footer` with **newsletter form**. The live rebuild kept the content strings and rough order (hero → features → who-it's-for → stats → testimonials → use-cases → updates → faq) under a new class scheme.

**darkroom.engineering (live studio site)** — the most device-dense:
DOM order is `header` (fixed) → **`footer.real-footer` placed BEFORE `<main>` and `sticky` — a reveal-under inverted footer** ("Let's talk →", nav, **OSS index**: satus, lenis, hamo, tempus, elastica, aniso, cc-settings, socials, giant "Where Things Get Developed" wordmark + dictionary device "[ Darkroom ], noun — A Lightproof Room for Developing Photographs / A Studio Engineering Creativity into Reality") → `main#home`: hero (same wordmark h1 + definition + manifesto) → **`section h-[300vh]` scroll-pinned showcase** ("Looped / Ibicash / Prosupps" + self-aware caption "A Small Sample, Just Three Builds We Liked…") → "What Clients Say" (h2 duplicated = split-text animation) → "Tools We Build and Use. Now Yours Too." → manifesto statement → **index tables** (Services / Clients / Technologies / Awards-Features) → **"Activity Log"** (dated h3 entries, 2025/03 → 2026/02 — a literal log/journal slot) → bottom `sticky bottom-0` bar footer ("Become an Open Source Sponsor").

## Pairwise: identical vs changed

**Dragonfly 2022 → Dragonfly Redux 2026 (same client, both honored — the cleanest test):**
- IDENTICAL: section sequence **hero → About → Research/Writing → Team → Portfolio → Careers → footer** is unchanged after 4 years; one-page anchored nav; giant typographic hero wordmark; even the line survives ("GLOBAL FROM DAY ONE" h2 → "Global Since Day 1" large-text interstitial).
- CHANGED: bilingual CN headings dropped; **numbered indices 01–05 added**; per-section light/dark theme flips → single theme + WebGL totem in a new pre-footer; semantic h1–h3 → styled divs with aria-labels; React-style build → Nuxt/Vue + Sanity.

**SCRIB3 2024 vs Hyperbolic 2025 (consecutive SOTD client one-pagers):**
- IDENTICAL slots: typographic mega-claim hero → **social-proof marquee band** (partner logo marquee vs looped testimonial names) → services → proof section → **updates/log slot** (press+cases vs "Latest updates") → **footer containing a form** (contact vs newsletter) + all-caps legal/persona line.
- CHANGED: SCRIB3's HUD frame-corners (342) and press-as-typography have no Hyperbolic counterpart; Hyperbolic adds the jokey prefooter sign-off and why-adjective grid; team section only on SCRIB3.

**Lenis 2023 → lenis.dev 2026 (same product across the rebrand):**
- IDENTICAL: hero-manifesto → why-features → narrative pivot ("rethink" / "so we built web scrolling") → solution → showcase → CTA footer; feature copy carried over nearly verbatim.
- CHANGED: credit SF → darkroom, 3 → 4 features, SVG wordmark intro, sponsor-CTA close.

**Studio site vs client sites:** darkroom.engineering runs the same macro order as the client work but owns three devices the client sites don't use: the inverted sticky footer, the index tables, and the dated Activity Log.

## What repeats

The studio repeats one skeleton and re-skins it. Most inspected sites open with a typographic hero and close on a form-or-CTA footer; SCRIB3 and Hyperbolic share 5–6 of 7 slots by role, and the Dragonfly pair preserves its section order, slot for slot, across four years on a rebuilt stack. The recurring slots are a typographic wordmark/claim hero (never image-led), a social-proof or marquee band placed high, an indexed catalog slot (cases/portfolio/work), a log/updates/writing slot, and a form-or-CTA footer bearing an all-caps legal line and a giant repeated wordmark — with Lenis smooth scroll underneath (they author it; fingerprints found in Dragonfly Redux, Hyperbolic 2025, lenis.dev, darkroom.engineering, legacy studiofreight.com). What varies between winners is the *device layer*, one signature per site — SCRIB3: HUD frame corners + parenthesized numbering; Hyperbolic: looped testimonial marquee + prefooter sign-off; Dragonfly Redux: numbered indices + WebGL totem; darkroom: inverted sticky footer + Activity Log — not the slot order.

## Could not verify

- **studiofreight.com's own SOTD** — unconfirmed. The verified profile award list contains client work only; no Awwwards evidence surfaced that studiofreight.com itself won SOTD. "Sofar" and "Dial-up" are also absent from the profile; "Easol" (SOTD Mar 1 2021) and "Lunchbox" (SOTD Nov 5 2021) are real but their domains presumably no longer carry SF builds — not inspected.
- **Death Chef** (SOTD Jan 3 2024) — deathchef.com is parked (JS redirect to `/lander`); would need archive, dropped in favor of stronger candidates.
- **Live hyperbolic.ai** is not the awarded build (rebuilt: different class scheme, no SF/Lenis fingerprints) — all Hyperbolic claims rest on the May 2025 Wayback snapshot, marked secondary.
- **`/sites/lenis` returns 404**, so Lenis's exact award date comes from the studio profile page and the studio's Instagram announcement, not the project page.
- **Runtime behavior** (mounted WebGL canvases, scroll scrubbing, hover states) — no browser execution was used; claims like "300vh scroll-pinned showcase" and "char-split hero" are inferred from SSR markup and CSS (`h-[300vh] sticky`, `.char{contain:layout style}`), not from lived interaction. No `<canvas>` exists in any SSR payload; WebGL is client-mounted.
- Wayback sources used: dragonfly.xyz 2022-11-15, lenis.studiofreight.com 2023-02, hyperbolic.xyz 2025-05.
