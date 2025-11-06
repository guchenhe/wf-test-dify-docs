---
title: "Concurrency Test"
description: "Testing rapid updates with concurrency groups"
---

# Concurrency Test

This file is used to test the concurrency control in translation workflows.

## Version 10 - Final Test Commit

Updated content - commit 10. This is the final commit that should complete successfully.

Expected results after all workflows complete:
- Commit 8: ✅ Completed
- Commit 9: ⚠️ Cancelled with notification posted to PR #121
- Commit 10: ✅ Completed
- Translation PR #122: Updated with commits 8 and 10 only
