# Gravitas

Gives a coding agent a checkable process: read before writing, plan in proportion to risk, verify against a command that actually ran, and report only what that evidence supports. It changes the process, not the model weights. Repo: https://github.com/udaysharmadev/Gravitas. MIT, Uday Sharma. Status on the README: research preview. Comparative performance is not measured, and no solve rates or model rankings are published.

Use this file when the work is running or checking a task under Gravitas. Open it from `C:\Users\ANISH\Documents\ai-playbook\LIBRARY.md` and use only the invariant the task needs. How ANISH wants ordinary work done stays in `C:\Users\ANISH\Documents\ai-playbook\work-standards.md`.

The README’s account of why it exists: in late 2026 Antigravity restricted third-party models, Claude access moved to direct paid subscriptions, and Claude 4.6 models on other plans were set to be removed on 2 November 2026. Gemini 3.8 Flash stays on every plan, Free included. Gravitas does not bring Claude back.

## The six invariants

1. Ground before mutating. Read the target, its tests, and its callers. File state is observed.
2. Stay in declared scope. Each task declares `allowed_write_scope`. Writes outside it are denied. A wrong scope is amended in the open.
3. Completion needs evidence. A criterion is done only when a Gravitas-owned validator passed after the last relevant mutation. An older green run, a self-review, and a prose summary do not count.
4. Never exact-retry a failure. Retry only after the diagnosis, context, or strategy changes. `gravitas resolve-failure` re-arms a fingerprint once a transient cause is resolved.
5. Satisfy the contract. Acceptance criteria and their required validators gate completion. A passing suite for unrelated code proves nothing about the task.
6. Say what you cannot verify. An unbacked claim is labeled. Uncertainty lowers confidence.

Planning records are `direct`, `compact`, `deep`, or `replan`. A one-line fix in one file is `direct`. An auth migration across twelve files is `deep` with a reviewer. Profiles named in the README: `eco`, `balanced`, `deep`, and `team`. None of them claims a speed or quality advantage.

Read-only modes: answer, research, plan, review, security-review. Scoped writes: implement, debug. Migration requires a user checkpoint.

## What is actually enforced

Core is instruction only. That is the recommended default. Native Antigravity adds hooks that can deny a write and block completion. OpenCode adds a permission profile and a `gravitas guard` shim. The failure policy is fail-closed: a broken guard denies mutations. Hooks are workflow controls, not an operating-system sandbox.

Completion-grade evidence is a record from `validator_runner.py`: a declared validator, exit code 0, timestamped after the latest file write, in an intact hash chain. A hash chain makes a silent edit detectable. It does not stop someone who can rewrite the whole ledger. The README says the model assumes filesystem integrity.

## Install

Core, for Antigravity:

```bash
npx skills add udaysharmadev/Gravitas --skill gravitas --agent antigravity --yes
```

Then: “Use Gravitas to fix this bug and verify the result.”

Native: clone the repo, `bash scripts/build-native-bundle.sh`, then `agy plugin install` and `agy plugin validate` on `dist/gravitas-antigravity`.

OpenCode: `gravitas init --host opencode --profile balanced`.

Skill folders in the repo: `gravitas` (the base loop), `gravitas-highstakes` (a stop for schema migrations, deletion, auth, production config, and force-pushes, until the user confirms), `gravitas-python` (load after the base skill), and `gravitas-typescript` (load after the base skill).
