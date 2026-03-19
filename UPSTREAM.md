# Upstream Sync

This repo wraps three upstream skill collections in named subfolders. A plain `git pull` won't work cleanly against any upstream because their directory layouts differ from ours. Instead, use `git fetch` to preview changes, then copy files manually.

## Git remotes

| Remote | URL | Local path |
|---|---|---|
| `obsidian-skills` | https://github.com/kepano/obsidian-skills.git | `obsidian-skills/` |
| `chrome-cdp-skill` | https://github.com/pasky/chrome-cdp-skill.git | `chrome-cdp-skill/` |
| `generate-shortcuts-skill` | https://github.com/drewocarr/generate-shortcuts-skill.git | `generate-shortcuts-skill/` |

## Skills inventory

### obsidian-skills/

| Skill | Description |
|---|---|
| `obsidian-markdown` | Create and edit Obsidian Flavored Markdown with wikilinks, embeds, callouts, and properties |
| `obsidian-bases` | Create and edit Obsidian Bases (`.base`) with views, filters, formulas, and summaries |
| `json-canvas` | Create and edit JSON Canvas (`.canvas`) files with nodes, edges, groups, and connections |
| `obsidian-cli` | Interact with Obsidian vaults via the Obsidian CLI, including plugin and theme development |
| `defuddle` | Extract clean markdown from web pages using Defuddle, removing clutter to save tokens |

### chrome-cdp-skill/

| Skill | Description |
|---|---|
| `chrome-cdp` | Control a Chrome browser from AI agents using the Chrome DevTools Protocol |

### generate-shortcuts-skill/

| Skill | Description |
|---|---|
| `shortcuts-generator` | Generate macOS/iOS Shortcuts by creating plist files, including actions, variables, and control flow |

---

## Checking for upstream changes

### obsidian-skills

```bash
git fetch obsidian-skills
# Their skills live under /skills/ — diff against that path
git diff obsidian-skills/main -- skills/
```

### chrome-cdp-skill

```bash
git fetch chrome-cdp-skill
git diff chrome-cdp-skill/main
```

### generate-shortcuts-skill

```bash
git fetch generate-shortcuts-skill
git diff generate-shortcuts-skill/main
```

---

## Updating obsidian-skills

```bash
git clone --depth=1 https://github.com/kepano/obsidian-skills /tmp/obs-update
cp -r /tmp/obs-update/skills/. obsidian-skills/
rm -rf /tmp/obs-update
git add obsidian-skills/
git commit -m "chore: sync obsidian-skills from upstream"
```

> Note: their skills live under `/skills/` — we copy that into our `obsidian-skills/`. Don't overwrite `obsidian-skills/.claude-plugin/`.

## Updating chrome-cdp-skill

```bash
git clone --depth=1 https://github.com/pasky/chrome-cdp-skill /tmp/cdp-update
cp -r /tmp/cdp-update/. chrome-cdp-skill/
rm -rf chrome-cdp-skill/.git
rm -rf /tmp/cdp-update
git add chrome-cdp-skill/
git commit -m "chore: sync chrome-cdp-skill from upstream"
```

## Updating generate-shortcuts-skill

```bash
git clone --depth=1 https://github.com/drewocarr/generate-shortcuts-skill /tmp/shortcuts-update
cp -r /tmp/shortcuts-update/. generate-shortcuts-skill/
rm -rf generate-shortcuts-skill/.git
rm -rf /tmp/shortcuts-update
git add generate-shortcuts-skill/
git commit -m "chore: sync generate-shortcuts-skill from upstream"
```
