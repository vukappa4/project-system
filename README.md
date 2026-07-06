# project-system

One system for every project you run with AI. It gets smarter each time.

## The files

Three Markdown files sit in your project root, next to a `<project-name>.md` context file:

- **[claude.md](project-docs/claude.md)** — the map. What the system is, which file holds what, the order to read them. Read it first. Never edit it.
- **[rules.md](project-docs/rules.md)** — the durable layer. *Global*: the rules you work by, shared by every project. *From this project*: lessons born here that might generalize. Only `/end` adds to it.
- **[state.md](project-docs/state.md)** — the live handoff. The one file that changes every session. Four sections: **Now**, **Short term**, **Long term**, **Rules & lessons**.

The fourth file, `<project-name>.md`, is the project's context — what it is, why it exists, the shared vocabulary. You write it once, before you start.

## The skills

Two skills, invoked by hand (`disable-model-invocation: true` — you call them, the model doesn't reach for them on its own):

- **[/start](skills/start/SKILL.md)** — begin a new project, or resume a session. Reads the files above, then interviews you until you both know what you're building and why.
- **[/end](skills/end/SKILL.md)** — close a session. Rewrites `state.md`, promotes any generalizable lesson into `rules.md`, then commits and pushes if the project has a git remote.

## The loop

1. `/start` — read the context, get grilled until you're aligned.
2. Build in vertical slices. Each change ships something that works.
3. `/end` — save state, capture the lesson, commit.
4. Next session, `/start` reads `state.md` and picks up exactly where you left off.

## Use it in your own project

1. Copy `claude.md`, `rules.md`, and `state.md` from [`project-docs/`](project-docs) into your project root.
2. Write a `<project-name>.md` next to them — what the project is and why it exists.
3. Put the `skills/` folder wherever your AI tool loads skills from.
4. Run `/start`.

`state.md` ships as an empty template. `/end` fills it — there's no "create from template" step.

## Repo layout

```
project-system/
├── project-docs/        # the three portable files (copied into each project's root)
│   ├── claude.md
│   ├── rules.md
│   └── state.md
└── skills/
    ├── start/SKILL.md
    └── end/SKILL.md
```

In this repo the three files live under `project-docs/` to keep the root clean — but every reference inside them is a bare, root-relative name (`claude.md`, `rules.md`, `state.md`). That's on purpose: when you copy them into a real project they land in its root, side by side, and the links just work.
