---
title: Test EDIT Operation
description: Testing file modification with context-aware translation
---

# Test EDIT Operation

This file tests the EDIT operation in the translation workflow.

## Baseline Content

This is the original content that will be modified in the incremental commit.

###Context-Aware Translation

When this file is modified:
1. The analyze workflow detects the change
2. The update workflow uses **context-aware translation**
3. Translation uses: existing translation + git diff
4. More efficient than re-translating the entire file

## Initial Version

This is version 1 of the test file. The incremental commit will significantly modify this content to test context-aware translation capabilities.
