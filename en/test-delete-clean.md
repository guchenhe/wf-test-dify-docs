---
title: Test DELETE Operation (Clean)
description: Testing file deletion with automatic cleanup
---

# Test DELETE Operation

This is a fresh test of the DELETE operation with the fixed workflow.

## Purpose

This file will be:
1. Created in the initial commit
2. Translated to cn/jp
3. Deleted in the incremental commit
4. Cleanup should propagate to translation PR

## Expected Behavior

When this file is deleted incrementally:
- **Analyze workflow** triggers (no paths filter blocking)
- **Update workflow** removes the file from translation PR
- **cn/test-delete-clean.md** and **jp/test-delete-clean.md** are deleted
- **docs.json** is updated to remove entries from all language sections

## Test Steps

1. ✅ Initial commit: Add this file + docs.json entry
2. ⏳ Wait for translation PR
3. ⏳ Incremental: Delete file + remove from docs.json
4. ⏳ Verify translation PR updated with deletions
