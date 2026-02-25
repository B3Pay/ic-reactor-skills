# IC Reactor Hooks Skill (ICP)

Codex/agent skill for building and refactoring `@ic-reactor/react` integrations in Internet Computer (ICP) projects.

This skill helps AI agents generate correct IC Reactor code for:

- `createActorHooks(...)`
- `createQuery` / `createMutation` factory modules
- `useActorMethod`
- TanStack Query cache invalidation
- generated hooks from `@ic-reactor/cli` and `@ic-reactor/vite-plugin`
- usage inside React components vs imperative usage outside React (`fetch`, `execute`, `invalidate`)

## Skill Files

- `SKILL.md` — skill instructions + trigger description
- `agents/openai.yaml` — store/listing metadata (name, description, icons, default prompt)
- `references/patterns.md` — concrete IC Reactor patterns and examples
- `assets/ic-reactor-icon.svg` — icon for store UIs

## Install (Repo Path)

Use your skill installer to install from this GitHub repository path.

Example prompt for an agent with a skill installer:

```text
Install the skill from github.com/B3Pay/ic-reactor-hooks-skill
```

## Use the Skill

Example usage:

```text
Use $ic-reactor-hooks-skill to build a reusable query/mutation factory pair for my canister and show usage inside a React component and in a route loader.
```

## Validation (Local)

The validator used by the Skill Creator requires `PyYAML`.

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -U pip pyyaml
python /Users/behraddeylami/.codex/skills/.system/skill-creator/scripts/quick_validate.py .
```

## Store / Catalog Submission Checklist

- [x] `SKILL.md` at repo root
- [x] `agents/openai.yaml` with display metadata
- [x] icon assets included
- [x] trigger-rich `description` in `SKILL.md` frontmatter
- [x] default prompt mentions `$ic-reactor-hooks-skill`
- [ ] submit this repo to the curated skills catalog/store process (platform-specific)

## License

MIT (skill content). IC Reactor logo/icon remains subject to the IC Reactor project licensing and branding terms.
