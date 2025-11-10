---
title: Test DELETE Operation
description: Testing file deletion with fixed workflow
---

# Test DELETE Operation

This file tests the DELETE operation with the fixed deletion handling.

## Test Steps

1. ✅ **Initial commit**: Add this file with docs.json entry
2. ⏳ **Wait for translation**: Translation PR should create cn/jp files
3. ⏳ **Delete commit**: Delete this file and remove from docs.json
4. ⏳ **Verify deletion**: Translation PR should delete cn/jp files

## Expected Behavior

The deletion fix ensures:
- **Always processes deletions** via `process_deleted_files()`
- **Independent of structure_changed** flag
- **Works for deletion-only commits** (sync_required=False)

## Fix Details

Two issues were fixed:
1. Deletion logic now runs always, not just when docs.json changes
2. Deletion-only commits (no additions/edits) are properly handled

## Files Deleted

When this file is deleted:
- ✓ `cn/test-delete-operation.md` deleted
- ✓ `jp/test-delete-operation.md` deleted
- ✓ Entries removed from docs.json (all languages)
