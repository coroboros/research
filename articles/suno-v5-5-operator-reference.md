---
title: "Suno v5.5 — Operator Reference"
date: "2026-05-09"
author: "Coroboros"
tags: ["ai-engineering", "ai-music", "suno", "music-generation", "generative-music", "prompt-engineering", "voice-cloning", "custom-models", "audio-ai", "creative-tools", "copyright", "ai-licensing", "wmg-settlement", "riaa-litigation", "model-deprecation", "api-reverse-engineering"]
sources:
  - "https://suno.com/blog/v5-5"
  - "https://help.suno.com/en/articles/11362305"
  - "https://help.suno.com/en/articles/11362369"
  - "https://help.suno.com/en/articles/11362433"
  - "https://help.suno.com/en/articles/11362497"
  - "https://help.suno.com/en/articles/11362561"
  - "https://help.suno.com/en/articles/6141377"
  - "https://help.suno.com/en/articles/10625089"
  - "https://help.suno.com/en/articles/2409473"
  - "https://help.suno.com/en/articles/5782977"
  - "https://x.com/suno_ai_/status/1836920791981568094"
  - "https://x.com/suno/status/2042674007007216055"
  - "https://kie.ai"
  - "https://sunoapi.org"
  - "https://www.cometapi.com"
  - "gcui-art/suno-api"
---

# Suno v5.5 — Operator Reference

The mainstream consensus is that Suno v5.5 is a personalization layer bolted onto v5, not a new audio engine — and the prompting surface is where most of the unrealized control lives. Treat the Style of Music field, the Lyrics field, and the Creative Sliders as three independent control planes. Tracks improve when each plane carries its own job and stops carrying the others.

Released March 26, 2026. Successor to v5 (chirp-crow). Internal model identifier `V5_5`. Pro and Premier tiers; free tier remains on v4.5-all. Surfaces: Web, iOS, Android, Suno Studio (Premier).

## TL;DR

- v5.5 ships voice cloning (Voices), per-user fine-tunes (Custom Models, up to three per Pro/Premier seat), and a passive preference layer (My Taste). Prompt syntax is unchanged from v5; the Style Stack still drives output.
- The 1,000-character Style of Music field carries five descriptor classes — genre, era, mood, instruments, vocal direction — with a sweet spot of four to seven tags. Less yields generic; more produces conflict.
- Commercial-rights chain remains broken at the copyright-vesting layer, the WMG settlement (November 25, 2025) commits Suno to deprecating current models when licensed successors ship later in 2026, and there is no public API. Export WAV now.

## Key Findings

