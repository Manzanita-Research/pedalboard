# Pedalboard: Musician Plugins

This is a marketplace of Claude Cowork & Claude Code plugins for independent musicians. Each subdirectory is a standalone plugin.

## Repository Structure

```
├── branding/  # Branding productivity
```

## Plugin Structure

Each plugin follows this layout:

```
plugin-name/
├── .claude-plugin/plugin.json   # Plugin manifest (name, description, version)
├── commands/                    # Slash commands (.md files)
├── skills/                      # Knowledge files for specific tasks
├── hooks/                       # Event-driven automation
├── mcp/                         # MCP server integrations
└── .claude/                     # User settings (*.local.md)
```

## Key Files

- `marketplace.json`: Marketplace manifest - registers all plugins with source paths
- `plugin.json`: Plugin metadata - name, description, version, and component discovery settings
- `commands/*.md`: Slash commands invoked as `/plugin:command-name`
- `skills/*/SKILL.md`: Detailed knowledge and workflows for specific tasks
- `*.local.md`: User-specific configuration (gitignored)
- `mcp-categories.json`: Canonical MCP category definitions shared across plugins

## Development Workflow

Where possible, use [`skill-creator`](https://github.com/anthropics/skills/tree/main/skills/skill-creator) to create, update & optimize skills.

1. Edit markdown files directly - changes take effect immediately
2. Test commands with `/plugin:command-name` syntax
3. Skills are invoked automatically when their trigger conditions match

## Conventions

- Keep the [Available Plugins](https://github.com/Manzanita-Research/pedalboard?tab=readme-ov-file#available-plugins) section in the README up to date, with plugins available
