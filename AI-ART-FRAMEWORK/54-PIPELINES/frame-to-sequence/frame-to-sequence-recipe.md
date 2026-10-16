# PIPELINE: Frame -> Sequence
Goal: extend a single gate-passed frame into a coherent multi-shot sequence.

## Input
One gated still frame + storyboard cards from 31-FILM-ENGINE/storyboards

## Procedure
1. Establish identity anchor from the gated frame (40-CONTROL/seed-anchors)
2. For each shot in the storyboard:
   a. Vary ONE craft parameter at a time (camera OR light OR position — never identity)
   b. Keep all 40-CONTROL/consistency-locks identical between shots
   c. Apply temporal-consistency rules from 30-VIDEO-ENGINE/temporal-consistency
   d. Gate each shot independently
3. Check temporal seams: frame N vs N-1 for continuity
4. If seam fails -> adjust shot N's identity lock + re-gate

## Key constraints
- Subject identity must NOT change between frames
- Props/environment positions must persist
- Lighting scheme must stay constant unless story-motivated
- Only camera move/angle varies freely
- Motion (for video) inherits easing from 23-MOTION
