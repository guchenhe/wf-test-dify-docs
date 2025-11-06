---
title: "Concurrency Test"
description: "Testing rapid updates with concurrency groups"
---

# Concurrency Test

This file is used to test the concurrency control in translation workflows.

## Version 9 - Middle Commit (Should Be Cancelled)

Updated content - commit 9. This is the middle commit that should be cancelled.

Expected behavior:
- Workflow for commit 8 should complete
- Workflow for commit 9 should be CANCELLED
- A notification should appear on PR #121
- Commit 10 (next) should complete
