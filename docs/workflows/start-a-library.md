# Start a Library

Use this when you want your own managed library instead of only browsing mine.

```bash
npx ai-agent-skills init-library my-library
cd my-library
```

That creates:

- `skills.json`
- `README.md`
- `WORK_AREAS.md`
- `skills/`
- `.ai-agent-skills/config.json`

The workspace starts small on purpose:

- `frontend`
- `backend`
- `workflow`

From there:

```bash
npx ai-agent-skills add frontend-design --area frontend --branch Implementation --why "I want this on my shelf."
npx ai-agent-skills build-docs
```

Use `list`, `search`, `collections`, and `browse` from inside the workspace when you want the CLI and TUI to read your library instead of the bundled one.
