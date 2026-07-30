---
title: "Jury Evidence — Criteria, Thresholds, Weight, and the Template Rule"
date: "2026-07-30"
author: "Coroboros"
tags: ["awwwards", "fwa", "cssda", "jury-criteria", "performance-budget", "core-web-vitals", "anti-template"]
sources:
  - "https://www.awwwards.com/about-evaluation/"
  - "https://www.awwwards.com/faqs/"
  - "https://thefwa.com"
  - "https://www.cssdesignawards.com"
  - "https://www.awwwards.com/become-an-awwwards-jury-member-in-2026.html"
  - "https://www.awwwards.com/about-young-jury/"
  - "https://www.awwwards.com/honors/about"
  - "https://www.awwwards.com/sites/lando-norris"
  - "https://www.awwwards.com/igloo-inc-case-study.html"
  - "https://www.awwwards.com/rob-ford-interview.html"
  - "https://www.awwwards.com/case-study-reinventing-locomotive-r.html"
  - "https://www.webgpu.com/showcase/messenger/"
  - "https://www.utsubo.com/blog/award-winning-website-design-guide"
  - "https://www.hontran.dev/blog/best-award-winning-websites-2026"
  - "https://greenspector.com/en/analysis_sites_nominated_mobile_excellence_awwwards/"
  - "https://web.dev/articles/vitals"
  - "https://14islands.com/blog/progressive-enhancement-with-webgl-and-react"
  - "https://tympanus.net/codrops/2026/03/06/obys-the-small-studio-designing-big-digital-narratives/"
  - "https://conference.awwwards.com/valencia-developers/speakers/alex-trost"
  - "https://borism.medium.com/on-the-visual-weariness-of-the-web-8af1c969ce73"
  - "https://dl.acm.org/doi/abs/10.1145/3411764.3445156"
  - "https://theconversation.com/yes-websites-really-are-starting-to-look-more-similar-136484"
  - "https://daringfireball.net/linked/2015/08/26/all-websites-look-the-same"
  - "https://zeldman.com/2015/09/10/all-websites-look-the-same/"
  - "https://dribbble.com/shots/23789018-Awwwards-Studio-of-The-Year-2023"
  - "https://www.awwwards.com/inspiration/the-homogenization-of-web-design-is-the-reason-why-every-website-looks-the-same"
  - "https://www.nngroup.com/articles/scrolljacking-101/"
  - "https://www.wearetenet.com/thoughts/design-awards-vs-real-ux-results"
---

# Jury Evidence — Criteria, Thresholds, Weight, and the Template Rule

Awwwards publishes four weighted criteria and defines none of them, no jury publishes a byte cap, and the only template rule is an eligibility bar at intake rather than a scoring penalty. Scope: published criteria and thresholds for Awwwards, FWA and CSSDA, the byte weights winners actually ship, and the juror commentary on record.