1. v5.5 is additive over v5. Prompts that worked in v5 work in v5.5 — often better — because the model is more responsive to subtle descriptors.
2. The Style of Music field is read as an ordered, weighted tag list. The first two to three tags dominate.
3. The Lyrics field accepts up to 5,000 characters. Bracket metatags inside it control structure; parenthetical cues control delivery.
4. Negative prompting works in two places: inline `no X` inside the Style field, and the Exclude Styles toggle in Advanced Create > More Options. The toggle is more reliable; both are exposed via `negativeTags` in third-party schemas.
5. Three Creative Sliders — Weirdness, Style Influence, Audio Influence — map to API floats `weirdnessConstraint`, `styleWeight`, `audioWeight`, range 0.00–1.00, step 0.01.
6. Voices accept 15 seconds to 4 minutes of audio; Suno selects the best 2 minutes and runs voice-print verification against a spoken phrase.
7. Custom Models require six tracks minimum, train in roughly 2–5 minutes, and degrade with stylistically scattered training material.
8. Commercial rights vest only for songs created during a paid subscription. Free-tier output is non-commercial and non-retroactive. Suno does not represent that copyright will vest in any output.
9. RIAA litigation continues against Suno in Massachusetts. GEMA judgment in Munich is scheduled for June 12, 2026. WMG settled and partnered November 25, 2025.
10. There is no official public API. Every "Suno API" — kie.ai, sunoapi.org, CometAPI, gcui-art/suno-api — is a reverse-engineered wrapper with vendor shutdown precedent (PiAPI's Suno V5 line was discontinued).

## 1. What v5.5 Is

Suno v5.5 launched March 26, 2026. The release framing from Suno's own blog: "v5.5 is our deepest expression of that belief so far, a model that doesn't just help create music, but fully reflects the person making it." Three personalization vectors ship alongside the model:

| Feature | Tier | Function | Hard limit |
|---|---|---|---|
| Voices | Pro, Premier | Vocal-print attached to generations | 15 s–4 min input; 2 min selected |
| Custom Models | Pro, Premier | LoRA-style fine-tune on user-owned tracks | 6 tracks minimum; 3 models per account |
| My Taste | All | Passive preference profile feeding the Magic Wand | Magic Wand button only |

v5.5 inherits v5's audio engine: 44.1 kHz stereo, up to 8 minutes per generation, lyrics-aware vocal synthesis, and improved low-frequency separation. Native output is MP3 on free, MP3 and WAV on Pro and Premier. Stem export to 12 time-aligned WAVs is paid-tier only.

The Personas button in the Create menu was renamed Voices. Existing Style Personas remain inside the Voices tab.

## 2. Flagship Features

### 2.1 Voices

Workflow: select Voice in Create, choose existing Voice or Create Voice, supply audio (record live, upload, or pick from a Suno song in the user's library). Suno asks the speaker to read a randomly displayed verification phrase aloud. The system compares the spoken phrase to the uploaded singing audio. Mismatches block the registration. Voices are private to the registering account.

*Consent and training data.* Suno's verification gate prevents registering somebody else's voice through the official UI. It does not prevent registering a voice already cloned by an external tool, then reading the verification phrase in the cloner. Registered Voices are private but inputs may still be processed in ways governed by Suno's evolving terms; treat the verification step as fraud control, not provenance.

### 2.2 Custom Models

Open the model dropdown in Create, select Create Custom Model, upload at least six tracks the user owns rights to, name the model. Training takes 2–5 minutes. The model lands in the model picker. Mixed-genre training material produces unstable output; single-lane catalogs (e.g., orchestral only, future bass only) produce coherent personalization.

### 2.3 My Taste

Default-on. Influences the Magic Wand suggestions in the Style box and biases generation defaults when prompts are underspecified. Does not override an explicit Style field. Disable from the avatar menu > My Taste.

## 3. Modes and Surfaces

| Mode | Inputs | When to use |
|---|---|---|
| Simple | One free-text box | Discovery, single-shot ideas |
| Custom | Style of Music, Lyrics, Title, Sliders, Exclude Styles | Production work |
| Studio | Generative Audio Workstation, stems, MIDI | Editing, finishing |
| Studio 1.2 | Warp Markers, Remove FX, Alternates, time signatures 2/4–12/8 | Post-generation correction |

Custom Mode is required for serious work. Simple Mode strips field separation and suppresses Sliders.

## 4. Field Limits

| Field | v5.5 limit | Notes |
|---|---|---|
| Style of Music | 1,000 characters | Front-load — first 2–3 tags dominate |
| Lyrics | 5,000 characters | Bracket metatags + parenthetical cues |
| Title | 100 characters | No effect on audio |
| Simple Mode prompt | 500 characters | Single-field equivalent |
| Voice input audio | 15 s–4 min | Best 2 min selected |
| Custom Model training | ≥6 tracks | Stylistic consistency required |
| Generation length | up to 8 min | Extend chains beyond |
| Audio upload | up to 30 min (Pro/Premier) | 8 min on free |

---

# 5. The Prompting Spine

This is the spine. Everything else is scaffolding. The prompting layer is where v5.5 is won or lost. The model is more obedient than v5; that obedience punishes vague prompts harder.

## 5.1 The Style Stack — Anatomy of the Style of Music Field

A Style of Music prompt is an ordered, weighted tag list. Fill it with four to seven descriptors across five classes. The verbatim formula from Suno's April 11, 2026 X post (Tier 1):

> "Fill the stylebox with 4–7 descriptors: Genre + era + mood + instruments + vocal direction. That's the foundation. Less description = more generic."

| Class | Examples | Weight |
|---|---|---|
| Genre | Indie folk, melodic trap, dark ambient | Load-bearing |
| Era / vibe | 90's warmth, 80s gated, 2010s indie | High |
| Mood | Nostalgic, brooding, euphoric | Medium |
| Instruments | Acoustic guitar, 808 sub, Rhodes | Medium |
| Vocal direction | Soft male vocal, breathy soprano, autotuned melodic rap | High when no Voice attached |

### 5.1.1 Order matters

Place genre first. Era and mood second. Instruments third. Vocal direction last unless vocal is the identity of the track, in which case promote it to second. Suno weights early tokens more than late tokens.

### 5.1.2 Character budget

The 1,000-character limit is generous, but density beats verbosity. Recommended allocation:

| Bucket | Characters | Tags |
|---|---|---|
| Genre stack | 30–80 | One or two |
| Era cue | 20–40 | One |
| Mood | 20–60 | One or two |
| Instruments | 60–150 | Two or three hero instruments |
| Vocal direction | 40–120 | One vocal block |
| Production texture | 60–150 | Two or three texture tags |
| BPM / key | 10–30 | Optional |
| Inline negatives | 40–100 | Optional, place last |

Total: 280–730 characters. The remaining headroom is reserve, not a target.

### 5.1.3 Filled stacks across genres

```text
Cinematic:
Dark cinematic orchestral, 2010s trailer scoring, foreboding,
deep strings, timpani rolls, brass stabs, no vocals, D minor, 85 BPM

Melodic techno:
Melodic techno, 2020s European club, hypnotic and brooding,
analog arp, sub bass, minimal kick, sparse female vocal hook, 124 BPM

Hip-hop (melodic trap):
Melodic trap, 2020s atmospheric, dark moody,
deep sub 808s, glitchy hi-hat rolls, pitched vocal chops,
autotuned melodic male rap, reverb-drenched ad-libs, 145 BPM half-time

Alt rock:
Alt rock, late 90s post-grunge, brooding,
distorted guitars, driving drums, raspy male vocal,
tape warmth, 96 BPM

Ambient drone:
Dark ambient drone, 2010s isolationist, glacial and unsettling,
evolving pads, tape hiss, no percussion, no vocals, 50 BPM

Vocal-forward indie pop:
Indie pop, 2010s bedroom, intimate and bittersweet,
fingerpicked acoustic guitar, soft female vocal,
slight lo-fi warmth, 92 BPM

Experimental dark (ritual industrial post-punk):
Ritual industrial post-punk, late 80s 4AD, ominous,
metallic percussion, chorused bass, baritone male incantation,
plate reverb, 102 BPM

Lo-fi hip-hop / chillhop:
Lo-fi hip-hop, 2010s bedroom-producer aesthetic, melancholic,
dusty jazzy piano sample, brushed drums, vinyl crackle,
no vocals, 78 BPM
```

### 5.1.4 Side-by-side: 1 / 6 / 12 descriptors

```text
1 descriptor (generic):
indie pop

6 descriptors (working):
indie pop, 2010s bedroom, nostalgic, fingerpicked acoustic,
soft male vocal, lo-fi tape warmth, 95 BPM

12 descriptors (overstuffed; conflicts):
indie pop, dream pop, shoegaze, bedroom, lo-fi, hi-fi polished,
nostalgic, euphoric, dark, fingerpicked acoustic, jangly Rickenbacker,
synthwave pads, 808 trap drums, soft male vocal, belting female vocal,
95 BPM, 140 BPM
```

The 12-tag version forces Suno to average across "lo-fi" plus "hi-fi polished" and across two BPMs and two vocal genders. The model collapses to a moody average — the output the prompt did not ask for.

### 5.1.5 Anti-patterns

| Mistake | Symptom | Fix |
|---|---|---|
| Brackets in Style field | Tag sung as a lyric | Brackets belong in Lyrics |
| BPM in Lyrics field | BPM treated as a sung phrase | BPM in Style |
| Three or more genres | Muddy averaged output | Maximum two |
| Conflicting eras (70s + 2020s) | Period-incoherent mix | Pick one era |
| Artist names | Filtered or ignored | Describe the sonic fingerprint |
| "Make a song that…" | Verbs ignored or sung | Describe, do not command |
| Mixing tags and prose | Wasted tokens | Comma-separated tags |
| Repeating the same tag in both fields | Doubled cost, no benefit | Style for sound, Lyrics for words |

## 5.2 Genre Stacking and Fusion

Two genres maximum. Validated working pairs share at least one of tempo, instrumentation register, or vocal idiom.

| Pair | Why it works | Example tags |
|---|---|---|
| Pop + EDM | Shared 4/4, shared BPM band | dance-pop, sidechain, big chorus, 124 BPM |
| Gospel + trap | Shared swung 808 feel, shared vocal range | gospel trap, choir stabs, 808s, 140 BPM half-time |
| Jazz + hip-hop | Shared swung phrasing | boom bap, jazzy piano chop, vinyl crackle, 92 BPM |
| Indie folk + electronic | Shared intimate vocal pocket | folktronica, fingerpicked guitar, granular pads |
| Synthwave + indie pop | Shared 80s gated drum reference | synthpop, gated reverb, glossy synth, 116 BPM |
| Drum and bass + cinematic | Shared sub register, cinematic strings ride 174 | neurofunk DnB, orchestral strings, 174 BPM |
| Ambient + post-rock | Shared crescendo arc | ambient post-rock, ebowed guitar, glacial build |
| Country + soul | Shared vocal grit and Rhodes/pedal-steel mix | country soul, pedal steel, Rhodes, raspy male vocal |
| Phonk + drift trap | Shared cowbell, shared 808 | phonk, cowbell, distorted 808, memphis sample |
| Afrobeats + R&B | Shared groove tempo, shared melodic ad-lib | afro-R&B, log drums, melodic male vocal, 102 BPM |

When fusion fails: BPM mismatch (lo-fi at 78 BPM with drum and bass at 174 BPM produces averaged 120 BPM nothing), vocal idiom conflict (operatic over drill is rare in training data), era conflict (60s Motown over modern hyperpop). Drop to one genre and reinforce with mood.

## 5.3 Vocal Direction

Name gender, register, timbre, delivery, age, and processing — in that order.

| Axis | Tags |
|---|---|
| Gender | Male, female, androgynous |
| Register | Bass, baritone, tenor, alto, soprano, falsetto |
| Timbre | Warm, breathy, raspy, smoky, nasal, smooth |
| Delivery | Whispered, spoken, sung, belted, rapped, chanted |
| Age | Youthful, mature, weathered |
| Processing | Autotuned, vocoded, telephone EQ, doubled, layered |

### 5.3.1 Eight worked examples

```text
"Soft breathy female soprano, intimate close-mic, slight room"
  → dream pop / bedroom indie register
"Deep weathered baritone male, raspy delivery, dry"
  → folk noir / americana
"Autotuned melodic male rap, reverb-heavy, doubled ad-libs"
  → modern melodic trap
"Belted female alto, gospel rasp, plate reverb"
  → soul / contemporary R&B
"Falsetto male tenor, breathy, telephone EQ"
  → alt R&B
"Layered female harmonies, choir-stacked, no lead"
  → choral / sacred minimalism
"Spoken word female, monotone, dry close-mic"
  → trip-hop / spoken-word post-punk
"Shouted male tenor, blown-out, room reverb"
  → punk / hardcore
```

Anti-pattern: when a Voice profile is attached, drop all vocal descriptors from the Style field. They conflict with the cloned voice and produce blended timbre.

## 5.4 Production Direction

Era cue + texture cue + mix cue stack into a coherent recording aesthetic.

| Era cue | Texture cue | Mix cue |
|---|---|---|
| 80s gated reverb | Tape hiss | Wide stereo |
| 70s analog warmth | Vinyl crackle | Dry close-mic |
| 90s dusty sample | Plate reverb | Sidechain pump |
| 2010s indie aesthetic | Lo-fi tape | Compressed bus |
| 2020s glossy digital | Hi-fi modern | Stereo-wide polished |
| Late 60s Motown | Spring reverb | Mono mid-forward |

Triggering the right region:

```text
"80s gated reverb, analog warmth, wide stereo"
  → Phil Collins-era pop region
"90s dusty sample, vinyl crackle, raw head-nod groove"
  → boom-bap region
"2020s glossy digital, sidechain pump, stereo-wide polished"
  → modern dance-pop region
"Lo-fi tape, room mic, dry"
  → bedroom-folk / indie demo region
```

## 5.5 BPM and Key

Numeric BPM works as approximate guidance, not a metronome lock. v5.5 holds tempo more reliably than v5, but ±4 BPM drift is normal.

```text
"Indie folk, 95 BPM"          → lands 92–98 BPM
"120–130 BPM"                  → model picks one
"Half-time feel at 140 BPM"    → renders as 70 BPM groove
```

Key specification ("D minor", "A major") is soft guidance. The model honors it about 60% of the time. For mixing-compatibility scenarios, generate, detect actual key with an external tool, and reuse the prompt with the corrected key.

## 5.6 Negative Prompting / Exclude Styles

Two mechanisms.

Mechanism one — inline. Append `no X` at the end of the Style field. v5.5 processes positive descriptors first, then exclusions.

```text
warm acoustic folk, fingerpicked guitar, soft male vocals,
90 BPM, no drums, no electric guitar, no autotune
```

Mechanism two — Exclude Styles toggle. Pro and Premier only. Custom Mode > More Options > Exclude Styles. Excluded styles appear in Song Preview with a `-` prefix. Suno's official guidance from the September 19, 2024 X post (Tier 1):

> "You can now Exclude Styles when making new songs. Try excluding specific instruments, specific styles, or even specific vocal-styles such as male/female vocals."

API equivalent: `negativeTags` (string, comma-separated) in kie.ai and sunoapi.org schemas.

### 5.6.1 Effective exclusions

| Category | Tags |
|---|---|
| Instruments | piano, electric guitar, drums, bass, synthesizer, strings, 808s, hi-hats, banjo |
| Vocals | male vocals, female vocals, autotune, vibrato, choir, ad-libs |
| Tempo | fast tempo, slow tempo |
| Era | 1940s, 1980s, 2010s pop |
| Mood | aggressive, melancholic, euphoric |
| Processing | heavy distortion, breathy vocals, reverb-drenched, telephone EQ |

Suno's Style Stack X post lists "Heavy distortion, Breathy vocals, Fast tempo" as canonical examples (Tier 1).

### 5.6.2 Before / after

```text
Before:
Indie folk, soft male vocal, acoustic guitar, 95 BPM
Output: arrives with drum kit, light strings, occasional piano

After (with Exclude Styles: drums, piano, strings):
Same Style field, exclusions applied
Output: stays acoustic, stays sparse
```

Anti-pattern: do not use negatives to define. Five `no X` tags with no positive tags produce mush. Positives define, negatives refine. Cap exclusions at three.

## 5.7 Meta Tag Canon — Structural Tags

Bracket tags belong in the Lyrics field, on their own line, at the start of the section they govern. They control arrangement.

### 5.7.1 Tier 1 — officially documented

```text
[Intro]
[Verse]
[Pre-Chorus]
[Chorus]
[Post-Chorus]
[Bridge]
[Outro]
[Instrumental]
```

### 5.7.2 Tier 3 — community-validated, inconsistent

```text
[Hook]
[Drop]
[Build]
[Break]
[Solo]
[Interlude]
[Refrain]
[Verse 1] [Verse 2] [Chorus 1] [Chorus 2]
[Final Chorus]
```

Numbered variants ([Verse 1], [Verse 2]) work reliably for differentiation. Custom invented tags ([My Special Section]) do not work — they get sung as lyrics or ignored.

Order in the Lyrics field is the intended song order. Suno honors it most of the time. When it ignores order, regenerate; do not rewrite tags.

## 5.8 Meta Tag Stacking Inside Sections

Stack three to five tags per section, line-broken, in the order structural → instrumentation → texture/mood → vocal direction. From Suno's April 11, 2026 X post (Tier 1):

```text
[Intro]
[Fingerpicked acoustic guitar]
[Soft room reverb, vinyl warmth]

[Chorus]
[Soaring falsetto, layered harmonies]
[Strings swell, emotional lift]
```

### 5.8.1 Four additional worked examples

```text
Cinematic build:
[Intro]
[Sparse piano, single sustained string]
[Tape hiss, wide stereo]

[Build]
[Layered strings entering, timpani pulses]
[Plate reverb, gradual swell]

[Drop]
[Full orchestra, taiko drums]
[Wide stereo, compressed]
```

```text
Melodic trap verse-chorus:
[Verse 1]
[Pitched vocal chop loop, hi-hat rolls]
[Reverb tail, dry kick]
[Autotuned melodic male delivery]

[Chorus]
[Sub-bass 808 drop, layered ad-libs]
[Reverb-drenched, sidechain pump]
[Doubled lead, harmonized 3rds]
```

```text
Indie folk bridge:
[Bridge]
[Solo fingerpicked acoustic, no drums]
[Close-mic, room tone]
[Whispered male vocal, intimate]
```

```text
Industrial post-punk:
[Verse 1]
[Metallic percussion, chorused bass]
[Plate reverb, mono mid]
[Baritone male, monotone delivery]

[Chorus]
[Distorted guitar wall, pounding floor toms]
[Wide stereo, blown-out compression]
[Shouted male, doubled, telephone EQ]
```

Why stacking outperforms single tags: a single `[Chorus]` only signals arrangement. Stacked tags signal arrangement plus instrumentation plus texture plus delivery — four control surfaces engaged at the same line break. The model has more signal to act on.

## 5.9 Vocal Direction Inline — Performance Cues

Two formats.

Format one — bracketed tags above the lyric block:

```text
[Whispered]
The kitchen light was always on
The radio was never off

[Belted]
But I won't carry this anymore
```

Format two — parenthetical cues inline:

```text
(whispered) The kitchen light was always on
The radio was never off
(belted) But I won't carry this anymore
```

Reliable inline cues: `[Whispered]`, `[Spoken Word]`, `[Belted]`, `[Falsetto]`, `[Harmonized]`, `[Layered Vocals]`, `[Ad-lib]`, `[Hummed]`, `[Shouted]`. Parenthetical equivalents work the same way: `(whispered)`, `(belted)`, `(shouted)`, `(building intensity)`, `(stripped back)`.

### 5.9.1 Six before/after examples

```text
Before:
But I'm still here

After:
(building intensity)
But I'm still here
```

```text
Before:
[Chorus]
Waiting on the weather to change

After:
[Chorus]
[Belted, layered harmonies]
Waiting on the weather to change
```

```text
Before:
The garden's overgrown

After:
(whispered)
The garden's overgrown
```

```text
Before:
[Bridge]
Everything I wanted

After:
[Bridge]
[Falsetto, sparse piano only]
Everything I wanted
```

```text
Before:
[Verse 1]
I left the porch light on

After:
[Verse 1]
[Spoken word, dry close-mic]
I left the porch light on
```

```text
Before:
[Outro]
Hold on, hold on, hold on

After:
[Outro]
[Hummed, fading]
Hold on, hold on, hold on
```

Tier 3 caveat: descriptor-style cues like `[Mood: Nostalgic]` and `[Energy: Soaring]` work inconsistently. Some renders honor them, some treat the bracket contents as lyrics. Use sparingly, audition every time, and do not depend on them.

## 5.10 Lyric Flow and Pacing

From Suno's April 11, 2026 post (Tier 1): tight lines yield faster flow; blank lines between lyrics yield pacing. Line breaks are pacing signal, not aesthetic preference.

Verbatim Suno examples:

```text
Faster flow:
My shrink says I'm crazy
My boss says I'm lazy
I don't mind long as you
call me baby

More pacing:
My shrink says I'm crazy

My boss says I'm lazy

I don't mind long as you
call me baby
```

### 5.10.1 Four additional worked examples

Rapid-fire flow (drill, bars per beat):

```text
[Verse 1]
Block hot, opps watching, can't sleep, eyes locked
Phone off, cash up, gun tucked, four-block
Heart slow, mind fast, no friends, just stock
Ten cars, no plates, midnight, full block
```

Ballad pacing (one breath per line):

```text
[Verse 1]
The hallway light still flickers

The dog still waits at the door

I haven't moved your jacket

It still hangs there, the same as before
```

Syncopated phrasing (em-dash for delay):

```text
[Verse 1]
I told you — once — and never again
I held it — close — until I couldn't pretend
```

Call-and-response (parenthetical layered backing):

```text
[Chorus]
Come on home (come on home)
The lights are on (the lights are on)
I'll wait all night (all night)
Until the sun (the sun)
```

### 5.10.2 Punctuation behavior

| Mark | Effect |
|---|---|
| Comma | Short syllabic pause, lyric continues |
| Em-dash with spaces — | Longer pause, often delivered as melismatic stretch |
| Ellipsis … | Often sung, occasionally treated as silence |
| Blank line | Section pause, the strongest pacing signal |
| Period | Generally inert |

Anti-pattern: do not use exclamation marks expecting volume; v5.5 ignores them and they sometimes get sung as the word "exclamation."

## 5.11 Language and Code-Switching

Write the target language directly. Tags like `[Bilingual]` and `[Spanglish]` do not work alone.

```text
Multilingual chorus (French / English):
[Chorus]
On danse jusqu'à l'aube
Until the morning light
On danse, on tombe
Holding on so tight
```

For proper nouns and unusual phonemes, write phonetic spelling:

```text
"Saoirse" → "Seer-sha"
"Nguyen"  → "Nwen"
"Worcestershire" → "Wuss-ter-sher"
"Loooove" → sustained vowel, not a typo
```

Best supported languages (Tier 2 community testing): English, Spanish, Portuguese, French, Japanese, Korean, Mandarin. Other languages produce accented or imprecise pronunciation.

## 5.12 SFX Bracket Tags

Stated plainly: most SFX brackets are unreliable in v5 and v5.5.

| Tag | Behavior |
|---|---|
| `[applause]` | Often nothing; sometimes sung |
| `[vinyl crackle]` | Works as Style-field texture, not as Lyrics tag |
| `[tape hiss]` | Same — Style only |
| `[gunshot]` | Almost always nothing |
| `[crowd noise]` | Inconsistent |
| `[siren]` | Inconsistent |
| `[doorbell]` | Almost always nothing |

Do not deploy SFX bracket tags in production. Generate ambience separately via Suno Sounds (the experimental sound-effect generator), then layer in Studio. The Scribd "Suno AI Meta Tags Verification and Usage Guide" (Tier 3) catalogs which SFX tags reliably fail; use it as a do-not-use list, not a deployment list.

## 5.13 Section Length Control

`[Verse 8 bars]` and similar bar-count tags have no official support. Community reports are inconsistent. Honor rate is below 30%.

What works: in Suno Studio, the Edit menu lets the user set bar counts per section directly, with a numeric input at the bottom-left of the section editor. That control is Tier 1 and reliable. Move bar-count work into Studio; do not put it in the Lyrics field.

## 5.14 Creative Sliders Deep Dive

Suno's official help-center description (Tier 1):

> "Weirdness goes from Safe to Chaos, where 50% is the 'normal' expected result. Style Influence lets you choose how close you stay to your style input from Loose to Strong. If you're using an Audio Upload, you'll also get a third slider for Audio Influence."

| Slider | Range | API parameter | What it controls |
|---|---|---|---|
| Weirdness | 0–100% | `weirdnessConstraint` (0.00–1.00) | Deviation from genre defaults |
| Style Influence | 0–100% | `styleWeight` (0.00–1.00) | Adherence to Style of Music tags |
| Audio Influence | 0–100% | `audioWeight` (0.00–1.00) | Adherence to uploaded audio or Voice |

### 5.14.1 Weirdness bands

| Band | Behavior |
|---|---|
| 0–25% | Predictable, genre-accurate, conservative phrasing |
| 25–50% | Standard expressive output, default territory |
| 50–70% | Unusual instruments, rhythmic surprises, riskier vocal phrasing |
| 70–100% | Genuinely unpredictable; sometimes brilliant, sometimes unusable |

### 5.14.2 Style Influence bands

| Band | Behavior |
|---|---|
| 0–30% | Pure exploration, lyrics drive feel |
| 30–60% | Loose adherence to genre tags |
| 60–80% | Tight adherence, recommended default |
| 80–100% | Plateau; phrasing variation drops |

### 5.14.3 Audio Influence

Surfaces only with audio upload, Voice attached, or Cover. 70–90% recommended for cloning resemblance per community testing. Below 50% the upload becomes texture or reference rather than identity.

### 5.14.4 Recommended profiles by genre

| Genre | Weirdness | Style Influence | Audio Influence (if applicable) |
|---|---|---|---|
| Radio pop | 35–50% | 65–80% | 60–75% |
| Hip-hop / trap beds | 40–55% | 55–70% | 60–80% |
| Worship / gospel | 25–40% | 70–85% | 70–90% |
| Cinematic orchestral | 55–70% | 45–60% | n/a |
| Ambient / experimental | 70–85% | 35–55% | n/a |
| Indie folk | 30–45% | 70–85% | 70–85% |
| Voices clone (resemblance) | 30–45% | 60–75% | 75–90% |

Workflow rule: change one slider at a time, regenerate, A/B against the prior take. Otherwise the variable is uncontrolled.

## 5.15 Voices-Aware Prompting

When a Voice is attached, drop all vocal descriptors from the Style field and from the Lyrics field. They conflict with the clone.

```text
Without Voice:
Indie folk, 2010s bedroom, nostalgic, fingerpicked acoustic,
soft male vocal, breathy delivery, lo-fi tape warmth, 95 BPM

With Voice attached (drop "soft male vocal, breathy delivery"):
Indie folk, 2010s bedroom, nostalgic, fingerpicked acoustic,
upright bass, brushed drums, lo-fi tape warmth, room mic, 95 BPM
```

The freed character budget reallocates to production detail (instruments, texture, mix). Audio Influence at 70–90% holds resemblance. Below 70%, the clone drifts toward generic.

Suno's Voices FAQ (Tier 1) confirms: "If you find that the songs you make with your Voice don't sound like you, experiment with turning up the Audio Influence slider in the Create form."

## 5.16 Custom Model-Aware Prompting

A Custom Model already encodes style. Drop redundant style descriptors. Use the Style field for variations within the model's range.

```text
Custom Model trained on dark cinematic catalog
(without Custom Model selected):
Dark cinematic orchestral, 2010s trailer, foreboding,
deep strings, timpani, brass stabs, no vocals, D minor, 85 BPM

(with Custom Model selected — drop genre and era; keep variation tags):
Sparser arrangement than usual, solo cello lead,
rising tension, no choir, 90 BPM
```

The Custom Model handles genre, era, and aesthetic. The Style field handles deviation from the model's center. Custom Model + Voice + 70–90% Audio Influence is the deepest personalization stack v5.5 offers.

## 5.17 Common Pitfalls — Consolidated

| Don't | Do |
|---|---|
| Type "make a song about love" | Describe the sound: "Indie folk, soft male vocal, fingerpicked guitar, 95 BPM" |
| Stack three or more genres | Maximum two |
| Put `[Verse]` in the Style field | `[Verse]` belongs in Lyrics on its own line |
| Put "120 BPM" in the Lyrics field | BPM in the Style field |
| Use artist names | Describe the sonic fingerprint |
| Write 12 descriptors hoping for richness | Four to seven descriptors |
| Use exclamation marks for emphasis | Use vowel elongation: "Loooove" |
| Repeat tags across both fields | One field, one job |
| Trust SFX bracket tags | Generate ambience in Suno Sounds, layer in Studio |
| Set bar counts in lyrics ([Verse 8 bars]) | Set bar counts in Studio's Edit menu |
| Run six exclusions | Cap at three; positives define, negatives refine |
| Attach Voice and keep "soft male vocal" in Style | Drop vocal descriptors when Voice is attached |
| Use Custom Model and re-state its genre | Drop redundant descriptors; the model encodes them |
| Move three sliders at once | One slider at a time, A/B compare |

## 5.18 Style of Music Templates by Genre

Eight fully worked recipes. Each is copy-pasteable.

### 5.18.1 Cinematic / score

```text
Style of Music (≤300 chars):
Dark cinematic orchestral, 2010s trailer scoring, foreboding and grand,
deep strings, timpani rolls, brass stabs, taiko drums, no vocals,
D minor, 85 BPM, plate reverb, wide stereo

Exclude Styles: pop drums, autotune, electric guitar
Sliders: Weirdness 60, Style Influence 55, Audio Influence n/a
Lyrics scaffold:
[Intro]
[Sparse solo piano, single sustained string]
[Tape hiss, wide stereo]

[Build]
[Layered strings, timpani pulses]
[Plate reverb, gradual swell]

[Drop]
[Full orchestra, taiko, brass stabs]
[Compressed, wide stereo]

[Outro]
[Solo cello, fading reverb tail]
```

Annotation: Weirdness pushed to 60 because cinematic underscoring benefits from unexpected harmonic motion; Style Influence kept at 55 because the bracket-stack inside Lyrics carries the section logic.

### 5.18.2 Melodic techno

```text
Style of Music:
Melodic techno, 2020s European club, hypnotic and brooding,
analog arp, sub bass, minimal kick, sparse female vocal hook,
tape saturation, 124 BPM, wide stereo

Exclude Styles: vocals, breakbeats, distorted guitar
Sliders: Weirdness 45, Style Influence 70, Audio Influence n/a
Lyrics scaffold:
[Intro]
[Filtered arp, no kick]
[Subtle white noise sweep]

[Build]
[Add sub bass, percussion enters]
[Tension rise, snare roll]

[Drop]
[Full kick + bass, hook arp peaks]
[Stereo wide, sidechain pump]

[Breakdown]
[Drop kick, keep pad + female vocal phrase]

[Drop]
[Second drop variation]

[Outro]
[Filter down, tail to silence]
```

Annotation: female vocal hook is in Style despite Exclude Styles listing "vocals" — the exclusion is for sung verses; the brief hook phrase is treated as texture and survives.

### 5.18.3 Melodic trap

```text
Style of Music:
Melodic trap, 2020s atmospheric, dark moody,
deep sub 808s, glitchy hi-hat rolls, pitched vocal chops,
autotuned melodic male rap, reverb-drenched ad-libs,
minor key, 145 BPM half-time

Exclude Styles: live drums, acoustic guitar, bright synths
Sliders: Weirdness 45, Style Influence 65, Audio Influence n/a (or 75–85 if Voice)
Lyrics scaffold:
[Intro]
[Pitched vocal chop loop]
[Reverb tail, dry kick]

[Verse 1]
[Autotuned melodic male delivery]
[Hi-hat rolls, sub bass]
Block cold, head spinning, lights low
…

[Chorus]
[Doubled lead, harmonized 3rds]
[808 drop, layered ad-libs]
…

[Verse 2]
[Same delivery, pull back hi-hats]
…

[Outro]
[808 sustain, reverb fade]
```

Annotation: 145 BPM half-time renders as a 70 BPM groove with hi-hats riding the upper grid — the canonical trap feel. State both numbers explicitly.

### 5.18.4 Alt rock

```text
Style of Music:
Alt rock, late 90s post-grunge, brooding,
distorted guitars, driving drums, raspy male vocal,
tape warmth, dry close-mic vocal, 96 BPM

Exclude Styles: 808s, autotune, synthesizers
Sliders: Weirdness 35, Style Influence 75, Audio Influence n/a
Lyrics scaffold:
[Intro]
[Clean guitar arpeggio, kick pulse]

[Verse 1]
[Restrained delivery, hi-hat closed]
…

[Pre-Chorus]
(building intensity)
…

[Chorus]
[Distorted guitar wall, raspy belt]
…

[Bridge]
[Half-time drums, feedback drone]
…

[Final Chorus]
[Bigger, doubled vocal, ride cymbal open]
…
```

Annotation: Style Influence at 75 because the distorted-guitar identity needs to lock; Weirdness at 35 to keep the riff structure conventional.

### 5.18.5 Ambient drone

```text
Style of Music:
Dark ambient drone, 2010s isolationist, glacial and unsettling,
evolving pads, tape hiss, no percussion, no vocals,
plate reverb, wide stereo, 50 BPM

Exclude Styles: drums, vocals, melodic hook
Sliders: Weirdness 75, Style Influence 40, Audio Influence n/a
Lyrics scaffold (instrumental — toggle Instrumental ON):
[Intro]
[Single sustained pad, low frequency hum]

[Section 1]
[Pad evolves, second layer enters]
[Tape hiss rises]

[Section 2]
[Granular texture, distant feedback]

[Outro]
[Layers strip away, tail to silence]
```

Annotation: Weirdness 75 is correct for ambient — the genre rewards melodic surprise; Style Influence 40 lets the texture breathe rather than forcing arrangement convention.

### 5.18.6 Vocal-forward indie pop

```text
Style of Music:
Indie pop, 2010s bedroom, intimate and bittersweet,
fingerpicked acoustic guitar, soft female vocal,
slight lo-fi warmth, room mic, 92 BPM

Exclude Styles: 808s, heavy distortion, EDM drops
Sliders: Weirdness 40, Style Influence 75, Audio Influence 75–85 if Voice
Lyrics scaffold:
[Intro]
[Solo fingerpicked acoustic, room tone]

[Verse 1]
[Soft female vocal, close-mic]
The hallway light still flickers
The dog still waits at the door

[Pre-Chorus]
(building intensity)
And I haven't moved your jacket

[Chorus]
[Doubled vocal, light harmony stack]
Waiting on the weather to change
Waiting on a reason to stay

[Verse 2]
…

[Bridge]
[Solo guitar, whispered]

[Final Chorus]
[Layered harmonies, fuller mix]
```

Annotation: vocal descriptors in Style are kept because no Voice is attached. With a Voice, drop "soft female vocal, room mic" and route those characters into more production detail.

### 5.18.7 Ritual industrial post-punk

```text
Style of Music:
Ritual industrial post-punk, late 80s 4AD aesthetic, ominous,
metallic percussion, chorused bass, baritone male incantation,
plate reverb, dry mid, 102 BPM

Exclude Styles: pop hooks, major key, autotune
Sliders: Weirdness 65, Style Influence 60, Audio Influence n/a
Lyrics scaffold:
[Intro]
[Metallic clang loop, chorused bass enters]
[Plate reverb, mono mid]

[Verse 1]
[Baritone monotone, dry close-mic]
…

[Chorus]
[Distorted guitar wall, pounding floor toms]
[Shouted vocal layer behind lead]
…

[Bridge]
[Drop drums, single sustained guitar feedback]
…

[Final Chorus]
[Bigger, blown-out compression]
```

Annotation: this recipe pulls from a thin region of the model. Generate four variations and discard three. Higher Weirdness is essential.

### 5.18.8 Lo-fi hip-hop / chillhop

```text
Style of Music:
Lo-fi hip-hop, 2010s bedroom-producer aesthetic, melancholic,
dusty jazzy piano sample, brushed drums, vinyl crackle,
tape saturation, no vocals, 78 BPM

Exclude Styles: vocals, EDM drops, distortion
Sliders: Weirdness 50, Style Influence 70, Audio Influence n/a
Lyrics scaffold (instrumental):
[Intro]
[Solo piano sample, vinyl crackle]

[Section 1]
[Drums enter, brushed snare]
[Upright bass walks under]

[Section 2]
[Add Rhodes counter-melody, tape wobble]

[Bridge]
[Drop drums, piano alone]

[Outro]
[Drums return, fade to vinyl noise]
```

Annotation: lo-fi rewards "no vocals" in both Exclude Styles and the Style field — the genre is identified by absence as much as presence.

---

# 6. Personas / Voices Workflow

| Step | Detail |
|---|---|
| Open Create | Click Voice (replaced Personas) |
| Create new | Choose audio source: library, live record, upload |
| Audio | 15 s–4 min; Suno selects best 2 min |
| Verify | Read displayed phrase aloud |
| Name | Save and name |
| Use | Select Voice in Create; raise Audio Influence to 70–90% |

Acapella beats fully produced audio. If the input has a backing track, Suno auto-runs stem extraction. Voices remain private to the account. Voice sharing is unimplemented.

# 7. Covers, Stems, Editing

| Tool | Where | Function |
|---|---|---|
| Replace Section | Studio, song editor | Regenerate a region with new prompt or lyrics |
| Quick Replace | Studio | One-click regenerate with default behavior |
| Extend | Generation menu | Continue from end of current track |
| Crop | Edit menu | Trim head or tail (Pro/Premier) |
| Remaster | Track menu | Upgrade older-version output to v5/v5.5 fidelity |
| Reuse Prompt | Track menu | Pre-fill Style, Lyrics, Title for a new generation |
| Stems | Track menu | Up to 12 time-aligned WAVs (paid) |
| Suno Sounds | Standalone | Single-shot SFX, ambience, instrument samples |

Studio 1.2 (Premier-only update) added four tools:

| Studio 1.2 tool | Function |
|---|---|
| Warp Markers | Manual or transient-detected time-stretch points; quantize to grid |
| Remove FX | Strip generation-baked reverb and delay; reverb removal can raise loudness measurably |
| Alternates | Stacked takes per Remake / Rewrite / Remove FX action |
| Time signatures | Native 2/4, 3/4, 5/4, 6/8, 7/8, 12/8 |

Order of operations: Warp first, then Remove FX, then Alternates audition. Reversing order produces artifacts.

# 8. Output Specs

| Spec | Value |
|---|---|
| Sample rate | 44.1 kHz (v5 and v5.5 native) |
| Bit depth | 16-bit stereo |
| Format | MP3 (free, paid); WAV (paid) |
| Max generation length | 8 minutes |
| Stem count | up to 12 |
| MIDI export | Premier (Studio) |
| Variations per generation | 2 |
| Approximate cost per generation | ~5 credits |

# 9. API Access

There is no official public Suno API. Every "Suno API" is reverse-engineered.

| Provider | Status | Notes |
|---|---|---|
| kie.ai | Operating | V5_5, V5, V4_5PLUS, V4_5ALL, V4_5, V4 supported; reverse-engineered |
| sunoapi.org | Operating | V5_5 supported; reverse-engineered |
| CometAPI | Operating | Reverse-engineered |
| gcui-art/suno-api (GitHub) | Operating | Cookie-based; needs 2Captcha for hCaptcha |
| PiAPI | Discontinued for Suno V5 line | Vendor shutdown precedent |
| fal.ai | Does not host Suno | Misattribution common |
| Wavespeed.ai | Does not host Suno | Misattribution common |

Risks: each integration depends on cookies or scraped private endpoints that Suno can break without notice. Terms-of-service exposure runs from both Suno (against scraping) and from end-user redistribution (commercial-rights chain breaks at the cloned-account level). The PiAPI shutdown is the operative precedent for vendor disappearance.

# 10. Plans and What Each Unlocks

| Plan | Price | Credits | v5.5 | Voices | Custom Models | Studio | Stems | Commercial use | WAV |
|---|---|---|---|---|---|---|---|---|---|
| Free | $0 | 50/day | No (v4.5-all) | No | No | No | No | No | No |
| Pro | $10/mo or $8 annual | 2,500/mo | Yes | Yes | Yes (3) | No | Yes | Yes | Yes |
| Premier | $30/mo or $24 annual | 10,000/mo | Yes | Yes | Yes (3) | Yes | Yes | Yes | Yes |

Monthly subscription credits do not roll over. Purchased top-up credits do not expire but require active subscription. Annual saves ~20%.

# 11. Commercial Use

Paid-tier subscribers receive a license, not copyright. Verbatim from Suno's terms (Tier 1): Suno assigns its right, title, and interest in output generated during a paid subscription, but "makes no representation or warranty that any copyright will vest in that output."

Non-retroactive. Songs created on the free tier do not gain commercial rights when the user upgrades. Suno retains ownership of free-tier output.

Covers — songs generated by uploading another song and applying a new style — are not commercializable, regardless of plan.

Suno does not indemnify against third-party claims.

Active litigation as of May 8, 2026:

| Case | Court | Status |
|---|---|---|
| RIAA (UMG, Sony, Warner pre-settlement) v. Suno | D. Mass. 1:24-cv-11611 | Active; amended complaint September 22, 2025 added DMCA §1201 stream-ripping claims; summary-judgment hearing rescheduled to January 8, 2027 |
| GEMA v. Suno | Munich I, 42 O 763/25 | Heard March 9, 2026; judgment scheduled June 12, 2026 |
| WMG v. Suno | Settled November 25, 2025 | Licensed-model partnership announced; current models scheduled to be deprecated |
| UMG v. Suno | D. Mass. | Continues post-WMG settlement |
| Sony v. Suno | D. Mass. | Continues post-WMG settlement |
| Independent artist class action v. Suno | D. Mass. | Filed October 2025; motion-to-dismiss hearing March 20, 2026 |
| Koda (Denmark) v. Suno | Denmark | Active |

US Copyright Office position (Thaler v. Perlmutter, D.C. Cir.): purely AI-generated material does not qualify for copyright protection. Writing the prompt does not constitute authorship. Practical effect: revenue can be earned from Suno output, but DMCA takedowns, exclusive licensing, and Content ID may not attach.

# 12. Model Deprecation

Per the November 25, 2025 WMG settlement press release: "When the new models launch in 2026, the current models will be deprecated. Moving forward, downloading audio will require a paid account."

Action: export WAV stems for any track intended to be preserved before WMG-licensed successors ship. No exact deprecation date has been published. Free-tier downloads will end; paid-tier monthly download caps will be introduced. Studio sessions tied to deprecated models may not regenerate identically against successors.

# 13. Known Limitations and Failure Modes

| Failure | Cause | Mitigation |
|---|---|---|
| Genre drift on Extend | High Weirdness during Extend | Drop Weirdness below 40 for Extend |
| Vocal identity loss across sections | Low Audio Influence with Voice attached | Raise to 75–90% |
| BPM drift ±4 | Approximate, not metronome-locked | Detect post-gen, regenerate with explicit BPM |
| Lyrics rushed | Over 3,000 characters in Lyrics | Cut to 200–300 words |
| Section ignored | Custom invented bracket tag | Use Tier 1 canon only |
| SFX silently dropped | Tag unrecognized | Generate in Suno Sounds; layer in Studio |
| Style prompt truncated | Over 1,000 characters or below 200 on legacy | Front-load |
| Artist-name filter | Trained name in prompt | Describe sonic fingerprint instead |
| Reverb stuck on vocal | Generation-baked FX | Run Remove FX in Studio 1.2 |
| Crackle / clicks in v5.5 | Known artifact | Regenerate; use Studio 1.2 Remove FX experimentally |

# 14. Changelog — v5 → v5.5

| Date | Change |
|---|---|
| March 26, 2026 | v5.5 release: Voices, Custom Models, My Taste |
| March 26, 2026 | Personas button replaced by Voices |
| April 11, 2026 | Suno X "Style Stack" prompting framework published |
| Studio 1.2 (early 2026) | Warp Markers, Remove FX, Alternates, time signatures added |

# 15. Confidence and Gaps

| Item | Confidence | Note |
|---|---|---|
| Style Stack content | High | Reproduced verbatim from Tier 1 X post |
| help.suno.com category content | High | Voices, Voices FAQ, Custom Models, My Taste, Creative Sliders, Studio 1.2, length, lyrics — all directly sourced |
| API parameter names | High | Confirmed in kie.ai and sunoapi.org public schemas |
| `weirdnessConstraint` exact range and step | Medium | 0.00–1.00 step 0.01 per reseller schema; not officially confirmed |
| Slider profile recommendations | Medium-Tier 3 | Synthesized from JackRighteous and SunoStyles testing; not Suno-official |
| GEMA judgment outcome | Pending | Scheduled June 12, 2026 |
| Model deprecation date | Unknown | WMG settlement says "later in 2026"; no specific date published |
| BPM drift ±4 figure | Tier 3 | Community-reported, not Suno-confirmed |
| Voices verification phrase mechanism | High | Tier 1 from help.suno.com |
| Custom Model training time 2–5 min | High | Tier 1 from help.suno.com |
| Crackle / clicks in v5.5 | Tier 3 | User reports; not officially acknowledged |

# 16. Operator Brief

Suno v5.5 is a personalization layer over the v5 audio engine. The model improved obedience to subtle descriptors but did not change prompt syntax. The Style of Music field accepts up to 1,000 characters and is read as an ordered, weighted tag list — the first two to three tags dominate. The recommended fill is four to seven descriptors across genre, era, mood, instruments, and vocal direction. The Lyrics field accepts up to 5,000 characters and carries song structure via bracket metatags ([Intro], [Verse], [Chorus], [Pre-Chorus], [Post-Chorus], [Bridge], [Outro], [Instrumental]) and vocal delivery via parenthetical cues. Stack three to five tags per section, line-broken, ordered structural → instrumentation → texture/mood → vocal direction. Negative prompting works two ways: inline `no X` in the Style field and the Exclude Styles toggle in Custom Mode > More Options (Pro/Premier). Three Creative Sliders — Weirdness, Style Influence, Audio Influence — map to API floats `weirdnessConstraint`, `styleWeight`, `audioWeight` (0.00–1.00, step 0.01). When a Voice profile is attached, drop vocal descriptors from the Style field and raise Audio Influence to 70–90%. When a Custom Model is selected, drop redundant style descriptors. SFX bracket tags are unreliable; generate ambience in Suno Sounds and layer in Studio. Plans: Free at $0 (50 credits/day, non-commercial, v4.5-all only), Pro at $10/mo (2,500 credits, v5.5, commercial use, WAV, Voices, Custom Models, stems), Premier at $30/mo (10,000 credits, plus Studio). Commercial rights are a license, not vesting copyright; free-tier output is non-commercial and non-retroactive. There is no official public API — kie.ai, sunoapi.org, CometAPI, and gcui-art/suno-api are reverse-engineered. Current models are scheduled for deprecation when WMG-licensed successors ship later in 2026; export WAV now.

# 17. Recommendations

Now (this week)
- Migrate all Style of Music inputs to the four-to-seven descriptor format. Front-load genre. Audit existing prompts for tag count above seven and below four; rewrite both directions.
- Move all bracket structural tags into the Lyrics field on their own lines. Remove brackets from Style fields.
- Add Exclude Styles toggles to every paid-tier session; cap at three exclusions.
- Export WAV stems of any track intended for distribution. Treat the WMG-licensed successor as a future deprecation event.
- Disable My Taste during evaluation runs to remove a hidden variable.

30–90 days
- Build a personal Voice profile with a clean acapella in a quiet room, 60+ seconds, covering low and high register. Test Audio Influence at 70%, 80%, 90% and pick the band that holds resemblance against the user's reference recordings.
- Build at least one Custom Model on six stylistically consistent tracks. Use it as the new baseline, prompt with deviation tags only.
- Calibrate slider profiles per genre. Generate four takes per profile, log the win rate, settle on house defaults.
- Stand up Studio 1.2 finishing pipeline: Warp first, Remove FX second, Alternates third. Export multitrack when external mastering is required.
- Treat any track requiring strong copyright protection as ineligible from Suno output. Use Suno for sketches and stems; finish with human-authored elements that vest copyright.

End of 2026
- Re-evaluate the entire stack when WMG-licensed successors ship. Old Custom Models and Voices may not migrate. Generate a deprecation inventory now: every track, model, and Voice the operation depends on.
- Reassess the API question only after Suno announces an official public API. Until then, every reverse-engineered integration is a single-vendor-shutdown away from breaking.
- Track GEMA judgment (June 12, 2026) and the RIAA summary judgment (January 8, 2027). Both reshape the commercial-rights chain.

Benchmarks that change the recommendation
- Suno publishes an official API → reseller dependency drops; build directly.
- WMG-licensed successor launch date is announced → start parallel-track regeneration immediately.
- GEMA ruling for plaintiffs → expect EU geofencing or licensed-model rollout in EU first.
- Slider API floats change beyond 0.00–1.00 → re-test all genre profiles.
- v6 announcement → freeze production work on v5.5, begin migration testing.

# 18. Caveats

Slider profiles by genre are community-derived (Tier 3, JackRighteous and SunoStyles); Suno publishes only the qualitative Safe / Chaos / Loose / Strong scaling. BPM drift, crackle artifacts, and SFX failure rates are community-reported and not officially acknowledged.

Pricing, plan structure, and download policy are scheduled to change when WMG-licensed models ship. Free-tier download removal is announced but not yet enforced as of May 8, 2026. Verify against suno.com/pricing before committing.

Commercial use grants a license, not copyright. The US Copyright Office position on AI-generated material has not changed. Active litigation in three jurisdictions can and will reshape the rights chain inside the next 18 months.

The model is more obedient than v5, which means the prompt is more responsible than ever for what the model produces.