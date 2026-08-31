---
name: feedback_check_surrounding_code_for_style
description: "Determine comment/code style by reading surrounding code, not by asking the user"
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 3596ac70-b3bb-4134-bf99-14d101563ea4
---

Read the surrounding code to identify the correct style before writing comments, variable names, or other stylistic elements. Never ask the user what style to use when the answer is derivable from the existing code.

**Why:** The CLAUDE.md "Code Consistency" rule already requires checking surrounding code before edits. Asking the user is a wasted step when the answer is right there.

**How to apply:** Before writing any comment, docstring, or stylistic element, scan nearby code for existing examples of the same construct and match that style exactly.
