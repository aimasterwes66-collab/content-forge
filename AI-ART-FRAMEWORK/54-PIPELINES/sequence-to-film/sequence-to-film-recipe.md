# PIPELINE: Sequence -> Film
Goal: assemble generated shots into a film sequence with editing and pacing.

## Input
Multiple gate-passed sequences + storyboard cards from 31-FILM-ENGINE

## Procedure
1. Edit assembly:
   - Lay shots in storyboard order
   - Apply transitions from 30-VIDEO-ENGINE/transitions
   - Set pacing from 31-FILM-ENGINE/grammar (180-rule, shot-reverse-shot)
   - Cross-cut parallel action using 31-FILM-ENGINE/cross-cutting
2. Montage if needed: 31-FILM-ENGINE/montage/montage-types
3. Title sequence: 31-FILM-ENGINE/title-sequences/title-style-lexicon
4. End credits: 31-FILM-ENGINE/credits/credit-conventions
5. Sound layer: composite scene-to-sound output per shot
6. Gate: 42-QUALITY-GATES/acceptance-sheets per scene
7. Iterate drift fixes in 52-WORKSHOPS/experiments
