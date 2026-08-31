---
name: feedback_consistency
description: Maintain implementation consistency with existing methods; avoid fragile designs
type: feedback
---

New methods must maintain consistency with existing methods in terms of
implementation patterns.

Do not build in fragilities even if they seem theoretical -- design for
robustness.

**Why:** The user values maintainable, uniform code. A fragile design
(e.g. relying on external iteration behavior staying the same) is
unacceptable even if it works today.

**How to apply:** When adding a new strategy/method that follows an
existing pattern, ensure it works correctly under the same conditions
as all other strategies. If the existing infrastructure doesn't support
the new case cleanly, fix the infrastructure rather than working around it.
