---
name: end
description: End a session — save state, capture lessons, commit.
disable-model-invocation: true
---
I'm ending a session. Do these three steps in order.

## 1. Update state.md

Rewrite only what actually changed. On each section's first fill (a fresh project), replace its placeholder description with real content, and leave the header comment untouched.

- **Now / Short term / Long term** — compress and rewrite to match where we are. Never append; they're a snapshot, not a log.
- **Rules & lessons** — add or prune deliberately, don't churn. Only rules specific to THIS project that never generalize. A lesson that would help other projects goes to `rules.md` instead (step 2).

## 2. Add a lesson to rules.md — only if one emerged

If this session produced a rule or lesson that could help other projects, add it to `rules.md` under **From this project**. If nothing generalizable came up, leave the file alone — don't pad it.

## 3. Commit and push — only if this is a git repo

If the project has a git repo with a remote, stage everything, commit with a message that captures the *why* of what changed, and push. If there's no repo or no remote, skip this and tell me the project has no git home yet.
