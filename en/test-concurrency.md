---
title: "Concurrency Test"
description: "Testing rapid updates with concurrency groups"
---

# Concurrency Test

This file is used to test the concurrency control in translation workflows.

## Version 5 - Testing head_branch fix

Updated content - commit 5. Testing the fixed concurrency with head_branch.

This should now work correctly because:
- Concurrency group uses `github.event.workflow_run.head_branch`
- Same PR branch = same concurrency group
- Workflows will queue properly
- No more cancelled workflows