**Awwwards published criteria** ([about-evaluation](https://www.awwwards.com/about-evaluation/)), verbatim: "Design: 40% points / Usability: 30% points / Creativity: 20% points / Content: 10% points." Process, verbatim: "Once approved, sites are sent to a minimum of 18 jury members, and the 3 jury scores furthest from the average are automatically eliminated by our system. The voting process lasts 5 days." Thresholds, verbatim: "HMs are awarded to sites that are scored 6.5 or more from the jury"; Developer Award "if the site is scored higher than a 7." **FWA:** 500+ judges, live daily voting on "technical excellence, creative innovation, user engagement"; rewards experimental work more aggressively. **CSSDA:** UI / UX / Innovation / Content.

**Threshold conflict, unresolved — the two readings are not averaged here.** One reading of the evaluation page reports a required average **≥ 8.0** for Site of the Day (SOTD); a verbatim pull of the same page carries only the 6.5 Honorable Mention (HM) figure and the >7 Developer figure. The parent article states "Site of the Day typically `7.5+`" ([`../award-winning-websites-2025-2030.md`](../award-winning-websites-2025-2030.md)). Measured SOTD scores across this corpus run **7.21, 7.3, 7.34, 7.47, 7.53, 7.55, 7.62, 7.9, 8.18** — which contradicts a hard ≥8.0 gate and sits with the 7.5-ish reading. Two further cautions about the threshold: the parent article never contrasts 7.5 against 6.5 directly (it anchors thresholds in one sentence and contrasts `6–7` against `8+` in another, so a "7.5 vs 6.5" discriminator is interpolation across two claims), and no source in this corpus supports a seconds-to-judge or first-impression-window premise — what is documented is instant recognition of template and AI layouts, plus "Judges check mobile first."

## Performance vs quality

**Outcome.** No jury publishes a total-byte or page-weight criterion. Performance is scored, but only as **perceived arrival speed** (inside Usability, 30%) and **optimization quality** (the Awwwards Dev-Award `WPO` sub-score, /10) — never against a fixed MB ceiling. A measured 2025 Awwwards Developer-Award winner (Messenger) ships **5.7 MB on initial load**; a heavy 3D Site of the Day (Lando Norris) scored **Usability 7.9 and WPO 7.60** while shipping a 3D helmet, Rive, and film assets. A "total weight < 3 MB" hard threshold has **no jury source** — the number appears only in an uncited agency-blog table. Downgrading a signature texture to honour it is a self-inflicted loss.

**Measurement limits.** Every transfer size below is **sourced from published reads as of 2026-07-16, not independently measured** — these winners' edges serve nothing to a direct non-browser fetch. Method is stated per number. The conclusion depends only on whether a byte cap exists in published criteria and whether winners exceed 3 MB.

**Where performance actually enters.** The Awwwards evaluation page has **zero** mention of weight, bytes, MB, load time, or WPO. It enters two levels down: **Usability** (perceived speed and smoothness) and a per-winner **Dev-Award technical breakdown** scored /10 — Semantics/SEO, Animations/Transitions, Accessibility, **WPO (Web Performance Optimization)**, Responsive, Markup. WPO scores optimization quality, with no published threshold. FWA and CSSDA carry no weight criterion either.

### What winners ship, 2024–2026

| Site | Award | Byte evidence | Method / source |
|---|---|---|---|
| **Messenger** (abeto) | Developer Award; the **Developer Site of the Year (SOTY) 2025** title is contested — [`../archetypes/immersive-cinematic.md`](../archetypes/immersive-cinematic.md) records SOTD 10 Nov 2025 + Developer Award 8.21 at `messenger.abeto.co` | **5.7 MB initial · 17.5 MB total** | dev network-tab read — webgpu.com/showcase/messenger + Medium (Talreja) + LinkedIn (Douma) |
| **Igloo Inc** (Abeto) | **SOTY 2024 + Dev Award** | none published; entire UI in WebGL | awwwards.com/igloo-inc-case-study |
| **Lando Norris** (OFF+BRAND) | **SOTD 8.18, 2025-11-17** | none; jury breakdown below | awwwards.com/sites/lando-norris |
| **Cartier W&W 2024** (Immersive Garden) | SOTD 7.53 + FWA + CSSDA | none; six 3D scenes | awwwards + immersive-g.com |
| **OceanX 2025** (Unseen + Propagande) | SOTD | none; cinematic WebGL | awwwards.com/sites/oceanx-2025 |
| **Symphony of Vines** (Unseen) | SOTD 7.43 + FWA + CSSDA | none; Three.js + C4D | awwwards.com/sites/the-symphony-of-vines |

The Cartier row's edition year is unresolved: the same 7.53 SOTD is dated 25 May 2026 in [`../foundations/motion-mechanics.md`](../foundations/motion-mechanics.md), while [`../archetypes/corporate-luxury.md`](../archetypes/corporate-luxury.md) records a distinct Cartier Watches & Wonders 2025 at 7.64 (SOTD 18 Aug 2025). The row carries no byte evidence either way.

**Lando Norris is the load-bearing artifact.** Public winner page: SOTD Design 8.12 / Usability **7.9** / Creativity 8.71 / Content 8.18 → **8.18**; Dev Award 7.58 with **WPO 7.60**, Animations 8.60, Accessibility 7.00. A heavy 3D/WebGL/Rive/film site scored 7.9 usability and 7.60 WPO. Weight did not block it; Creativity led.

### How winners reconcile weight

- **Two-phase load + background streaming** — Igloo loads textures and compiles shaders "both during the initial load and in the background."
- **Compression to sub-image sizes** — Igloo's custom VDB→browser exporter compressed volume data "smaller than a typical website image."
- **Custom LOD + WASM glyphs** — Messenger swaps detail by distance and renders text via WebAssembly on the GPU; this is why a dense game holds 5.7 MB initial.
- **Tiered progressive enhancement** — 14islands ship no-JS → JS-no-WebGL → full-WebGL over a shared react-three-fiber canvas.
- **Device-power gating + adaptive quality by live fps** — three-tier matrix desktop-GPU / mobile-flagship / mobile-mid (digitalstrategyforce.com); Draco + LOD standard in Three.js r160+.
- **Preloader bound to real load** — WebGL apps preload and pre-compile textures before reveal because first GPU upload janks (threejsresources.com).

### Documented weight criticism targets jank, not bytes

Greenspector measured 10 Awwwards **Mobile Excellence nominees**: Betterup.com 400+ requests, **>12 MB** full-scroll ("too many third-party scripts"); Datagrid.co.jp loading "never really ends," "absolutely not usable"; Webflow.com **2 MB initial**, 57 domains. Heavy sites (12 MB) still get nominated — no byte gate — and the criticism that bites is destroyed usability, i.e. arrival and jank. Caveat: Greenspector is a sustainability lab, **not** an Awwwards juror. No case was found of an Awwwards/FWA/CSSDA juror penalising an otherwise-strong site for byte weight itself.

**Source of the "< 3 MB" figure.** It appears only in utsubo.com's "Judging Criteria Decoded" post, inside a self-made uncited table (LCP <1.5s / CLS <0.05 / INP <100ms / weight <3 MB), attributed to no jury. Awwwards carries none of these numbers. Counter-current: Awwwards also awards minimal, lightweight sites (SOTD "Lightweight"; Minimal collection). A 3D world and a 200 KB minimal site can both win.

### Limits of the byte evidence

- **Messenger 5.7 MB initial / 17.5 MB total** — single-lineage: every citation traces to one person reading the network tab, and "initial" versus "total" are that author's definitions. Stands as a counter-example to a universal cap, since the favourable 5.7 MB figure already exceeds 3 MB and the technical jury that saw that network tab gave the site the Developer award.
- **Betterup >12 MB** — measured full-scroll, on a nominee rather than a winner, by a non-jury lab: supporting evidence for "heavy sites get nominated," nothing more.
- **Igloo, Cartier, OceanX, Symphony as heavy-byte winners** — unsupported: zero measured bytes, "heavy WebGL" inferred from scope, and a well-compressed WebGL scene can sit under 3 MB initial (Igloo compressed volume data "smaller than a typical website image"). Messenger is the only byte-measured winner.
- **Messenger's Dev award proves the design jury tolerates weight** — false: a Dev award rewards technical craft, so rewarding a 5.7 MB site there arguably rewards the optimization. Jury tolerance of weight rests only on Lando's SOTD-track Usability 7.9 on a heavy 3D site.
- **No byte mention on the evaluation page means weight is not judged** — false: absence of a cap is not irrelevance, and WPO is scored (Lando 7.60). Weight is judged as optimization quality plus perceived speed, never as a fixed ceiling.
- **A juror comment marking a strong site down for weight** — searched, none found: absence of evidence, not evidence of absence.
- **Five winners all ship > 3 MB** — false: only Messenger is measured.

### Where the record puts the threshold

No published criterion caps total bytes. What the evidence supports as the operative threshold is arrival speed, layout stability, responsiveness, and sustained frame rate — measured on the target device tier and a throttled 4G connection:

1. LCP ≤ 2.5 s, CLS < 0.1, INP < 200 ms — Google's official "good" Core Web Vitals (web.dev / Google Search Central, 2025-12).
2. Sustained ≥ 55 fps through the signature scroll, motion, or scrub; no frame over 50 ms once past the loader.
3. First meaningful paint immediate (poster or static-first) or covered by a designed loader whose progress is bound to real asset bytes rather than a timer; no uncovered blank canvas beyond 1 s.

Only 1 carries an official source. The 55 fps, 50 ms, and 1 s figures in 2 and 3 have no jury or platform source — they are this report's floor, derived from what the winners' preloader and frame-rate techniques are built to protect.

Streamed weight is uncapped; what the winners' own techniques control is how it arrives:

4. Only bytes needed to reach LCP and first interaction sit on the critical path; heavier assets stream behind the loader or after first paint.
5. Device-tiered quality is required above the critical-path budget — at minimum a desktop-discrete-GPU / mobile-mid split, quality driven by live fps.
6. Current codecs before any resolution reduction: Draco or meshopt geometry, KTX2/Basis textures, AVIF/WebP images, MP4 + WebM video.
7. Initial-interactive transfer as small as the signature allows. Single-digit MB is the observed floor among measured winners (Messenger: 5.7 MB initial); exceeding it warrants review, not automatic failure.
8. Signature-asset fidelity — hero texture resolution, model detail, film grade — is not traded for a byte number. Weight is solved by streaming, tiering, and compression; a visibly soft hero shipped to honour a weight budget indicates the budget was the wrong threshold.

**How each is measured** (target device tier, throttled network): Lighthouse or field CrUX for 1; an fps trace across the signature interaction for 2; the first second on cold cache for 3; critical path against total transfer in the network panel for 4 and 7; a mobile-mid tier holding fps for 5; asset codecs in the network panel for 6; an A/B of the signature asset at shipped versus one step higher fidelity for 8.

## The template penalty

**Key negative finding on the primary source:** the evaluation page contains **no definition of "Creativity" and no wording about originality, novelty, or templates**. The January 2019 Wayback snapshot says the same — the four criteria are only named ("we've created an evaluation system based on 4 criteria: Design, Usability, Creativity and Content"), never defined. Awwwards has never published what Creativity means operationally. Jury scores are private: "Jury votes are only revealed to SOTD winners" (2019 snapshot).

The jury-recruitment page says only that jurors will be "evaluating the best work from top designers and agencies worldwide, setting standards for quality" — no anti-template or anti-trend instruction. The Young Jury page frames its mission as helping Awwwards "stay at the forefront of new concepts and approaches" — the closest official text to a novelty mandate, and it is weak.

**Template policy** ([FAQs](https://www.awwwards.com/faqs/)), verbatim: **"We do not accept websites built using pre-made templates."** And: **"However, we do accept demo websites showcasing templates for future sale, as long as the design and development were entirely created by the individual, team, or studio submitting the work."** Templates are an **eligibility rule at intake, not a scoring penalty** — original template demos compete normally, which is how theme demos have won SOTD. Honorable Mention is purely a score tier (≥6.5), not a template category. The newer [Awwwards Honors](https://www.awwwards.com/honors/about) program adds user-voted categories (Typography, **No-code**, E-commerce, Product, Portfolio, Business & Services) — an institutional lane for tool-built work; its page says nothing about templates. The claim that Awwwards sells templates in a marketplace could **not** be verified — no policy text found.

### Jury-member commentary

**No on-record quote from a named Awwwards juror saying they penalize template-feel or "sites that all look the same" was found.** What exists is one step removed.

- **Hon Tran** — self-identified "creative developer, Awwwards jury member, and two-time Awwwards Independent of the Year nominee", verbatim: **"Award-winners aren't decorated templates; every type choice, color, and layout grid serves a single idea."** Also: "The gap between a 6.5 and a 9 almost always lives in three places at once: Art direction, Directed motion, Performance" and "jurors test on real devices." The source is a personal blog; the jury status is self-claimed and independently unconfirmed.
- **Rob Ford (FWA founder)**, interviewed on Awwwards: judging "happens on gut instincts and experience, not after spending hours going through a 100 point score sheet"; he praises work "ripping up the latest trends and setting the bar at a time when people were moaning how web design was all too samey"; "the only chance we have of changing the direction of web design lies in the hands of individuals and their personal projects and experimental works." The FWA founder registers "samey" as a complaint — as commentary on the web at large, not as a stated scoring rule.
- **Counter-current from the institution itself.** Awwwards curates the tropes as teachable inspiration — collections for text marquee effects, preloader animations, WebGL — and its conference hosts Alex Trost's "The Linear Look Decoded: Secrets to Sleek and Stylish Websites", whose description teaches reuse of the look ("tricks and techniques… use them in your own projects"), with zero framing of homogenization as a problem. Awwwards republished the Medium piece "The homogenization of web design is the reason why every website looks the same" as *inspiration* content.

### Homogenization critiques, and who they target

- **Dave Ellis**, "All Websites Look The Same" (novolume.co.uk, 2015) — the ur-critique of the hero-image/big-text skeleton; linked by Daring Fireball and Zeldman.
- **Boris Müller** (Prof. of Interaction Design, FH Potsdam), "Why Do All Websites Look the Same?" (Medium, 2018) — "generic fonts, no layouts to speak of… an absence of expressive visual language."
- **Sam Goree, Bardia Doosti, David Crandall, Norman Makoto Su**, "Investigating the Homogenization of Web Design: A Mixed-Methods Approach" (CHI 2021) — quantitative: average layout differences declined significantly across ~10k sites (summaries report roughly 30–43% depending on period and dataset).

All three target the **mainstream web** (Bootstrap-era sameness), not award sites. Award-specific critique is thinner and lower-authority: **Shantanu Pandey**, "The Reality of Design Awards No One Wants to Admit" (Tenet, Apr 2026) — awards "prioritize 'visual innovation' over basic usability"; judges "review a highly polished 'submission package'". **NN/g's "Scrolljacking 101"** empirically indicts the signature award-site scroll pattern (disorientation, users reading it as a bug); wpdean.com's "Your Award-Winning Website Is Unusable" exists but was not fetched in detail. **No authoritative named essay specifically aimed at the "Awwwards aesthetic"** (huge type / preloader / marquee / WebGL formula) was found — that critique lives in community threads and SEO-adjacent pieces.

**Jocelyn Lecamus** (CEO, Utsubo), "Award-Winning Web Design: Judging Criteria Decoded" (Mar 2026), documents the formula *from the winners' side*: "Every recent SOTD winner we've studied shares these characteristics: One signature moment… Performance under pressure… Real content… Cross-device parity… Scroll as narrative." That is evidence a shared winning skeleton **exists and wins**, not that it is penalized. The same post claims judges "recognize WordPress themes and Webflow templates instantly."

### The opposite direction — signatures rewarded

Awwwards' **annual awards structurally reward consistent bodies of work**: Studio / Agency / Independent of the Year. **Obys** won Awwwards Studio of the Year 2023 plus 4× CSSDA Studio of the Year (2020, 2021, 2023, 2024) with a recognizable typography-driven signature; in Codrops' March 2026 profile they say verbatim: "If there is one thing that connects all our projects, it is narrative" and "Structure is emotional. It creates rhythm, tension, and balance." **Locomotive** claims "more than 100 awards since 2018 — including five consecutive Awwwards Agency of the Year" (seen in search summaries; no canonical URL pinned — plausible but unverified). Awwwards' own Locomotive case study contains **no jury quotes** (verified). **Zhenya Rynzhuk**: 2× Independent of the Year, Awwwards juror since 2018, strongly recognizable art direction — no jury praise quote about her signature found. **No verbatim jury comment praising a studio's recognizable repeated structure was found.** The evidence is institutional, not quoted.

### Repeating a page anatomy across a studio's own sites

Not a documented penalty, but a real scoring risk via an undefined criterion. (a) No Awwwards text penalizes structural repetition — the only hard rule bans *pre-made* templates, which a studio's own reused skeleton does not violate. (b) Scoring is per-site by ≥18 jurors with no published cross-submission comparison, and Creativity (20%) has no published definition, so "template-feel" lives entirely in juror gut judgment — exactly where practitioner consensus says recognizable skeletons get read as ceiling-capped work. (c) The opposite force is equally real: SOTD winners demonstrably share a recurring structural formula, and the studios with the most rigid signatures (Obys, Locomotive) win the top annual honors — but their rewarded signature is art direction and narrative, with each site still delivering a bespoke signature moment rather than a visibly reused section order. **Unverifiable:** whether jurors ever see two sites from the same studio, any internal jury guidance, and actual score effects.

Net: reusing six of seven structural slots across sites is neutral by rule and hazardous by gut — safe at the level jurors call signature (voice, type, motion grammar), risky at the level they call template (slot-for-slot page anatomy). The corpus-side counterpart is [`studio-variance.md`](./studio-variance.md).
