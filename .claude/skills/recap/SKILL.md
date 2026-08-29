---
name: recap
description: Give a status recap of the current task when the user asks for a "recap," "status," "where things stand," or "catch me up."
---

# Recap

A recap is a status report, not a work session. The point is to report
status without quietly sliding into "let me just fix this real quick."  The
recap must be grounded in the current state of the code, not in what was
said about it earlier in the conversation.

## Process

### 1. Refresh — recheck the code, not your memory of it

The only thing likely to have changed between sessions is the code on
disk. Before reporting status, re-derive it from the current state of the
repo rather than trusting what was said about it earlier in the
conversation:

- Run `git status` / `git diff` (or `git log` since the last commit you're
  aware of) to see what's actually changed — edits made by the user
  directly, or by another Claude session working on the same repo.
- Re-read any file you're about to make a claim about, rather than quoting
  what it contained the last time you read it.
- Re-run anything you're about to cite as evidence (tests, a build, a
  script) rather than reusing an earlier run's result — the code behind that
  result could have changed since.

Skip the refresh for anything you already checked in the last few minutes of
this same session — the goal is catching drift across time, not repeating
work.

### 2. Report — three parts, always in this order

1. **Goal** — restate the goal in the user's own words, not your inferred
   version of the underlying intent. If it appears to have drifted since it
   was set, say so briefly. If there's more than one distinct open goal,
   list each one separately with its own status rather than blurring them
   into one line; goals already finished just get a one-line "done."
2. **Actual status, with evidence** — where things stand, and what
   specifically supports that claim. Passing tests is not proof something
   works end-to-end. If there's no real evidence for a claim, say that
   plainly instead of rounding up.
3. **Next steps** — a short list, each tagged `[Claude]` or `[User]`. For
   anything stalled, say specifically what's needed to move it: something
   only `[User]` can decide or provide, versus a technical problem
   `[Claude]` hasn't solved yet.

### 3. Hard constraint

Do not start any new work during a recap — no fixes, no extra investigation
beyond the refresh step, no speculative next actions. If something urgent
turns up while refreshing, report it in the status section rather than
acting on it.

## Gotchas

- Don't treat your own earlier read of a file, or an earlier test run, as
  still accurate — that's exactly what goes stale between sessions.
- "Tests pass" and "this is verified" are not the same claim. Call out the
  difference if the evidence bar has quietly slipped.
- If nothing has actually changed since the last recap, say that directly
  instead of restating the same status in new words.
