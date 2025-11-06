---
title: "Concurrency Test"
description: "Testing rapid updates with concurrency groups"
---

# Concurrency Test

This file is used to test the concurrency control in translation workflows.

## Version 4

Updated content - commit 4. Final rapid update test.

This is the fourth workflow trigger. The concurrency group should ensure:
- Only one workflow runs at a time
- No git conflicts on the translation branch
- All commits are processed in order
- Translation state remains consistent
