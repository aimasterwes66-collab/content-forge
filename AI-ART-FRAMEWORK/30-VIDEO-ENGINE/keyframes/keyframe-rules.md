# KEYFRAME RULES
- lock identity at k0: seed + 3 fixed features + costume
- change ONE craft param per keyframe (camera OR light OR motion)
- interpolate craft params, never identity params
- motion vectors between keyframes inherit 23-MOTION easing
- max drift budget: <5% face/feature variance between kN, kN+1
