---
name: hab-self-coding
description: Convert an approved software goal into staged plans, isolated implementation, tests, and a human-reviewed path to main. Use for agent coding and self-improvement workflows; never grant direct main-branch, deployment, provider-spend, or secret authority.
---

# Hab controlled self-coding

## Goal and boundary

Automate the repetitive parts of building software while preserving owner
judgment, project history, secrets and production control. First inspect the
actual project, its instructions, current revision, open changes and task
dependencies. Never assume the current conversation workspace is the target
project. Continue existing work rather than overwriting it.

## Three working lanes

1. **Draft-only:** inspect and propose design, file list, patch outline, tests,
   cost/privacy impacts, acceptance criteria and rollback. Make no project-file
   writes until the authorized workflow approves implementation.
2. **Creative sandbox branch:** when the task owner permits implementation,
   explore broader alternatives in an isolated branch forked from the selected
   main revision (for example `creative/<task>`). Use synthetic fixtures and
   preserve the baseline. Label exploratory shortcuts, incomplete tests and
   discarded ideas. This branch is not release-ready and never pushes to or
   edits `main`.
3. **Implementation branch:** create a separate narrow branch from the recorded
   clean base (for example `task/<task>`). Move only the selected, reviewed
   design into production-quality code. Keep diffs small, write tests and
   documentation, run existing checks and compare the final diff to the base.
   Keep unrelated changes and other active branches untouched.

## Path to main

The default branch remains protected. The agent does not make direct main
commits, force-push, bypass required checks, approve its own changes, auto-merge,
or deploy. After tests and human code review, prepare a draft pull request to
main with changed paths, evidence, risks, disabled behavior, migration/rollback
instructions and unresolved questions. A human maintainer must explicitly
approve the merge. Deployment and post-deploy validation are separate gates.

## Execution contract

- Interpret run-on requests into goal, scope, assumptions and exclusions;
  ask only when an ambiguity changes cost, private data, financial behavior,
  permissions, irreversible operations or release destination.
- Use the smallest relevant skills and existing project utilities. Reuse
  existing dependencies; don't build a second storage/archive/provider engine.
- Separate planning, coding, testing, review, pull-request publication, merge,
  secrets configuration and deployment. Approval of a code task does not grant
  every later action.
- Tests use deterministic local fixtures and mocked network/provider boundaries
  by default. No actual paid API calls, model fan-out, key provisioning or
  license bypass while coding. Respect project/account limits.
- Secrets and wallet signing material stay in the approved server-side secrets
  manager. Never hard-code them, expose them to browser bundles, prompts,
  logs, test output, skill files or exported archives.
- Never implement financial, identity, authorization, compliance, custody,
  trading, minting or deployment behavior from an unverified claim or test-only
  proof. Preserve a manual review gate for consequential effects.
- Report exactly what changed and what was not run. Use small checkpoints,
  inspect status before retrying uncertain writes and preserve a rollback path.

See `references/branch-policy.md` for branch lifecycle, comparison and promotion.
