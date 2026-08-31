---
name: feedback_no_premature_implementation
description: Never edit code unless explicitly instructed; questions and opinions are not instructions
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 7550e818-149c-4e36-8016-fa38573b5ce9
  modified: 2026-08-18T10:24:10.663Z
---

Only edit code when the user explicitly instructs it with words like
"do it", "implement", "fix it", "edit", "remove it", "go ahead".

Things that are NOT instructions to edit code:
- Opinions ("that is confusing", "I prefer X")
- Questions ("why does this work?", "isn't this redundant?")
- Questions about edits ("why did you add X?", "what happened here?")

Respond to all of the above with explanation and discussion, not edits.
"Why did you do X?" seeks understanding, not reversal.

**Why:** The user discusses design before deciding. Jumping to edits
during discussion is frustrating, as is reverting code when the user
merely asks about it. 

**How to apply:** During discussions, answer questions and explore the
problem. Only touch code on unambiguous instruction, and only do
exactly the action instructed - not other actions that feel implied
by it.
