# PIPELINE: Final Grade
Goal: final color + audio grade before output delivery.

## Final color
- Apply LUT family from 24-COLOR/luts
- Grade per 24-COLOR/grades/grade-grammar (temperature, contrast, accent)
- Consistency check: compare grade across all shots in the same scene

## Final audio
- Master mix: level all sound layers (34-SOUND-ENGINE/mix-terms)
- Loudness gating: 34-SOUND-ENGINE/loudness-feel from SOUND-DESIGN ontology
- Crossfade scene transitions

## Export
- Resolution: per 30-VIDEO-ENGINE/resolutions/format-recs
- Frame rate: per 30-VIDEO-ENGINE/frame-rates/rate-feel
- Aspect ratio: per 33-STILLS-ENGINE/aspect-ratios or 30-VIDEO resolutions

## Delivery
- Archive final in 53-ARCHIVE/superseded (with version tag)
- Log prompt + params in 50-META/changelogs
- Promote working template to 51-TEMPLATES if reusable
