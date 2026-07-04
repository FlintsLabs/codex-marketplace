---
name: flintslabs-skill-authoring
description: Use when creating or updating skills inside the FlintsLabs Codex marketplace. Keep skills small, triggerable, and easy to share across machines.
---

# FlintsLabs Skill Authoring

## Workflow

1. Decide whether the behavior belongs in an existing skill or a new skill.
2. Use lowercase kebab-case for skill folder names and frontmatter `name`.
3. Write a frontmatter `description` that says exactly when Codex should use the skill.
4. Keep the skill focused on workflow, decision rules, required evidence, and output expectations.
5. Put long examples or reusable prompts in sibling reference files and link to them from `SKILL.md`.
6. Avoid secrets, machine-specific absolute paths, and private credentials in committed skills.
7. Validate by installing the plugin and opening a new Codex thread.

## Recommended Shape

```text
plugins/flintslabs-skills/skills/<skill-name>/
  SKILL.md
  references/
```
