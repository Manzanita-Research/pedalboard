# Pedalboard

Open source Claude Cowork & Claude Code plugins for independent musicians. Built by [Manzanita Research](https://github.com/manzanita-research).

Musicians shouldn't need a label's budget to make smart decisions about their careers. Pedalboard is a collection of plugins that handle the tedious research so you can focus on the music.

## Install

### Claude Code

```sh
claude plugin marketplace add manzanita-research/pedalboard
claude plugin install branding@pedalboard
```

### Claude Cowork

1. Open the **+** menu
2. **Add plugin** → **Browse Plugins**
3. Go to the **Personal** tab
4. Click **+** → **Add marketplace from GitHub**
5. Enter `manzanita-research/pedalboard`

Once installed, Pedalboard's skills are available in any session.

## Available Plugins

Pedalboard is separated into several modules representing the many "hats" that independent musicians wear, and they can be installed separately.

| Plugin       | What it does                                                            | Status      |
| ------------ | ----------------------------------------------------------------------- | ----------- |
| **booking**  | Venue research and booking tools                                        | Coming soon |
| **branding** | Check if your stage name is taken across streaming and social platforms | Active      |
| **press**    | EPK generator, press releases, and one-sheets                           | Coming soon |
| **legal**    | Split sheets and legal guidance                                         | Coming soon |

### Branding

### name-check

Checks if an artist name is already taken across Spotify, Apple Music, YouTube Music, Bandcamp, SoundCloud, Discogs, MusicBrainz, TikTok, Subvert, and Tidal.

**Use it:**

```
/branding:name-check King Dream
```

Or just ask naturally:

```
Is the stage name "Midnight Phantom" taken?
```

```
Check if anyone is using the name "Luna Verde" on streaming platforms
```

## Contributing

Pedalboard is open source. If you want to add a skill or improve an existing one, PRs are welcome at [github.com/manzanita-research/pedalboard](https://github.com/manzanita-research/pedalboard). Preferably use Anthropic's [`skill-creator`](https://github.com/anthropics/skills/tree/main/skills/skill-creator) skill.

Pedalboard is targeted to optimizing and automating the non-musical tasks that independent artists have to do (or pay other people to do). Contributions relating to using AI for music _generation_ will be rejected.

## License

MIT

_🌅 With love from California_
