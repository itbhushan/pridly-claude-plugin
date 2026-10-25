---
description: "Undo a change Pridly made (give the change number, or ask for the list)"
argument-hint: "[change number]"
---

If I gave a change number ("$ARGUMENTS"), call `undo_change` with that `change_id` and show me the preview of what would be restored. Wait for my explicit yes before confirming.

If I did not give a number, call `change_history`, list the most recent changes with their numbers, and ask which one to undo.
