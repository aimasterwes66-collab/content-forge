# VAULT INDEX — Worldbuilding / Character / Narrative System

5 overarching parents, 59 sub-folders, 295 populated stubs, 2 master ontologies (121 terms each).

## The two master ontologies

- `ONTOLOGY-AI-MUSIC-KEYWORDS.md` — 121 AI music/sound prompt keywords (11 cats x 11)
- `ONTOLOGY-AI-ART-MODIFIERS.md` — 121 AI art/video/image prompt modifiers (11 cats x 11)

Both are copied into EVERY sub-folder for offline use. Edit the masters at root, then re-sync with `cp`.

## Parents and their content folders

### WORLD-BUILDING — the setting as artifact: environments, peoples, systems, and how they run.

- Shared spine (every parent): FICTIONAL, REAL-LIFE, METADATA, TEMPLATES, WORKSHOPS, ARCHIVE
- `races` — peoples, species, lineages
- `locations` — places and their character
- `technology` — tools, machines, infrastructure
- `fauna-and-flora` — creatures, plants, ecology
- `geography-and-cartography` — terrain, maps, borders
- `science-and-magic-systems` — physics, alchemy, spell-logic
- `economy-and-trade` — currency, markets, resources

### CHAR-DESIGN — cast engineering: who exists, how they look, feel, fill a role, and change.

- Shared spine (every parent): FICTIONAL, REAL-LIFE, METADATA, TEMPLATES, WORKSHOPS, ARCHIVE
- `classes` — roles, vocations, archetypes
- `clothing` — dress, armor-adjacent, silhouette
- `weapons` — arms, tools of violence
- `moods` — emotional states as material
- `character-arcs` — transformation paths

### NARRATIVE-STRUCTURE — story engine: what happens, how conflict fires, where it breaks.

- Shared spine (every parent): FICTIONAL, REAL-LIFE, METADATA, TEMPLATES, WORKSHOPS, ARCHIVE
- `storytelling` — craft, voice, delivery
- `plot-twists` — reversals and reveals
- `conflicts-and-wars` — battles, campaigns, friction

### SETTING-LORE — the flavor layer: culture, belief, aesthetics, sound, taste, law, language.

- Shared spine (every parent): FICTIONAL, REAL-LIFE, METADATA, TEMPLATES, WORKSHOPS, ARCHIVE
- `culture` — customs, norms, collective behavior
- `belief-systems` — faiths, cosmologies, dogmas
- `iconography` — symbols, sigils, visual language
- `design-aesthetics` — style genomes and looks
- `rituals-and-festivals` — ceremonies, holidays, rites
- `music-and-soundscapes` — audio identity, sonic worlds
- `food-and-cuisine` — meals, ingredients, dining
- `languages-and-scripts` — tongues, writing systems
- `laws-and-governance` — codes, factions, power

### TIMELINE-HISTORY — the temporal spine: eras, anchors, artifacts, and period machines.

- Shared spine (every parent): FICTIONAL, REAL-LIFE, METADATA, TEMPLATES, WORKSHOPS, ARCHIVE
- `earth` — real-world anchor and atlas
- `middle-ages` — medieval era strata
- `mid-century` — mid-1900s era strata
- `objects-and-artifacts` — relics, tools, treasures
- `muscle-cars-and-motorcycles` — period machines, chrome era

## Stub convention

Each folder holds `1.md`..`5.md` (5 stubs), pre-populated with folder-relevant keywords
(music ontology) and modifiers (art ontology), round-robined so the five stubs cover the
folder's selected categories. Functional folders (METADATA/TEMPLATES/WORKSHOPS/ARCHIVE)
carry operational placeholders instead.

## Workflow

1. Edit ontology masters at root when the vocab evolves.
2. Re-sync: `for d in $(find <PARENT> -type d ...); do cp ONTOLOGY-*.md "$d"/; done`
3. Grow stubs from 5-per-folder by copying and re-theming, or attach an ontology category
   to a folder by editing its stub's `keywords:` / `modifiers:` blocks.

