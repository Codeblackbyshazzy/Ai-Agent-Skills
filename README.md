<h1 align="center">
  <br>
  🔧 AI Agent Skills
  <br>
</h1>

<p align="center">
  <strong>There are a lot of agent skills now. These are the ones I keep around.</strong><br>
  Some are mine. Some come from other great repos.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/skills-41-blue?style=flat-square" alt="Skills" />
  <img src="https://img.shields.io/badge/agents-11+-green?style=flat-square" alt="Compatible Agents" />
  <img src="https://img.shields.io/npm/v/ai-agent-skills?style=flat-square&color=red" alt="npm" />
  <img src="https://img.shields.io/npm/dt/ai-agent-skills?style=flat-square&color=orange" alt="Downloads" />
</p>

<p align="center">
  <a href="#quick-start"><strong>Quick Start</strong></a> ·
  <a href="#collections"><strong>Collections</strong></a> ·
  <a href="./CURATION.md"><strong>Curation Guide</strong></a> ·
  <a href="./CONTRIBUTING.md"><strong>Contribute</strong></a> ·
  <a href="https://agentskills.io"><strong>Specification</strong></a>
</p>

---

## What This Is

I launched this on December 17, 2025, the day after Agent Skills became an open standard, and before `skills.sh` launched on January 14, 2026.

I built it as a universal installer. That still works, but it is not the center of the project. 

If you just want the default universal installer now just use `skills.sh`.

This repo is my library of agent skills: the ones I use, adapt, or recommend.

## Quick Start

```bash
# Install one skill to all supported agents
npx ai-agent-skills install frontend-design

# Install to a specific agent only
npx ai-agent-skills install frontend-design --agent cursor

# Browse curated collections
npx ai-agent-skills collections

# See my starter set
npx ai-agent-skills list --collection my-picks

# Search the catalog
npx ai-agent-skills search testing
```

By default, `install` targets the major agents I already support: Claude Code, Cursor, Codex, Amp, VS Code, Copilot, Gemini CLI, Goose, Letta, Kilo Code, and OpenCode.

## How I Organize It

- `Collections` are the first place I would tell someone to browse.
- `My Picks` is where I would tell most people to start.
- A few skills are authored here. Most are curated from upstream repos and kept clearly attributed.
- `Source` stays attached to every skill. The library matters, but so does provenance.
- `Featured` means I would actively point someone to that skill first.
- `Verified` means I have personally checked the skill and its metadata.
- `Categories`, `tags`, and search cover everything that does not need a top-level shelf.

The folder layout stays flat under `skills/<name>/` because installs stay simpler that way. The catalog handles the grouping.

## Collections

Start here. They are the front shelf, not the whole catalog.

| Collection | What it's for | Start with | Main sources |
|-------|-------------|-------------|--------------|
| `my-picks` | The first skills I would install on a fresh setup | `frontend-design`, `mcp-builder`, `qa-regression` | Anthropic, Moiz |
| `build-apps` | Web product work with a high interface bar | `frontend-design`, `artifacts-builder`, `theme-factory` | Anthropic, Composio |
| `build-systems` | Backend, architecture, MCP, and deeper engineering work | `mcp-builder`, `backend-development`, `database-design` | wshobson, Anthropic |
| `test-and-debug` | Review, QA, debugging, and cleanup work | `qa-regression`, `code-review`, `webapp-testing` | Moiz, Anthropic |
| `docs-and-research` | Docs, files, research, and execution support | `pdf`, `doc-coauthoring`, `code-documentation` | Anthropic, Composio |

CLI shortcuts:

```bash
npx ai-agent-skills collections
npx ai-agent-skills list --collection my-picks
npx ai-agent-skills list --collection build-apps
npx ai-agent-skills search expo
```

## Source Repos

This is still my library, but the upstream lineage stays visible on purpose.

