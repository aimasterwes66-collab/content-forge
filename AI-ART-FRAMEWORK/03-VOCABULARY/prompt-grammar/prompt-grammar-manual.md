# PROMPT GRAMMAR — the assembly language of generative AI
A prompt is a constraint-specification, not a wish. Every token either narrows the
output distribution or wastes a slot. Grammar rules:

## Token roles
- NOUN = subject (what): "man", "city", "dragon", "knight"
- ADJECTIVE = modifier (which): "weathered", "cyan-lit", "brass-and-leather"
- VERB = action/setting (what doing): "walks", "fades", "transforms"
- CONTEXT = world/anchor (where/when): "cyberpunk-tokyo", "victorian-london"

## Canonical prompt order (for stills)
[SUBJECT] + [VERB?] + [STYLE] + [CAMERA] + [LIGHT] + [COMP] + [COLOR] + [TEXTURE] + [NEGATIVES]
Weight: subject carries 40%, style 20%, camera/light 25%, other 15%

## Canonical prompt order (for motion/video)
[SUBJECT] + [ACTION/EVOLUTION] + [CAMERA MOVE] + [TRANSITION] + [MOTION] + [STYLE] + [DURATION]
Time-based tokens must appear IN ORDER of the shot timeline
