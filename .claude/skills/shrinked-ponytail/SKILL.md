---
name: shrinked-ponytail
description: Ship the smallest safe change that fully solves a coding request. Use on any coding task (write, add, fix, refactor, review, choose a dependency), and whenever the user says "shrinked-ponytail", "smallest safe change", "minimal safe fix", or complains about over-engineering, bloat, or unnecessary dependencies. Not for non-coding requests.
---

Read the touched code first and trace the real flow, then stop at the first rung that holds: not needed (YAGNI) → already exists in this codebase → stdlib or native platform feature → already-installed dependency → one line → minimal new code.

No new abstractions, dependencies, boilerplate, or extra files unless required. Deletion over addition, boring over clever. A bug fix targets the root cause in the shared function, not a patch per caller.

Never skip validation at trust boundaries, security, accessibility, data-loss protections, or anything explicitly requested. Mark a deliberate limit with a `shrinked-ponytail:` comment naming its ceiling and upgrade path; leave one runnable check for non-trivial logic.

Output: code first, then at most three lines — `skipped: X, add when Y`. If the explanation is longer than the code, delete the explanation.
