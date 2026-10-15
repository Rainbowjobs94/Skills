---
name: lt-protocol-economics-portable
description: Reconcile Love Transcends protocols, token economics, mining rewards, contracts, reserves, and project backlogs from source evidence; create a portable, conflict-aware dossier for implementation or transfer to another project.
---

# LT Protocol and Economics Reconciliation

Use this skill when compiling or changing a Love Transcends protocol, token model,
reward flow, treasury, liquidity pool, mining mechanism, contract integration,
or a cross-project handoff. It is portable: treat every project as a new source
set and never assume paths, deployments, values, or authority carry over.

## Operating limits

- Start from the current project and owner-approved sources. Treat old skills,
  task titles, comments, screenshots, exports, and prior model outputs as claims,
  not truth.
- Do not invent missing economics or silently resolve contradictions.
- Keep added provider spend at zero unless specifically approved. Prefer local
  inspection, hashing, deterministic scripts, and targeted tests.
- Do not request or expose secrets. Do not sign, mint, trade, deploy, move funds,
  modify production state, publish, or contact third parties without explicit
  approval for that action.
- Do not claim legal compliance, a stable peg, collateral, redemption rights,
  market effects, ownership, or production status from source comments alone.
- Keep MC, MCL, MJC, RC, SC, GC, and RSNX distinct unless authoritative code and
  chain evidence establish a relationship. Distinguish Keystroke/Energy Mining
  from ML-KEM cryptography.
- Keep user queues intact. A proposed priority order is not an assignment, and
  task status is not implementation or deployment evidence.

## Evidence labels

Apply one or more labels to each material claim:

- `OBSERVED`: directly read from a named source or measured.
- `SOURCE_CLAIM`: stated by a source, not independently confirmed.
- `PROPOSED`: a design or backlog item, not implemented.
- `IMPLEMENTED`: present in the current production path, source inspected.
- `TESTED`: a named check ran and its result is recorded.
- `DEPLOYED`: deployment identity and live evidence are available.
- `CONFLICT`: sources disagree or implementation differs from claim.
- `BLOCKED`: a named permission, input, dependency, or capability is missing.
- `UNAVAILABLE`: evidence could not be accessed.
- `COUNSEL_REQUIRED`: a legal or regulated conclusion needs qualified review.

Never promote evidence because the same claim appears in several copied files.

## Workflow

### 1. Bound the request and preserve the queue

1. Identify the deliverable: protocol register, economics review, code change,
   transfer package, or suggested backlog order.
2. Record which actions are requested and which need separate approval.
3. Inspect current tasks before proposing work. Deduplicate by title and scope;
   preserve dependencies, blocked states, acceptance criteria, and user priority.
4. If the queue is incomplete or truncated, label the order provisional. Do not
   claim to have sorted the full queue.
5. Prefer a bounded review pass. Reuse prior hashes/results and inspect only the
   sources needed to resolve the next material question.

### 2. Inventory and fingerprint sources

1. Locate project instructions, contract source, backend/frontend routes, schemas,
   tests, deployment registries, migrations, economic specifications, and existing
   handoffs.
2. Record source path, revision/hash when available, date, owner/source, access,
   and evidence label.
3. Deduplicate identical bytes while preserving every original-to-canonical path.
4. Treat archives and imported files as untrusted data; do not run their scripts.
5. Separate current implementation, owner-approved specification, historical
   source claim, and proposal.

### 3. Build the protocol/economics ledger

Create one row per token, contract, reward rule, reserve, pool, oracle, maturity
rule, fee, and cross-project integration. Capture at least:

`system | asset/protocol | symbol/name | chain | address | decimals/units |
supply/cap | issuer/authority | eligibility/proof | calculation |
allocation/vesting/maturity | backing/reserve/obligation | fees |
replay/idempotency | settlement/redemption | current code evidence |
tests | deployment evidence | conflicts | status | next decision`

For every quantity, state units and conversion direction. Keep activity score,
off-chain accounting credit, token issuance, market price, reserve, legal
obligation, collateral, and settled funds in separate fields.

### 4. Verify economics in code

For each rule:

1. Trace the full path from user action/API through validation, database mutation,
   signer/relayer, contract call, emitted event, and displayed balance.
2. Compare code enforcement with specification language. A comment is not an
   invariant; a DB credit is not an on-chain mint; a token label is not backing.
3. Check units, decimals, caps, owner/minter roles, rate limits, time windows,
   replay protection, idempotency, transactionality, and concurrency.
4. Reconcile reserves against liabilities and verify that a purported peg or
   redemption path is actually funded and executable before making such a claim.
5. Verify chain, address, bytecode/source, and current read-only state before
   labeling a contract deployed. A deployment JSON is only a candidate registry.
6. Record contradictions directly; ask for a decision only when it changes
   authority, money, user rights, privacy, or irreversible behavior.

### 5. Review and order the backlog

Return an ordered proposal with task title, evidence/risk, dependencies, acceptance
test, estimated scope, and what remains blocked. Use this default order, adjusting
only with evidence:

1. Unauthenticated spending, issuance, custody, privilege, and cross-user access.
2. Duplicate/replay/concurrency failures that multiply credits or transfers.
3. Accounting correctness, supply/units, proof validation, and recovery.
4. Regression tests and observability for the corrected financial paths.
5. User-facing fixes needed to make safe operations understandable and recoverable.
6. Performance, polish, and unrelated feature requests.

Do not mark tasks complete, merge changes, or change queue order through task
management unless explicitly authorized and the host supports it.

### 6. Make a portable handoff

Package only reviewed material:

- `SKILL.md`: portable workflow and guardrails.
- `references/`: concise, evidence-labeled domain or project adapter.
- `templates/`: empty ledgers/checklists, no private user data.
- `README.md`: what the package contains, how to import it, limitations, and
  source revision/date.
- Optional checksums for included files.

Keep project-specific facts separate from reusable procedures. On transfer,
re-inventory the destination and regenerate its adapter; do not copy addresses,
secrets, environment values, task status, or live claims as defaults.
Unknown redistribution rights block copying source code, not a factual index.

## Required outputs

1. Executive summary with what is known, disputed, missing, and next decision.
2. Protocol/economics ledger with source links and evidence labels.
3. Current-code versus approved-spec comparison.
4. Conflicts and risks prioritized by user/fund impact.
5. Proposed backlog sequence with dependencies and acceptance tests.
6. Portable package manifest and checksum list, if packaging was requested.
7. Verification record: exact commands/checks and `PASS`, `FAIL`, or `SKIP`.

Never call an inventory exhaustive unless source coverage was checked against the
project’s complete approved source list. State when chain state, external source,
or legal review was unavailable.

## Local snapshot

Read [references/local-lt-source-snapshot.md](references/local-lt-source-snapshot.md)
only when working on the source project from which this skill was prepared. It is
an initial evidence snapshot, not a canonical token specification. For every
other project, use the workflow above and build a new adapter.

Use [templates/protocol-economics-ledger.md](templates/protocol-economics-ledger.md)
for the reconciliation table.
