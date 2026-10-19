---
name: feedback-no-line-ending-reports
description: Do not report line endings (CRLF/LF) or that files keep them after edits
metadata:
  node_type: memory
  type: feedback
  originSessionId: f7b9a8ee-2c0a-4929-b300-1bd694519eb5
  modified: 2026-10-19T15:19:53.022Z
---

Do not mention line endings in replies (e.g. "the file still uses CRLF
line endings"). Keep preserving and checking existing line endings
silently. See also [[feedback-no-line-length-reports]].

**Why:** The user finds it noise; preserving a file's line endings is
expected, not news.

**How to apply:** Keep each file's existing line endings when editing and
verify them as usual, but only mention line endings when they cause a
problem that needs a decision (e.g. mixed endings already in a file, or a
tool that cannot preserve them).
