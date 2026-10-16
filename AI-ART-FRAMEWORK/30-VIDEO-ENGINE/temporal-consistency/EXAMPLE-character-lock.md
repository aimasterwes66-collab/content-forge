# TEMPORAL CONSISTENCY — character lock
> rule: subject identity must persist across frames.
- anchor: reference image + seed (40-CONTROL/seed-anchors)
- per-frame reassert: <3 fixed face features> + <costume set>
- motion coherence: keep 23-MOTION params identical between keyframes
- check: 42-QUALITY-GATES per-shot sheet, compare against frame N-1
