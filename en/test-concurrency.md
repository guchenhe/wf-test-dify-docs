---
title: "Concurrency Test"
description: "Testing rapid updates with concurrency groups"
---

# Concurrency Test

This file is used to test the concurrency control in translation workflows.

## Version 7 - Third rapid test

Updated content - commit 7. Third consecutive commit.

Final validation:
- Three workflows queued in sequence (commits 5, 6, 7)
- All using concurrency group: `docs-translation-test/concurrency-rapid-updates`
- Should all complete without cancellation
- Translation PR should be created/updated successfully
