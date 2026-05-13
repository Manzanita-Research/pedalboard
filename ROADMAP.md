# Roadmap

## What this is

An open-source collection of Claude Code plugins for independent musicians. Each plugin covers a "hat" musicians wear, with a current emphasis on social video, promo, artist worldbuilding, and campaign materials rather than label-style back office work.

Every skill must save a musician real time on a task they'd otherwise do by hand (or skip entirely because it's too much work). If Claude already handles it well without a skill, it doesn't ship.

## Done

- [x] **Branding plugin** — stage name availability checking across music platforms (Spotify, Apple Music, Tidal, Bandcamp, SoundCloud, Discogs, MusicBrainz). Working, installed, auto-triggers.
- [x] **Artist plugin** — guided onboarding that creates `ARTIST.md` and `DESIGN.md` context for promo, video, and campaign skills.

## Open

- [ ] **Parallelize name-check searches** — the web search agent makes 12+ sequential calls. Split into parallel platform-group agents to cut search time. (`branding/skills/name-check/`)
- [ ] **Validate artist onboarding** — run `artist:onboard` against 2-3 real or fictional artist projects and tighten the question flow.

## Future plugin ideas

These need validation before building. The question for each: does a skill meaningfully outperform Claude's baseline?

- **Promo** — reel hooks, show recaps, fan-footage prompts, captions, trend translation, and release content calendars.
- **Video** — HyperFrames / Remotion workflows for lyric videos, visualizers, tour-poster motion, and social ad cutdowns.
- **Artist** — onboarding, artist-world refreshes, visual system capture, and context-file maintenance.
- **Press** — EPK / one-sheet generator with interview-style conversation and audience-specific variants (venue, press, label)
- **Booking** — venue research outputting structured data (capacity, genre fit, booking contact) for import into Notion. User has an existing I-5 corridor venue database as the UX target.
- **Legal** — contract red flags, sample clearance workflows, sync licensing. Split sheets tested and rejected (Claude handles them well natively).

## Principles

- **Instruments, not automations.** Help with the business side, never replace the art.
- **No AI music generation.** Songwriting skills may offer reflection (feedback, meter analysis) but never generation.
- **Taste context first.** Promo and video skills should read `ARTIST.md` and `DESIGN.md` before producing public-facing assets.
- **Ask, then draft.** Onboarding should ask focused questions one at a time, not make artists fill out a giant worksheet.
- **Public APIs only.** No paid API keys required to use any skill.
- **Plugin marketplace compatible.** Follows Anthropic's `.claude-plugin/plugin.json` manifest pattern.
- **Use skill-creator for all skills.** Draft, eval, iterate, optimize description. If the baseline is good enough, don't ship a skill.

## Out of scope

- Lyric writing / ghostwriting
- Paid API integrations
- Mobile app or web UI
- Label/manager workflows — built for the artist
