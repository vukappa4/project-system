# Walter's Projecct System

One system for every project you run with AI. It gets smarter each time.

## The files

Three Markdown files sit in your project root, next to a `<project-name>.md` context file:

- **[claude.md](project-docs/claude.md)**. What the system is, which file holds what, the order to read them.
- **[rules.md](project-docs/rules.md)**. *Global*: the rules you work by, shared by every project. *From this project*: lessons born here that might generalize. Only `/end` adds to it.
- **[state.md](project-docs/state.md)**: the live handoff. The one file that changes every session. Five sections: **Now**, **Short term**, **Long term**, **Rules & lessons**, and **Continue**.

The fourth file, `<project-name>.md`, is the project's context — what it is, why it exists, the shared vocabulary. You write it once, before you start.

## The skills

Four skills, invoked by hand (you call them, the model doesn't reach for them on its own):

- **[/start](skills/start/SKILL.md)** begin a new project, or resume a session. Reads the files above, then interviews you until you both know what you're building and why.
- **[/end](skills/end/SKILL.md)** closes a session. Rewrites `state.md`, promotes any generalizable lesson into `rules.md`, then commits and pushes if the project has a git remote.
- **[/handoff-continue](skills/handoff-continue/SKILL.md)**: writes what a fresh chat needs to continue the current session when a session is running out of context mid-task.
- **[/continue](skills/continue/SKILL.md)**: reads the Continue handoff and picks the work up in a fresh chat.

## The loop

1. `/start` — read the context, get grilled until you're aligned.
2. Build in vertical slices. Each change ships something that works.
3. `/end` — save state, capture the lesson, commit.
4. Next session, `/start` reads `state.md` and picks up exactly where you left off.

Run out of context mid-task? `/handoff-continue` in the dying chat, `/continue` in a fresh one — same work, new context.

## Use it in your own project

1. Copy `claude.md`, `rules.md`, and `state.md` from [`project-docs/`](project-docs) into your project root.
2. Write a `<project-name>.md` next to them — what the project is and why it exists.
3. Put the `skills/` folder wherever your AI tool loads skills from.
4. Run `/start`.

## Repo layout

```
project-system/
├── project-docs/
│   ├── claude.md
│   ├── rules.md
│   └── state.md
└── skills/
    ├── start/SKILL.md
    ├── end/SKILL.md
    ├── handoff-continue/SKILL.md
    └── continue/SKILL.md
```

In this repo the three files live under `project-docs/` to keep the root clean — but every reference inside them is a bare, root-relative name (`claude.md`, `rules.md`, `state.md`). That's on purpose: when you copy them into a real project they land in its root and the links just work.
