---
name: hab-debugging
description: Diagnose software failures with bounded evidence, a reproducible case, competing hypotheses, and regression tests. Use when a bug, failed test, deployment symptom, or unexpected behavior needs investigation; do not infer a fix or deployment from source alone.
---

# Hab evidence-first debugging

## Boundary

Read current project instructions, task state, relevant source and recent changes
before diagnosis. This skill directs investigation; it does not grant production
access, publish a fix, change credentials, or activate a provider. Protect user
data and redact secrets from logs, screenshots and test output.

## Workflow

1. State the observed failure, where and when it occurred, affected revision,
   expected behavior and actual behavior. Separate verified evidence from a
   report, hypothesis and unknown.
2. Reproduce using the lowest-risk local path. Prefer a minimal synthetic
   fixture. Capture the exact command, environment constraints and full relevant
   error context; omit tokens, personal data and unrelated log noise.
3. Trace the failure through the call path, configuration, state and recent
   changes. Check existing issues, tests, workarounds, rollbacks and whether a
   proposed fix already exists before editing.
4. Maintain up to three ranked hypotheses with evidence for and against each.
   Run the cheapest discriminating read/test first; change one factor at a time.
   A successful query with no error record is not proof of successful behavior.
5. If implementation is authorized, use `hab-self-coding`'s chosen lane. Add a
   focused failing regression test, make the smallest change, then run targeted
   tests and relevant regression suites. Do not weaken a test merely to turn it
   green.
6. Inspect the resulting diff for unrelated edits, secret/data exposure,
   migrations, compatibility and security impact. Record the actual commands
   and pass/fail/blocked result. Never claim a test, code review or live check
   that did not run.
7. Verify a production symptom only through an authorized live read-only check.
   Source code, local mocks and CI do not prove a deployment changed. Production
   mutation, rollback, publication and merge require their own authorization.

## Stop and escalate

Stop rather than guess when evidence is missing, a repro would affect users,
the issue may involve private credentials/data, or the proposed change alters
funds, accounts, migration, authentication, deployment or legal status. Report
the exact evidence needed and a reversible next step. Preserve current behavior
and unrelated work. Don't fan out to paid models or external services by default.
