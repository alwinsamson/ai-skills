# ai-skills

A personal collection of AI skill sets for use with Claude Code and other agent frameworks.

Skills follow the [Agent Skills specification](https://agentskills.io/specification) and can be used by any skills-compatible agent.

## Collections

### [obsidian-skills](obsidian-skills/)

Agent skills for working with Obsidian vaults. Forked from [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills).

| Skill | Description |
|---|---|
| [obsidian-markdown](obsidian-skills/obsidian-markdown) | Create and edit Obsidian Flavored Markdown with wikilinks, embeds, callouts, and properties |
| [obsidian-bases](obsidian-skills/obsidian-bases) | Create and edit Obsidian Bases (`.base`) with views, filters, formulas, and summaries |
| [json-canvas](obsidian-skills/json-canvas) | Create and edit JSON Canvas (`.canvas`) files with nodes, edges, groups, and connections |
| [obsidian-cli](obsidian-skills/obsidian-cli) | Interact with Obsidian vaults via the Obsidian CLI, including plugin and theme development |
| [defuddle](obsidian-skills/defuddle) | Extract clean markdown from web pages using Defuddle, removing clutter to save tokens |

### [chrome-cdp-skill](chrome-cdp-skill/)

Agent skill for browser automation via Chrome DevTools Protocol. Forked from [pasky/chrome-cdp-skill](https://github.com/pasky/chrome-cdp-skill).

| Skill | Description |
|---|---|
| [chrome-cdp](chrome-cdp-skill/skills/chrome-cdp) | Control a Chrome browser from AI agents using the CDP protocol |

### [generate-shortcuts-skill](generate-shortcuts-skill/)

Agent skill for generating macOS/iOS Shortcuts as signed `.shortcut` plist files. Forked from [drewocarr/generate-shortcuts-skill](https://github.com/drewocarr/generate-shortcuts-skill).

| Skill | Description |
|---|---|
| [shortcuts-generator](generate-shortcuts-skill/) | Generate macOS/iOS Shortcuts by creating plist files, including actions, variables, and control flow |

### [personal-skills](personal-skills/)

Personal skills not tied to any upstream.

| Skill | Description |
|---|---|
| [yeet](personal-skills/yeet) | Stage, commit, push, and open a GitHub PR in one flow using the GitHub CLI |

## Upstream sync

See [UPSTREAM.md](UPSTREAM.md) for instructions on checking for and applying upstream changes from the tracked upstream sources.
