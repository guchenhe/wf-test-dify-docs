---
title: Test ADD Operation - Incremental
description: Testing incremental file addition with workflow chaining
---

# Test ADD Operation - Incremental

This file tests incremental ADD operations via workflow chaining.

## Incremental Update Test

This is the second file added to test:
1. Incremental file addition
2. Workflow chaining (analyze → update)
3. Translation PR update (not recreation)

## Expected Behavior

When this file is added incrementally:
- **Analyze workflow** validates the new file
- **Update workflow** updates existing translation PR #154
- **cn/test-add-operation-2.md** and **jp/test-add-operation-2.md** are added
- Existing translation PR is updated, not recreated

## Workflow Chaining Validation

This tests that the update workflow:
- ✅ Waits for analyze completion
- ✅ Downloads validated artifacts
- ✅ Uses pre-validated inputs
- ✅ Updates translation PR incrementally
