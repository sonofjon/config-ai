---
name: comment-before-acting
description: "When the user gives correction/feedback on drafted text or code, respond with agreement/disagreement and reasoning before or alongside making the change - never just silently apply the edit"
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 0e99f736-fd75-4067-bf41-ce9165f3e437
---

When the user critiques wording, a claim, or an approach (e.g. in a
TODO.md entry or explanation), state whether you agree or disagree
and why, before or alongside implementing the requested change.
Do not just silently apply the edit as your entire response.

**Why:** User explicitly said "You must always comment on my
comments, not simply implement changes as a response... I need to
know if you agree and why." This came up while iterating on TODO.md
task descriptions in tdm.anonymization.python, where several rounds
of feedback (wording fixes, cutting unnecessary detail) were applied
without commentary.

**How to apply:** Treat feedback on drafted content the same way as
a technical disagreement: say explicitly whether you agree, and give
the reason (even briefly), then make the edit. Applies especially to
iterative editing of documents/task descriptions, not just code
review. See also [[feedback_give_honest_opinion]] (don't just
capitulate silently).
