# CHAINING RULES — linking prompt segments
Prompts chain when a single generation needs constraints across multiple domains.
Chain order: WORLD -> SUBJECT -> STYLE -> CRAFT -> QUALITY

## Chain syntax
- `|` separator: SECTION|SECTION|SECTION (flat chain)
- `, ` natural separator: component tokens within section
- `--` explicit thematic break

## Context chaining (for sequences)
[WORLD: cyberpunk-alley] -> [SUBJECT: detective, trenchcoat] -> [STYLE: neo-noir] ->
[CAMERA: low-angle, wide] -> [LIGHT: neon-wash, rain-slick]

## Chaining rules
1. Never chain before the subject noun — subject must be first
2. Style chain immediately after subject, before camera/light
3. Quality/control tokens are ALWAYS last
4. Negative tokens are NOT chain tokens — they're a separate input field
5. For video sequences, chain SHOT_N into SHOT_N+1 preserving identity + camera
