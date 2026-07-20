---
name: start
description: Start a session on a project that already exists.
disable-model-invocation: true
---

I'm starting a session on a project that already exists. Do these two steps in order.

## 1. Get your bearings

Before asking me anything, read, in this order:

- `CLAUDE.md` — the map of how this system works and what each file holds (it auto-loads, so it's already in context).
- The `<name>.md` context file, named after the project folder — what the project is and why it exists. If you can't find it, ask me where it is.
- `rules.md` — the global rules I work by, plus this project's generalizable lessons.
- `state.md` — the live handoff from the last session. Sections still holding a placeholder mean nobody has decided them yet.

## 2. Grill me

Interview me relentlessly until we reach a shared understanding — until we can both state what we're building and why. Walk down each branch of the design tree, resolving dependencies between decisions one-by-one. For each question, give your recommended answer.

Ask one question at a time and wait for my answer before the next. Asking several at once is bewildering.

If a question can be answered by exploring the files or the code, explore instead of asking.

Don't write `state.md` here — /end owns that at the session's close.
