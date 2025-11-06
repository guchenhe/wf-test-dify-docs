---
title: "Concurrency Test"
description: "Testing rapid updates with concurrency groups"
---

# Concurrency Test

This file is used to test the concurrency control in translation workflows.

## Version 6 - Second rapid test

Updated content - commit 6. Second rapid commit with fixed concurrency.

Testing workflow queuing behavior:
- This commit pushed immediately after commit 5
- Should queue behind commit 5's workflow
- Both should complete successfully
- No cancellations expected