| Source repo | Why it's here | In this library |
|------------|----------------|-----------------|
| [Anthropic Skills](https://github.com/anthropics/skills) | The strongest general-purpose skill set in the ecosystem, especially for frontend, docs, and workflow. | 13 skills |
| [Anthropic Claude Code](https://github.com/anthropics/claude-code) | Extra Claude Code workflow coverage that belongs here when it clears the bar. | 1 skill |
| [wshobson/agents](https://github.com/wshobson/agents) | Strong backend, systems, and architecture coverage. | 7 skills |
| [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) | Broad practical coverage for workflow, files, research, and creative tasks. | 15 skills |
| [MoizIbnYousaf/Ai-Agent-Skills](https://github.com/MoizIbnYousaf/Ai-Agent-Skills) | The skills I write and maintain directly. | 5 skills |

## Supported Agents

| Agent | Flag | Install Location |
|-------|------|------------------|
| Claude Code | `--agent claude` | `~/.claude/skills/` |
| Cursor | `--agent cursor` | `.cursor/skills/` |
| Codex | `--agent codex` | `~/.codex/skills/` |
| Amp | `--agent amp` | `~/.amp/skills/` |
| VS Code / Copilot | `--agent vscode` | `.github/skills/` |
| Gemini CLI | `--agent gemini` | `~/.gemini/skills/` |
| Goose | `--agent goose` | `~/.config/goose/skills/` |
| OpenCode | `--agent opencode` | `~/.opencode/skill/` |
| Letta | `--agent letta` | `~/.letta/skills/` |
| Kilo Code | `--agent kilocode` | `~/.kilocode/skills/` |
| Portable | `--agent project` | `.skills/` |

## Commands

```bash
# Discovery
npx ai-agent-skills collections
npx ai-agent-skills list
npx ai-agent-skills list --category development
npx ai-agent-skills list --collection my-picks
npx ai-agent-skills search testing
npx ai-agent-skills info frontend-design

# Installation
npx ai-agent-skills install <name>
npx ai-agent-skills install <name> --agent cursor
npx ai-agent-skills install <owner/repo>
npx ai-agent-skills install <git-url>
npx ai-agent-skills install ./path
npx ai-agent-skills install <name> --dry-run

# Management
npx ai-agent-skills uninstall <name>
npx ai-agent-skills update <name>
npx ai-agent-skills update --all

# Configuration
npx ai-agent-skills config --default-agent cursor
```

## Manual Install

```bash
git clone https://github.com/MoizIbnYousaf/Ai-Agent-Skills.git
cp -r Ai-Agent-Skills/skills/pdf ~/.claude/skills/
```

## Contributing

This repo is curated. I do not accept everything, and I do not want the catalog to sprawl.
I would rather keep it small and strong than let it get messy.

Before opening a PR:

1. Read [CURATION.md](./CURATION.md).
2. Follow [CONTRIBUTING.md](./CONTRIBUTING.md).
3. Add or update the `skills.json` entry.
4. Put the skill on a top-level shelf only if it clearly belongs there.
5. Explain why it belongs here.

## What Are Agent Skills?

Agent skills follow the open format documented at [agentskills.io](https://agentskills.io). A skill is just a folder:

```text
my-skill/
├── SKILL.md
├── scripts/
└── references/
```

All major coding agents support some variation of this pattern.

## Links

- [Agent Skills Spec](https://agentskills.io)
- [Anthropic Skills](https://github.com/anthropics/skills)
- [Curation Guide](./CURATION.md)
- [Contributing Guide](./CONTRIBUTING.md)
- [Issues](https://github.com/MoizIbnYousaf/Ai-Agent-Skills/issues)

## Credits & Attribution

This library builds on work from the open-source community, especially:

- [Anthropic Skills](https://github.com/anthropics/skills)
- [Anthropic Claude Code](https://github.com/anthropics/claude-code)
- [ComposioHQ Awesome Claude Skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [wshobson/agents](https://github.com/wshobson/agents)

If something here traces back to your work and you want clearer attribution, open an issue.

---

<p align="center">
  <sub>Built and curated by <a href="https://github.com/MoizIbnYousaf">Moiz Ibn Yousaf</a></sub>
</p>
