# PIPELINE: Concept -> Prompt
Goal: turn a story beat or idea into a complete, gate-ready prompt.

## Step 1 — extract constraints
From the concept note (12-STORY/beats), extract:
- Subject (who) -> 11-CHARACTERS sheet
- Setting (where/when) -> 10-WORLD pack
- Mood (emotion) -> check HEARTFIRE or MOOD ontologies
- Action (what happening) -> one sentence present tense
- Duration (for motion) -> short/medium/long shot

## Step 2 — select context packs
- World pack from 10-WORLD/ (pick one per scene)
- Character sheet from 11-CHARACTERS/sheets
- Style reference from 26-STYLE-REF/movements or hybrid-styles
- Camera grammar from 20-CAMERA/shot-types + moves

## Step 3 — assemble prompt
Use the golden template from 51-TEMPLATES:
[SYSTEM] + [MEMORY] + [WORLD] + [CHARACTER] + [STYLE] + [CAMERA] + [LIGHT] + [MOTION/video only] + [COLOR] + [TEXTURE] + [CONTROL] + [NEGATIVES]

## Step 4 — set control gates
- 40-CONTROL/style-pinning (3 adjectives constant)
- 40-CONTROL/consistency-locks (seed + features)
- 40-CONTROL/seed-anchors (subject-anchor line)

## Step 5 — gate
- 42-QUALITY-GATES eval-criteria: score identity/craft/negatives/temporal/intent/style
- Reject <3, iterate with 52-WORKSHOPS
