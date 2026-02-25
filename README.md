# IC Reactor Hooks Skill (ICP)

Codex/agent skill for building and refactoring `@ic-reactor/react` integrations in Internet Computer (ICP) projects.

This skill helps AI agents generate correct IC Reactor code for:

- `createActorHooks(...)`
- `createQuery` / `createMutation` factory modules
- `useActorMethod`
- TanStack Query cache invalidation
- generated hooks from `@ic-reactor/cli` and `@ic-reactor/vite-plugin`
- usage inside React components vs imperative usage outside React (`fetch`, `execute`, `invalidate`)

## Skill Location

This repository keeps the skill in a subfolder so the repository name can remain `ic-reactor-hooks-skill` while the installed skill name stays short:

- `ic-reactor-hooks/` (skill folder)

## Skill Files

- `ic-reactor-hooks/SKILL.md` — skill instructions + trigger description
- `ic-reactor-hooks/agents/openai.yaml` — store/listing metadata
- `ic-reactor-hooks/references/patterns.md` — concrete IC Reactor patterns and examples
- `ic-reactor-hooks/assets/ic-reactor-icon.svg` — icon for store UIs

## Install (Repo Path)

Use your skill installer to install from the `ic-reactor-hooks/` subfolder in this GitHub repository.

Example prompt for an agent with a skill installer:

```text
Install the skill from github.com/B3Pay/ic-reactor-hooks-skill path ic-reactor-hooks
```

For the `skills` CLI (multi-skill repo scan), use nested discovery and select the skill:

```bash
npx skills add B3Pay/ic-reactor-hooks-skill --full-depth --skill ic-reactor-hooks
```

## Use the Skill

Example usage:

```text
Use $ic-reactor-hooks to build a reusable query/mutation factory pair for my canister and show usage inside a React component and in a route loader.
```

## Validation (Local)

The validator used by the Skill Creator requires `PyYAML`.

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -U pip pyyaml
python /Users/behraddeylami/.codex/skills/.system/skill-creator/scripts/quick_validate.py ./ic-reactor-hooks
```

## Store / Catalog Submission Checklist

- [x] `ic-reactor-hooks/SKILL.md` present
- [x] `ic-reactor-hooks/agents/openai.yaml` with display metadata
- [x] icon assets included
- [x] trigger-rich `description` in `SKILL.md` frontmatter
- [x] default prompt mentions `$ic-reactor-hooks`
- [x] skill folder name matches skill name (`ic-reactor-hooks`)
- [ ] submit this repo to the curated skills catalog/store process (platform-specific)

## License

MIT (skill content). IC Reactor logo/icon remains subject to the IC Reactor project licensing and branding terms.
