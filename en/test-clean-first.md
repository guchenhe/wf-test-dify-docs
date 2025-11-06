---
title: Clean Incremental Test - First File
description: Testing incremental translation with English file removal fix
---

# Clean Incremental Test - First File

This is the **first file** in a clean incremental translation test, after fixing the English file leakage issue.

## Expected Behavior

When this PR is created:
1. Translation PR should be created
2. This file should be translated to `cn/` and `jp/`
3. Translation PR should ONLY contain:
   - `cn/test-clean-first.md`
   - `jp/test-clean-first.md`
   - `docs.json`
4. Translation PR should NOT contain any `en/` files

## Verification

After the first translation commit, we'll verify:
- No English source files in translation branch
- Clean git history
- Proper Last-Processed-Commit tracking
