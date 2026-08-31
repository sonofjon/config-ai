---
name: feedback-ask-before-memory
description: Always ask before adding or updating a memory - do not save proactively without confirmation
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 7550e818-149c-4e36-8016-fa38573b5ce9
  modified: 2026-08-18T14:39:19.922Z
---

Never write a new memory file, or add content to an existing one,
without asking the user first and getting confirmation. This
overrides the general auto-memory instruction to save proactively -
that default is revoked.

**Why:** The user wants control over what accumulates in the
persistent, cross-conversation memory index, rather than having
content added unilaterally based on my own judgment of what seems
worth keeping.

**How to apply:** When something comes up that seems worth
remembering, propose it to the user first (what you'd save, and
which file/type) and wait for explicit agreement before calling
Write or Edit on anything under the memory directory. The only
exception is when the user has already given an explicit, direct
instruction to save something specific (e.g. "add a memory that
says X") - that instruction itself is the confirmation, so it can be
acted on directly without a further round-trip.
