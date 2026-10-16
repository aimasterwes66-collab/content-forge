# AI-ART-FRAMEWORK — Context-Engineering Operating Manual

Generative media framework (stills / video / film / animation / sound) organized as a
PROMPT + CONTEXT ASSEMBLY LINE. Every folder is a context pack. Order matters.

## The Three Laws

1. CONTEXT OVER TOKENS — inject the smallest context pack that still pins the look.
   The framework tiers are sized so a full brief is ~15-25 context blocks, not 200.
2. LOCK THE STATIC, VARY THE DYNAMIC — style/camera/negative/quality packs stay
   stable per project; only subject packs (world/character/scene) change per shot.
3. NEGATIVES ARE POSITIONS — a negative pack is a first-class prompt layer, not a
   footnote. It defines the search space as much as the positive does.

## Tier Map (assembly order)

00-SYSTEM        framework rules, recipes, token budgets, context schemas
01-MEMORY        persistent motifs, learned styles, session state (compacts here)
02-ONTOLOGIES    the 6x121 keyword/modifier masters:
                 AI-MUSIC-KEYWORDS (music/sound prompts)
                 AI-ART-MODIFIERS (stills art/image/video modifiers)
                 VIDEO-MODIFIERS (motion, transitions, physics, loops)
                 FILM-GRAMMAR (shots, cuts, montage, pacing, genre grammar)
                 ANIMATION-MODIFIERS (12 principles, smears, cycles, styles)
                 SOUND-DESIGN (foley, ambience, SFX, voice, mix)
03-VOCABULARY    prompt grammar, weighted terms, chaining rules, emphasis syntax
10-WORLD         setting context: eras, locations, factions, ecology (FICTIONAL/REAL-LIFE)
11-CHARACTERS    cast context: sheets, appearances, arcs, voices, costumes
12-STORY         narrative context: beats, scenes, plots, twists, dialogue
20-CAMERA        shot types, focal lengths, angles, moves, rigs, aerial
21-LIGHTING      schemes, time-of-day, practicals, volumetric, period light
22-COMPOSITION   framing, thirds, negative space, depth layers, symmetry/chaos
23-MOTION        easing, speed ramps, physics, secondary motion, blur
24-COLOR         palettes, grades, LUTs, temperature, contrast, bleed
25-TEXTURE       materials, wear, finishes, organic/inorganic, macro detail
26-STYLE-REF     movements, precedents, hybrid styles, trademark-safe paraphrases
30-VIDEO-ENGINE  frame rates, transitions, keyframes, temporal consistency, in/outpainting
31-FILM-ENGINE   editing grammar, coverage, montage, storyboards, animatics, titles
32-ANIMATION-ENGINE  12 principles, rigs, cycles, lip-sync, walk cycles, smears
33-STILLS-ENGINE seed logic, aspect ratios, detail multipliers, resolution hacks
34-SOUND-ENGINE  music keywords, foley, voice, ambience, SFX cues, mix terms
40-CONTROL       quality boosters, consistency locks, style pinning, seed anchors
41-NEGATIVE-PROMPTS  exclusions: anatomy fails, text artifacts, watermark, leaks
42-QUALITY-GATES eval criteria, checkpoint tests, iteration logs, acceptance sheets
43-EDGE-CASES    uncanny valley, prompt drift, mode collapse, AI tells
50-META          versioning, changelogs, provenance, licensing, sources
51-TEMPLATES     reusable prompt scaffolds per medium
52-WORKSHOPS     live iteration sandboxes (experiments/failures/breakthroughs)
53-ARCHIVE       retired and superseded material
54-PIPELINES     end-to-end recipes: concept -> prompt -> frame -> sequence -> film

## Golden Prompt Recipe (stills / single frame)

[00-SYSTEM role block] + [01-MEMORY compact] + [10 WORLD pack] +
[11 CHARACTER pack] + [26 STYLE-REF pack] + [20 CAMERA pack] +
[21 LIGHTING pack] + [22 COMPOSITION pack] + [24 COLOR pack] +
[25 TEXTURE pack] + [33 STILLS quality] + [41 NEGATIVES] + [42 GATE]

## Golden Prompt Recipe (video / film / animation)

[SYSTEM] + [MEMORY] + [10 WORLD] + [11 CHARACTER] + [12 STORY beat] +
[26 STYLE] + [20 CAMERA moves] + [23 MOTION] + [21 LIGHT] + [24 COLOR] +
[30/31/32 MEDIUM ENGINE block] + [34 SOUND cue] + [40 CONTROL locks] +
[41 NEGATIVES] + [42 GATE per shot]

## Rules of Thumb

- One context pack per folder = one stable chunk. Keep each pack under the
  token budget in 00-SYSTEM/token-budgeting.
- Copy the framework per-project (or symlink 02/26/41/42 which rarely change).
- Reuse 52-WORKSHOPS for controlled experiments; promote wins to 51-TEMPLATES
  and 01-MEMORY/learned-styles.
- When a style destabilizes (drift), freeze it: 40-CONTROL/style-pinning +
  43-EDGE-CASES/prompt-drift diary.