# WEIGHTED TERM SYNTAX
Standard:  (term:factor)  or  term::factor

## Weighting conventions
- normal emphasis: (word:1.2) or word::1.2 — slight push
- strong emphasis: (word:1.5) — dominant element
- de-emphasis: (word:0.7) — background it
- suppression: (word:0.3) — barely present
- negative: (word:-0.5) — explicitly avoid (redundant with negatives pack)

## Platform notes
- Stable Diffusion: (token:1.2), {token} for +10%, [token] for -10%
- Midjourney: primarily adjective stacking; --style, --iw, --cw, --s for weight
- ComfyUI: node-based; strength inputs govern weights explicitly
- Sora/Runway: natural language dominates; weighted repetition instead of numeric
  e.g. "a cyberpunk city" vs "a VERY cyberpunk, EXTREMELY neon city"

## Compositional weighting
Combine weights to express relationships:
- (subject:1.3) + (style:1.2) + subject -- (style:0.8)  = subject-driven
- (camera:1.4) + subject -- (style:0.7)               = camera as POV
