---
name: ic-reactor-hooks
description: Moved. The IC Reactor skill is now `ic-reactor` in the B3Pay/ic-reactor repository. Use this stub when working with @ic-reactor/react, @ic-reactor/core, createActorHooks, defineReactor, createQuery/createMutation, useActorMethod or IC Reactor codegen, to find the maintained skill and the guides for the installed version.
---

# IC Reactor Hooks (moved)

This skill is retired. Its guidance was written against an older IC Reactor
and for contributors to the IC Reactor repository, so do not rely on it for
API details.

## Do this instead

1. Read the guide that ships with the installed package, which matches the
   version the app uses:
   - `node_modules/@ic-reactor/react/llms.txt` (React apps)
   - `node_modules/@ic-reactor/core/llms.txt` (framework-agnostic code)
   - `node_modules/@ic-reactor/<package>/llms.txt` for candid, codegen, cli,
     vite-plugin or parser
2. For the complete guide, read https://ic-reactor.b3pay.net/llms-full.txt;
   for an index of the docs, https://ic-reactor.b3pay.net/llms.txt.
3. Tell the user that this skill has been replaced by the `ic-reactor` skill
   and how to install it:
   - Claude Code: `/plugin marketplace add B3Pay/ic-reactor`, then
     `/plugin install ic-reactor@ic-reactor`
   - Other agents: `npx skills add B3Pay/ic-reactor --skill ic-reactor`
   - Then remove this `ic-reactor-hooks` skill.

The maintained skill lives at
https://github.com/B3Pay/ic-reactor/tree/main/skill-packages/ic-reactor.
