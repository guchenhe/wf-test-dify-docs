---
title: Test ADD Operation
description: Testing file addition with automatic translation
---

# Test ADD Operation

This file tests the ADD operation in the translation workflow.

## Initial Commit

This is the baseline content added in the first commit to test:
1. File creation and translation
2. Workflow chaining (analyze → execute)
3. Translation PR creation

## Expected Behavior

When this file is added:
- **Analyze workflow** validates the file
- **Execute workflow** creates translation PR
- **cn/test-add-operation.md** and **jp/test-add-operation.md** are created
- Translation PR is opened with fresh translations

## Test Scenario

Testing that new files are:
- ✅ Translated to all target languages
- ✅ Added to docs.json navigation for all languages
- ✅ Security validated (file size, path, count)
