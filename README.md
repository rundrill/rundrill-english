# RunDrill English

Your personal **English coach** inside your AI agent — short targeted drills, an honest picture of
your level (A1–C2), and mistake memory that resurfaces what you got wrong. The skill is the voice;
your level, weak topics, vocabulary, and goal live on the RunDrill MCP server (`mcp.rundrill.com`),
synced across machines — not in a local file.

Built for **Russian- and Kazakh-speaking learners**: the coach explains in your native language and
moves toward English as your level rises (comprehensible input, i+1), and drills the things English
actually turns on — tenses, articles, prepositions, conditionals.

## One plugin, three hosts

The coaching skill (`skills/english-coach/SKILL.md`) and `.mcp.json` are shared; each host reads its
own manifest and ignores the rest.

| Host | Reads |
|---|---|
| Claude Code / Claude Desktop | `.claude-plugin/plugin.json` + `.mcp.json` |
| OpenAI Codex | `.codex-plugin/plugin.json` + `.mcp.json` |
| Google Antigravity | `plugin.json` + `mcp_config.json` (+ `rules/`) |

On first use the host opens a browser tab for the OAuth handshake with `mcp.rundrill.com`, then
closes it — no API key to paste.

## Install

- **Claude Code / Desktop** — via the RunDrill marketplace:
  ```
  /plugin marketplace add rundrill/marketplace
  /plugin install rundrill-english@rundrill
  ```
  Then run `/english-coach`.
- **OpenAI Codex** — add the RunDrill catalog, then install `rundrill-english` from the plugin directory:
  ```
  codex plugin marketplace add rundrill/marketplace
  ```
- **Google Antigravity** — drop this folder into `~/.gemini/config/plugins/rundrill-english/` (global)
  or `<workspace>/.agents/plugins/rundrill-english/` (workspace-scoped).

## License & attribution

© RunDrill. Licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0
International (CC BY-NC-ND 4.0)** — full text in [LICENSE](LICENSE).

In short, you **may** view, run, and share this plugin unchanged, for non-commercial purposes, **as
long as you give credit**. You **may not**:

- use it, or any part of it (including the coaching skill), **commercially**;
- publish **modified or derivative** versions (forks, ports, translations, reworded skills).

Required attribution when sharing: *“RunDrill English coach — © RunDrill, CC BY-NC-ND 4.0,
https://rundrill.com”.*

For commercial use, derivatives, or any license beyond CC BY-NC-ND 4.0, contact
**hello@rundrill.com**.
