# claude.md

I'm the map for this project: what the system is, which file holds what, and the order to read them.

## The system

A small, repeatable setup for every project where I lean on AI, each project feeds rules back up so the next one starts smarter.

## The files

- **claude.md**: this map. You never edit it.
- **`<project-name>.md`**, the project's context: what it is, why it exists, the shared vocabulary. Written before we start.
- **rules.md**: *Global*: the rules I work by, shared by every project. *From this project*: lessons born here that may generalize. You read it; you only add to it via /end.
- **state.md**, the live handoff and the only file that changes every session.

## Read order

claude.md (this) → the `<name>.md` context file → rules.md → state.md.

## The skills

- **/start** — begin a new project, or start a new session: read the files above, then interview me until we're aligned.
- **/end** — close a session: update state.md, add any generalizable lesson to rules.md, and commit.
- **/handoff-continue** — a session hits its context limit mid-task: dump what a fresh chat needs into state.md's Continue section.
- **/continue** — in the fresh chat: read the Continue handoff, pick the work up, then clear it.
