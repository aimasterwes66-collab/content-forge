# TERMINAL EMPHASIS SYNTAX
How emphasis is expressed in different prompt environments:

## Text model emphasis
- `[CAPS]` = loud, prominent, shouted
- _italic_ = subtle, whispered, internal
- **bold** = crucial, anchoring, must-not-drift
- `code` = technical, precise, literal

## Image model emphasis
- repetition: "very dark, DARK, EXTREMELY dark" vs "dark"
- position: earlier = more important (subject first rule)
- specificity: "red" < "crimson" < "oxidized-blood-crimson"
- compound: "32mm f/1.4 portrait lens" vs "lens"

## Weighted syntax (cross-model)
- (term:1.0-1.5) = amplify
- (term:0.3-0.9) = attenuate
- [term] = SD-specific negative emphasis
- term::float = platform-agnostic weight

## Context-wrapping
- "in the style of X" = style injection
- "X, but Y" = override (use sparingly; causes drift)
- "while maintaining Z" = preservation instruction

## Golden rule
For each token, ask: does this NARROW or EXPAND the output?
If it expands, replace it with a narrower term or add a constraint.
