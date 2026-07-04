---
name: flintslabs-delivery-check
description: Use before finalizing coding, documentation, plugin, or repository changes for FlintsLabs work. Verify git status, changed files, tests or validation, pushed state when applicable, and produce a concise delivery summary with explicit verification gaps.
---

# FlintsLabs Delivery Check

## Overview

Run a final delivery pass before reporting work as complete. The goal is to prevent vague summaries, missed dirty files, and unverified claims.

## Workflow

1. Check `git status -sb` and identify changed, staged, untracked, and pushed files.
2. Review the final diff or relevant file snippets before summarizing.
3. Run the most relevant validation available for the change scope.
4. If validation cannot run, state the exact blocker or skipped check.
5. If a remote push was requested, verify the remote branch or repository state.
6. Summarize only what changed, where it changed, and what passed.
7. Call out residual risk or follow-up commands when useful.

## Output Shape

Keep the final answer short and concrete:

- Changed files or repo path.
- Version, commit, PR, or pushed branch when relevant.
- Validation commands and results.
- Any verification gap.

## Guardrails

- Do not say tests passed unless they actually ran.
- Do not hide unrelated dirty changes.
- Do not over-explain small changes.
- Prefer paths, commands, versions, and commit hashes over generic status language.
