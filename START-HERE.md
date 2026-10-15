# Start here: copy, connect, and use one skill

## 1. Pick a starting point

- **Need to reconcile Love Transcends protocols, token economics, mining rewards, contracts, reserves, or a project handoff?** Start with `.agents/skills/lt-protocol-economics-portable/SKILL.md`.

- **Need a repeatable workflow or agent handoff?** Start with
  `.agents/skills/hab-workflow-library/SKILL.md` or
  `.agents/skills/hab-agent-universal/SKILL.md`.
- **Need to debug a failure?** Use `.agents/skills/hab-debugging/SKILL.md`.
- **Need an agent to build a feature?** Use
  `.agents/skills/hab-self-coding/SKILL.md` and read its branch policy first.
- **Need help with OmniRoute?** Use `skills/hab-omniroute/SKILL.md`; choose one
  native upstream skill in `sources/omniroute/skills/` only when relevant.

Load one task-relevant skill plus its directly linked references. Do not paste
the entire library into every conversation. Preserve each versioned workflow
folder; the original and Free-first n8n templates are both intentional.

## 2. Copy/paste prompt

```text
Read START-HERE.md and the one skill at [SKILL PATH].
Follow the project's instructions before acting. Tell me which repository,
branch/revision, files and connectors you actually have access to.
Use only an already-enabled, task-relevant connector. If one is unavailable,
give me a copy/paste path or ask me to enable it; never request credentials in
chat. Keep external calls, paid-provider use, posting, publication, merging and
deployment off until their specific approval gates are met.
For code work, use the approved self-coding lane, inspect current changes first,
preserve unrelated work, run the stated local tests and report exact results.
Do not claim a connector action, test, merge or deployment that did not happen.
```

Replace `[SKILL PATH]` with one path listed above. On a host without file access,
paste that skill's full `SKILL.md` text and the minimum linked reference. The
copy/paste packet is guidance; it does not install a skill.

## 3. Connectors and credentials

Only use integrations that the current host reports as enabled and authorized
for this task. Verify the connected account, repository and read/write scope
before use. If a needed integration is not available, prepare a manual,
read-only or downloadable alternative. Never paste API keys, OAuth tokens,
passwords, private keys or wallet seed phrases into a chat or public repository.
Use the host's approved server-side secret store. Connection is not consent to
send private files, make billable calls or perform external writes.

## 4. Choose a coding lane

The self-coding skill includes all three lanes:

1. **Draft-only:** propose a design and patch/test plan; do not write project files.
2. **Creative sandbox:** with an approved task, explore alternatives on an
   isolated branch forked from the recorded main revision; do not edit main.
3. **Implementation branch:** move selected changes to a narrow task branch,
   test and prepare a draft pull request. Main changes only after human review
   and explicit approval. Deployment is a separate decision.

These lanes do not automatically grant a GitHub connection, connector scope,
secret access or deployment permission.
