---
name: flintslabs-debug
description: Use when debugging a real codebase, service behavior, integration issue, or production-like failure. Gather evidence from code, logs, data, and commands before proposing fixes.
---

# FlintsLabs Debug

## Workflow

1. Establish the exact failing behavior, environment, and expected behavior.
2. Read the relevant code path before proposing a fix.
3. Inspect logs, data, API responses, or command output when available.
4. Identify the root cause and separate confirmed facts from assumptions.
5. Make the smallest scoped fix that addresses the cause.
6. Verify with the most relevant build, test, smoke check, or reproduced scenario.
7. Report changed files, verification results, and any remaining verification gaps.

## Guardrails

- Do not revert unrelated dirty changes.
- Do not claim a root cause without evidence.
- Prefer concrete file paths, commands, and observed output over broad advice.
