# Rainbow Jobs Skills

A portable library of IA Guardian Hab skills, manual workflow references, and pinned upstream skill sources for personal AI agents.

## What is included

- 15 Hab-authored skill folders in `.agents/skills/`, including their reference files, record examples, validator and tests. Both original and Free-first n8n workflow versions are retained.
- A Hab OmniRoute reference skill for selecting native skills and comparing routes. Its optional paid-fallback design is user-approved but still proposed, not implemented or activated: free-first, explicit operator opt-in, approval for every paid request, and a conservative $10 per-task-run reserve ceiling.
- The complete 52-file `skills/` subtree (46 native modules) from `diegosouzapw/OmniRoute`, pinned to commit `7510677f2f8f5317f1947284dab650d01333915d`, placed under `sources/` as references rather than active skills. Upstream MIT license and notices are retained there.
- Catalog and SHA-256 source manifest for the packaged paths.

## Use

Start with [`START-HERE.md`](START-HERE.md). It includes a short copy/paste prompt, a skill-by-skill route and a three-lane coding process. Copy one `.agents/skills/<name>/` folder into a host-supported skills location, or paste the linked skill text if that host has no skill importer. Validate its format there. The upstream OmniRoute modules under `sources/` are references, not auto-activated.

## Rights and limits

The owner authorized this public publication and confirmed redistribution rights for the 15 Hab skill folders. That permission is not an open-source license for others to reuse those files; see `RIGHTS-AND-SOURCES.md`. No repository-wide license is asserted. The separate OmniRoute snapshot retains its upstream MIT LICENSE and THIRD_PARTY_NOTICES.

This expanded package also adds original Hab debugging and self-coding skills, including the three authorized coding lanes. `main` remains protected: a person reviews and approves any merge. The original n8n examples are manual templates, not imported workflows or running automations. The OmniRoute snapshot is only the selected skills subtree and notices, not a full application/repository mirror, installation, code audit, provider account or deployed service. No personal profile, credentials, or private signing material is included.
