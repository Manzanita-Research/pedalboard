---
name: stylescape
description: Visual style exploration for independent musicians and artist projects. Use when a musician wants to dial in visuals, generate style directions, create stylescapes, explore cover art / social / merch / video aesthetics, compare visual lanes, or turn generated image variants into brand guidelines. This skill reads ARTIST.md and DESIGN.md, proposes 3-5 distinct visual lanes, uses available image generation tools when present, then distills the selected direction back into DESIGN.md so later promo and video skills inherit a coherent visual world.
allowed-tools: Read Write Edit Glob Grep
---

# Artist Stylescape

Generate visual lanes, help the artist choose, then update `DESIGN.md`.

This is not a logo generator and not a final cover-art pipeline. It is a taste-calibration instrument.

The user may invoke this as:

- `/artist:stylescape`
- `/artist:stylescape quick`
- `/artist:stylescape deep`
- `/artist:stylescape refresh`

If no mode is clear, default to `quick`.

## Ground Rules

- Read `ARTIST.md` first. If it is missing or placeholder, run `/artist:onboard` before continuing.
- Read `DESIGN.md` if present. Treat it as a working hypothesis, not law.
- Ask one clarifying question if the intended asset surface is unclear.
- Generate visual options as distinct lanes, not minor variations of one idea.
- Do not generate images immediately. First present lane briefs and wait for explicit user approval.
- Never collapse the artist into genre defaults. Preserve anti-references.
- Do not update `DESIGN.md` with a lane until the user chooses or clearly approves it.
- If image generation is unavailable, write image prompts and a comparison matrix instead of pretending images were generated.
- Keep generated images and notes in a project-local `stylescapes/` folder when the project filesystem is available.
- A stylescape is not one impressive hero image. It should expose reusable visual grammar: palette, texture, typography feel, motif, composition, motion implication, and asset applications.
- "Looks like AI" is a hard failure. Reject glossy CGI, generic fantasy concept art, over-rendered cosmic digital painting, fake game-cinematic environments, and prompt-candy visuals unless the artist's actual references require that exact medium.

## Preflight

Before making images or prompts:

1. Locate the artist project directory.
2. Read `ARTIST.md` and `DESIGN.md`.
3. Identify:
   - current era and primary goal
   - visual thesis
   - taste anchors
   - anti-references
   - palette and motif hypotheses
   - the output surface: social, lyric video, visualizer, cover art, merch, show poster, or general brand system
4. Name three reflex visual defaults you might accidentally reach for, then reject them.
5. Say:

```text
PEDALBOARD_STYLESCAPE_PREFLIGHT: artist=pass design=pass|missing surface=known|asked imagegen=available|unavailable mutation=closed
```

Open mutation only after the user has chosen a lane or explicitly asks for drafts to be saved.

## Modes

### Quick

Use for a first stylescape pass.

1. Propose 3 visual lanes with names and 2-3 bullets each.
2. Score each lane against the artist context and anti-references.
3. Ask the user to pick lanes to generate. Only proceed after explicit approval.
4. For each approved lane, create one stylescape board or concept image suitable for a moodboard.
5. Compare the lanes against `ARTIST.md`.
6. Ask which lane to keep, merge, or reject.
7. Update `DESIGN.md` only after selection.

### Deep

Use for more serious brand-world work.

1. Propose 4-5 lanes.
2. Score each lane and ask the user which to generate.
3. For each approved lane, generate 2-3 assets:
   - key art / world image
   - social still or vertical crop concept
   - merch or poster object concept
4. Create a `STYLESCAPE.md` with image references, prompt text, strengths, risks, and recommended usage.
5. Distill the selected direction into `DESIGN.md`.

### Refresh

Use when visual work already exists.

1. Read `DESIGN.md` and any recent `stylescapes/**/STYLESCAPE.md`.
2. Ask what feels wrong, stale, too generic, or newly exciting.
3. Generate replacement lanes only for the parts that need movement.
4. Patch `DESIGN.md` narrowly.

## Image Generation Workflow

Use the available image generation tool when the environment supports it. In Codex, use the `imagegen` skill / built-in `image_gen` tool by default.

Before using image generation, run the anti-slop gate:

1. Name the lane's **medium**: documentary photo, scanned print artifact, xerox collage, risograph poster, stage-light photograph, merch/product photo, hand-painted illustration, 3D render, etc.
2. Name the lane's **physical object**: record sleeve, ritual scarf, burned show flyer, altar cloth, tour poster, VHS still, black candle label, lyric booklet, venue projection, merch table photo, etc.
3. Name the lane's **non-AI reference logic**: what would this look like if a human designer, photographer, printmaker, art director, or stage designer made it?
4. Reject the lane if its only visual logic is "beautiful generated image."

