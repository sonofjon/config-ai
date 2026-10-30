---
name: agent-commit-hunks
description: Commit hunks when only part of a file's changes goes into a
  commit.
---

# Commit hunks

## Why

The changes on disk are what the user has approved. Committing them in parts
must not alter them: every committed line has to come from those changes.
Taking lines unchanged from `git diff` guarantees this, whereas recreating
or rewriting file content does not: any slip would end up in the commit
unnoticed.

## How

Save `git diff` to a file and build the patch file from it with commands
that select and edit lines by number, such as `sed`. Never write patch lines
yourself, and keep the text of every line as it is. Stage the patch with
`git apply --cached --recount <patch>`, and leave the files being committed
as they are.

If a hunk mixes changes for different commits, turn its unselected `-` lines
into context lines (leading space) and delete its unselected `+` lines. For
example, to commit only `b` -> `B`:

```
 a          a
-b         -b
+B   ->    +B
-c          c
+C
```
