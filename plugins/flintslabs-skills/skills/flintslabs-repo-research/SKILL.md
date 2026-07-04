---
name: flintslabs-repo-research
description: Use when asked to study, compare, or review a repository or GitHub project. Clone or use the existing checkout, inspect real files, and keep analysis read-only unless edits are explicitly requested.
---

# FlintsLabs Repo Research

## Workflow

1. Clone the repository into an appropriate workspace or use an existing checkout when present.
2. Read primary files first: `README`, manifests, configuration, source entry points, tests, and CI.
3. Analyze separate dimensions clearly: purpose, architecture, code quality, security/risk, dependency/tooling, and verification.
4. Prefer `rg`, `find`, `git log`, and targeted file reads over broad speculation.
5. Keep the work read-only for analysis requests.
6. Summarize findings with paths, commands, and evidence.

## Output

- Keep the answer concise.
- Lead with practical conclusions.
- Call out unknowns or verification gaps explicitly.
