---
name: flintslabs-codex-marketplace
description: Use when creating, updating, validating, publishing, installing, or troubleshooting the FlintsLabs Codex marketplace or the flintslabs-skills plugin. Applies to marketplace.json, plugin.json, SKILL.md files, version bumps, Codex plugin add/upgrade flows, and cross-machine skill sharing.
---

# FlintsLabs Codex Marketplace

## Overview

Maintain the FlintsLabs Codex marketplace as a shareable Git-backed plugin source. Keep marketplace metadata, plugin versions, skill files, and install instructions consistent.

## Workflow

1. Inspect the current repo state with `git status -sb` before editing.
2. Keep marketplace metadata in `.agents/plugins/marketplace.json`.
3. Keep plugin metadata in `plugins/flintslabs-skills/.codex-plugin/plugin.json`.
4. Put reusable workflows under `plugins/flintslabs-skills/skills/<skill-name>/SKILL.md`.
5. Use lowercase kebab-case for skill folder names and frontmatter `name`.
6. Bump `plugin.json` `version` for every skill change that should be picked up by other machines.
7. Validate the changed skill folders and the plugin manifest before pushing.
8. Commit and push the marketplace repo.
9. Tell users to run `codex plugin marketplace upgrade flintslabs` and `codex plugin add flintslabs-skills@flintslabs`, then open a new thread.

## Install And Update Commands

Initial install:

```bash
codex plugin marketplace add FlintsLabs/codex-marketplace --ref main
codex plugin add flintslabs-skills@flintslabs
```

After a pushed update:

```bash
codex plugin marketplace upgrade flintslabs
codex plugin add flintslabs-skills@flintslabs
```

## Guardrails

- Do not commit secrets, tokens, private credentials, or machine-specific absolute paths.
- Do not edit installed cache copies under `~/.codex/plugins/cache`; edit the Git repo source.
- Do not use sparse checkout without including `.agents/plugins/marketplace.json`.
- Prefer small skill updates with clear trigger descriptions over broad catch-all instructions.
