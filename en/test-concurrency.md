---
title: "Concurrency Test"
description: "Testing rapid updates with concurrency groups"
---

# Concurrency Test

This file is used to test the concurrency control in translation workflows.

## Version 8 - Testing Cancellation Notifications

Updated content - commit 8. Testing the new cancellation handler.

This commit should trigger a workflow that includes the cancellation notification feature.
Expected: If cancelled, a clear message will appear on the PR.
