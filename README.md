# FlintsLabs Codex Marketplace

Shared Codex plugin marketplace for FlintsLabs skills.

## Structure

```text
.agents/plugins/marketplace.json
plugins/
  flintslabs-skills/
    .codex-plugin/plugin.json
    skills/
```

## Install

```bash
codex plugin marketplace add FlintsLabs/codex-marketplace --ref main
codex plugin add flintslabs-skills@flintslabs
```

Open a new Codex thread after installing so newly installed skills are loaded.

## Update On Another Machine

```bash
codex plugin marketplace upgrade flintslabs
codex plugin add flintslabs-skills@flintslabs
```

Open a new Codex thread after updating.

## Add A Skill

Create a folder under `plugins/flintslabs-skills/skills/<skill-name>/` with a `SKILL.md` file:

```markdown
---
name: skill-name
description: Use when ...
---

# Skill Name

## Workflow

1. ...
```

Keep skill names lowercase kebab-case and write descriptions that clearly describe when Codex should use the skill.
