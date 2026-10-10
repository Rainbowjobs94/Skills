# Self-coding branch policy

## Lifecycle

`main` (read-only starting point)
→ `creative/<task>` (optional broad experiment)
→ human-selected design
→ `task/<task>` (focused implementation forked from the recorded clean base)
→ tests and independent human review
→ draft PR against `main`
→ human-approved merge
→ separately authorized deployment and live verification

The creative experiment is optional; implementation need not copy it wholesale.
Copy only approved changes into the task branch. Record the base commit for each
branch so differences and rollback are clear. Never merge the creative branch
directly into main. Do not silently change main protections or release settings.

## Required handoff

For each branch report:

- exact base revision and branch name
- changed files and why
- checks actually run, with pass/fail/blocked results
- security, privacy, compatibility, migration and cost impacts
- unfinished work, disabled behavior and rollback/recovery notes
- the specific human decision needed next

No route in this lifecycle authorizes an external provider request, secret
addition, production write, merge or deployment by itself.
