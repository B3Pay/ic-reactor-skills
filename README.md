# IC Reactor skills have moved

The IC Reactor agent skill now lives in the main repository, next to the code
it describes, and is versioned with each release:

**[B3Pay/ic-reactor → `skill-packages/ic-reactor`](https://github.com/B3Pay/ic-reactor/tree/main/skill-packages/ic-reactor)**

It replaces the `ic-reactor-hooks` skill that used to live here. That skill
was written for contributors to the IC Reactor repository and pointed at its
source paths; the new `ic-reactor` skill is written for apps that install
`@ic-reactor/*` and uses only public APIs. This repository is no longer
updated.

## Install the current skill

### Claude Code

The main repository is a Claude Code plugin marketplace:

```text
/plugin marketplace add B3Pay/ic-reactor
/plugin install ic-reactor@ic-reactor
```

### Other agents (Codex, Cursor, Copilot, Gemini CLI, OpenCode, ...)

With the [`skills`](https://github.com/vercel-labs/skills) CLI, from your
app's root:

```bash
npx skills add B3Pay/ic-reactor --skill ic-reactor
```

### Agents without skill support

Point your agent at the guides IC Reactor publishes:

- `node_modules/@ic-reactor/<package>/llms.txt`: the guide for the version
  your app has installed
- https://ic-reactor.b3pay.net/llms.txt: index of the docs
- https://ic-reactor.b3pay.net/llms-full.txt: the complete guide

## If you installed `ic-reactor-hooks` from here

Remove it and install `ic-reactor` as shown above, or delete the
`ic-reactor-hooks` folder from your agent's skills directory (for example
`.claude/skills/ic-reactor-hooks/`). The `ic-reactor-hooks` folder in this
repository is now a stub that sends an agent to the new skill and the
published guides, so an old install still leads somewhere current.

## License

MIT (skill content). IC Reactor logo/icon remains subject to the IC Reactor
project licensing and branding terms.
