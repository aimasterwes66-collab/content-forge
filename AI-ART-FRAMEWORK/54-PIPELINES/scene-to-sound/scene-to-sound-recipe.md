# PIPELINE: Scene -> Sound
Goal: attach audio context to a generated sequence.

## Input
Sequence of gate-passed frames + storyboard cards (which include sound cue notes)

## Procedure
1. For each shot, identify:
   - Foley needed (from 34-SOUND-ENGINE/foley pack)
   - Ambience layer (from 34-SOUND-ENGINE/ambience pack)
   - Impact SFX (from 34-SOUND-ENGINE/sfx-cues — impacts, whooshes, clicks)
   - Voice (from 34-SOUND-ENGINE/voice pack — V/O, dialogue, narration)
2. Select mix terms from 34-SOUND-ENGINE/mix-terms
3. Pull sound-design prompt terms from ONTOLOGY-SOUND-DESIGN.md (foley/ambience/SFX categories)
4. Assemble the audio prompt:
   [AMBIENCE] + [FOLEY] + [IMPACTS] + [VOICE] + [MIX: placement, reverb-level]
5. Generate or composite audio; gate on clarity, synch-point alignment, mix balance
