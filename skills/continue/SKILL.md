---
name: continue
description: Resume a session handed off mid-task.
disable-model-invocation: true
---

A previous session ran out of context mid-task and left a handoff in `state.md`'s `Continue` section. Pick the work up from there. Do these in order.

## 1. Get your bearings

Read, in this order: `CLAUDE.md`, the `<name>.md` context file, `rules.md`, then `state.md`, with `Continue` as the priority. If `Continue` is empty there's no handoff to resume: stop and run `/start` instead.

## 2. Absorb the handoff

Read the `Continue` section carefully. Then check the working tree matches "done since the last clean state" — don't build on state you haven't confirmed is on disk.

## 3. Resume

State where you're picking up and the next action (the top unchecked box). The handoff already holds the plan: use `/grill` only if you're missing something important to continue the task.

## 4. Clear the handoff

Once you've absorbed it and resumed, empty the `Continue` section.