For each generated lane:

- Use case: `stylized-concept`, `ads-marketing`, or `product-mockup`, depending on surface.
- Asset type: stylescape board, not a final cover unless explicitly requested.
- Prompt from `ARTIST.md` + `DESIGN.md`, with the lane's unique thesis.
- Include constraints and anti-references explicitly.
- Ask for a composed board when exploring brand direction: one large atmosphere panel plus 4-6 smaller studies for palette, texture, motif, type feel, social crop, and object/merch application.
- Avoid text in images unless the user asks for a poster or merch mockup with exact copy.
- Prefer 16:9 for visualizer/brand-world lanes, 9:16 for reels, 1:1 for grid/moodboard, and product framing for merch.
- Reject generated outputs that are merely beautiful but generic. Say why, then revise the prompt before saving them as guidance.

Prompt against AI/CGI slop explicitly:

- Prefer physical, camera, print, scan, textile, object, stage, or editorial art-direction language.
- Use lens/film/print/process words when relevant: 35mm flash photo, xerox, risograph, offset ink, screenprint, tour-poster paper, VHS still, projected stage light, embroidered thread, foil-stamped card, candle-label photo.
- Avoid or ban: CGI, 3D render, Unreal Engine, Octane render, glossy digital painting, fantasy concept art, videogame environment, hyper-detailed cosmic goddess, generic tarot, ornate AI glyph overload, "epic cinematic" as the only idea.
- If the lane truly needs illustration, specify a human-feeling process: gouache poster, ink drawing, screenprinted gig poster, illuminated manuscript scan, airbrushed van-art panel, handmade collage, photocopied zine spread.

Save final selected images into:

```text
stylescapes/YYYY-MM-DD-<slug>/
```

Suggested files:

```text
stylescapes/YYYY-MM-DD-<slug>/
├── STYLESCAPE.md
├── lane-1-<name>.png
├── lane-2-<name>.png
└── lane-3-<name>.png
```

If images cannot be generated, still write `STYLESCAPE.md` with complete prompts.

## Lane Template

Use this structure before generation:

```md
## Lane: <Name>

Thesis: <one sentence>

- Best for:
- Visual ingredients:
- What it protects from ARTIST.md:
- Risk:
- Anti-reference risk:
- Medium:
- Physical object:
- Slop risks:
- Score:
- Prompt:
```

Lane names should be memorable and specific. Avoid generic names like "Dark", "Light", "Modern", or "Vintage".

## Scoring

Score each proposed lane before image generation:

```md
### Score

- Artist fit: /5
- Distinctiveness: /5
- Anti-reference safety: /5
- Anti-AI-slop safety: /5
- Reusable system value: /5
- Promo/video usefulness: /5
```

If a lane scores below 4 on anti-reference safety, anti-AI-slop safety, or reusable system value, rewrite it before generating.

Common failure modes:

- **Poster trap:** one dramatic scene, no reusable system.
- **Genre-default trap:** generic metal, witchcore, fantasy goddess, wellness, or cinematic goth defaults.
- **Image-model candy:** beautiful saturated cosmic art that ignores the artist's actual thesis.
- **CGI-slop trap:** glossy 3D/concept-art surfaces, impossible polished temples, over-rendered cosmic figures, and fake game-cinematic lighting.
- **Prompt ontology trap:** the prompt names the subject but not the medium, object, or human production method.
- **Portrait drift:** attractive avatar image with weak ritual/cosmological grammar.
- **Moodboard blur:** pretty references with no decisions about palette, type, composition, or usage.

## STYLESCAPE.md Template

```md
# Stylescape: <Artist / Project>

## Source Context

- ARTIST.md:
- DESIGN.md:
- Goal:
- Surface:

## Lanes

### <Lane Name>

- Image:
- Thesis:
- Strengths:
- Risks:
- Medium:
- Physical object:
- Score:
- Prompt:

## Recommendation

## User Decision

## DESIGN.md Patch Notes

-
```

## DESIGN.md Update Rules

After the user chooses a lane, update only the relevant sections:

- `Visual Thesis`
- `References`
- `Palette`
- `Type And Layout`
- `Image Treatment`
- `Motion`
- `Symbols And Motifs`
- `Merch And Objects`
- `Never Do This`
- `Still Unknown`

Preserve useful existing language. Add a short note if the chosen direction merges multiple lanes.

## Quality Bar

A good stylescape makes future visual work easier. The user should be able to say:

- "Yes, this is the world."
- "This is close, but too soft / too literal / too trendy."
- "Make the video / poster / merch feel like lane 2 with lane 3's palette."
- "I know what to make next."

If the generated images are beautiful but strategically wrong, say so and regenerate with a narrower prompt.
