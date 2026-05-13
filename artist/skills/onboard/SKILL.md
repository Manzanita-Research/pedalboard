---
name: onboard
description: Guided artist onboarding for independent musicians. Use when a musician wants to set up, clarify, refresh, or document the creative and promo context for an artist project before making social posts, reels, lyric videos, visualizers, show recaps, campaign assets, brand kits, merch concepts, bios, captions, or release materials. This skill interviews conversationally, one question at a time, then writes or updates ARTIST.md and DESIGN.md so later Pedalboard skills can sound and look like the artist instead of producing generic marketing output.
allowed-tools: Read Write Edit Glob Grep
---

# Artist Onboarding

Create useful working context for an artist project. This is a taste intake, not a marketing worksheet.

The user may invoke this as:

- `/artist:onboard`
- `/artist:onboard quick`
- `/artist:onboard deep`
- `/artist:onboard from-links`
- `/artist:onboard from-assets`
- `/artist:onboard refresh`

If no mode is clear, default to `quick`.

## Ground Rules

- Ask one question at a time. Never ask the artist to write a whole essay.
- Keep the tone like a smart creative director friend: warm, specific, low-pressure.
- Create working drafts, not final identity doctrine. Mark uncertainty clearly.
- Do not generate lyrics, melodies, chord progressions, or music. Pedalboard helps with non-musical artist work.
- If `ARTIST.md` or `DESIGN.md` already exists, read it first and update it carefully. Preserve useful prior context.
- If the current directory is not the artist's project folder, ask where to write the files before editing.

## Output Files

Write or update these files in the current artist project directory:

- `ARTIST.md`: creative, audience, voice, platform, comfort, materials, and campaign context.
- `DESIGN.md`: visual and motion direction for social/video/merch/campaign assets.

If there is not enough visual evidence for `DESIGN.md`, still write a lightweight draft with `Still Unknown` rather than blocking.

## Intake Flow

Before asking questions, check for existing context:

1. Look for `ARTIST.md`, `DESIGN.md`, `README.md`, `bio.md`, `press.md`, `EPK.md`, or obvious artist/project notes.
2. If context exists, summarize what you found in 2-4 bullets, then ask what should change.
3. If context is missing, begin the interview.

### Quick Mode

Ask 5-8 questions total. Stop once you can draft a useful `ARTIST.md`.

Ask in this order, adapting to answers:

1. Project: "What artist or project are we setting up?"
2. Current moment: "What are you trying to make easier right now: posting, a release, shows, merch, visuals, or general clarity?"
3. Sound and scene: "How would you describe the music, and what scenes or artists does it sit near?"
4. Taste anchors: "Give me 3 references that feel adjacent: artists, films, designers, venues, labels, eras, internet accounts, anything."
5. Anti-references: "What should this absolutely not feel like?"
6. Voice: "How should posts sound: funny, mysterious, earnest, diaristic, blunt, poetic, chaotic, deadpan, something else?"
7. Promo comfort: "What kinds of promo make you cringe, and what feels natural?"
8. Materials and first use: "What do you already have, and what should Pedalboard help make first?"

### Deep Mode

Use quick mode first, then continue only if the artist has energy for more. Explore:

- Audience: who already cares, who should care next, and where they gather.
- Era: release cycle, tour, rebrand, local scene push, recovery/reset, catalog push.
- Story: origin, recurring themes, public mythology, private truths that can safely become public.
- Platforms: Instagram, TikTok, YouTube Shorts, Bandcamp, Spotify, mailing list, Discord, Patreon.
- Visual world: colors, textures, symbols, typography, photo treatment, clothing, locations, objects.
- Assets: songs, lyrics, cover art, logos, live footage, fan clips, press quotes, old captions, show posters.
- Boundaries: subjects, aesthetics, captions, platforms, or tactics to avoid.

### From-Links Mode

Ask for links one at a time or accept a pasted list. Useful links include:

- Artist website, Bandcamp, Spotify, YouTube, SoundCloud.
- Instagram, TikTok, YouTube Shorts.
- Press, interviews, reviews, EPKs, venue pages.

Without browsing tools, ask the user to paste representative text or screenshots. Do not pretend to inspect unavailable links.

### From-Assets Mode

Ask for the folder or file paths containing source material. Look for:

- Cover art, posters, photos, logos.
- Lyrics, bios, press releases, liner notes.
- Live clips, fan footage, rough exports.

Summarize what the files imply before drafting. If media inspection is unavailable, ask for a short description of the assets.

### Refresh Mode

Use when `ARTIST.md` / `DESIGN.md` already exist. Ask:

1. "What changed since this was written?"
2. "What still feels true?"
3. "What feels wrong, stale, or too generic?"
4. "What should the next Pedalboard task be optimized for?"

Then update only the affected sections.

## ARTIST.md Template

Use this structure. Keep it concise and specific.

```md
# ARTIST.md

## Project

- Artist/project:
- Current era:
- Primary goal:
- First Pedalboard use:

## Public Myth

One sentence people could remember.

## Sound And Scene

- Genre language:
- Adjacent artists/scenes:
- Anti-references:

## Audience

- Existing audience:
- Next audience:
- Where they gather:

## Voice

- Should sound like:
- Should not sound like:
- Caption instincts:
- Words/phrases to use:
- Words/phrases to avoid:

## Promo Comfort

- Feels natural:
- Feels cringe:
- Boundaries:

## Materials

- Music:
- Lyrics:
- Visuals:
- Video:
- Press/social proof:
- Links:

## Platforms

- Primary:
- Secondary:
- Avoid or deprioritize:

## Useful Outputs

- Near-term:
- Later:

## Still Unknown

- 
```

## DESIGN.md Template

Use this structure. Do not invent precision the artist has not earned yet.

```md
# DESIGN.md

## Visual Thesis

One sentence for how this artist should look and feel in public.

## References

- Taste anchors:
- Anti-references:

## Palette

- Working colors:
- Avoid:

## Type And Layout

- Typography feel:
- Layout instincts:
- Poster/social treatment:

## Image Treatment

- Photos:
- Video:
- Texture/material:

## Motion

- Lyric video:
- Reels/shorts:
- Visualizers:

## Symbols And Motifs

- 

## Merch And Objects

- 

## Never Do This

- 

## Still Unknown

- 
```

## Drafting Rules

- Use the artist's own phrases when they are vivid.
- Prefer concrete language over genre soup.
- Keep "Still Unknown" honest. It is better to name uncertainty than fake confidence.
- Include a short "Next best Pedalboard task" note after writing the files.
- After writing, report the paths changed and a brief summary of what is now usable.

