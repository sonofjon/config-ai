---
name: feedback-no-line-length-reports
description: "Do not report line lengths or \"within the limit\" checks to the user"
metadata:
  node_type: memory
  type: feedback
  originSessionId: 5ed4a8db-f63e-498c-a9d6-ce17dfea5b56
  modified: 2026-10-09T18:37:02.547Z
---

Do not mention line lengths in replies (e.g. "the line is 50 characters,
within the limit"). Keep checking the 79-character limit silently.

**Why:** The user finds it noise; compliance with the limit is expected, not
news.

**How to apply:** Check widths as usual, but only mention a line length when a
line cannot be made to fit and a decision is needed.
