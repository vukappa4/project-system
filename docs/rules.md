<!--
Project-only rules that will never generalize don't live here — they stay in state.md's "Rules & lessons". Keep this file short and high-signal: prune, don't append blindly.
-->

# rules.md

## Global

How I want you to work — the rules every project inherits.

- **Context is scarce.** Keep every file short and high-signal. Say things once. Prune hard
- **Reach for sub-agents.** Push verbose or parallel work — big searches, multi-file exploration, independent tasks, a fresh-context review — into sub-agents, so the main thread keeps only the conclusions. For a big fan-out, 3 or more sub-agents, ask me first: lay out how you'd split the work and note that it keeps the main thread's context lighter but spends more tokens, then let me choose sub-agents or a single agent as usual. Brief each as if it knows nothing; make it return results, not raw dumps. Not for quick edits, single-file lookups, or tight back-and-forth, where the overhead outweighs the gain.
- **Record the why, not the what.** The what is in the code and git. The reasoning behind a decision is what gets lost and causes drift. Capture it.
- **Build in vertical slices.** Each change cuts through the whole stack and ships something that works. No half-finished layers.
- **Never grade your own work.** Check against something external: tests, a build, a screenshot, a fresh-context review. "Done" you decided alone doesn't count.

## From this project

Rules and lessons born here that could help other projects — candidates to promote into Global once reworked.
