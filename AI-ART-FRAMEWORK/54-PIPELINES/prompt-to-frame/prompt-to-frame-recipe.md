# PIPELINE: Prompt -> Frame
Goal: generate a single frame from an assembled prompt.

## Input
A fully assembled canonical prompt from concept-to-prompt pipeline.

## Procedure
1. Load in the target engine (33-STILLS-ENGINE for stills, 30-VIDEO for motion)
2. Apply 41-NEGATIVE-PROMPTS for the medium
3. Apply 40-CONTROL seed anchors + style pins
4. Generate; if motion, use minimum viable frame rate (30-VIDEO/frame-rates)
5. Run 42-QUALITY-GATES:
   - Identity match (check vs character sheet)
   - Style driftt check (3 adjectives)
   - Negative tripped? (scan for watermark, artifacts, anatomy)
6. If gate fails -> 52-WORKSHOPS/experiments: change ONE variable per iteration
7. If gate passes -> stage to frame-to-sequence pipeline

## Common failure modes
| symptom | likely cause | fix |
|----------|-------------|------|
| subject drift | seed changed, character lock missing | re-anchor + freeze seed |
| oversaturated | color palette too warm | switch to cold LUT |
| anatomy fail | negative pack missing common-exclusions | add anatomical-fails |
| uncanny | subsurface-scatter + texture missing | add skin-texture pack |
