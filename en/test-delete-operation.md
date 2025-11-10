---
title: Test DELETE Operation
description: Testing file deletion with automatic cleanup
---

# Test DELETE Operation

This file tests the DELETE operation in the translation workflow.

## Purpose

This file will be:
1. Created in the initial commit
2. Translated to cn/jp
3. Deleted in the incremental commit
4. Cleanup should propagate to translation PR

## Expected Behavior

When this file is deleted incrementally:
- **Analyze workflow** detects the deletion
- **Update workflow** removes the file from translation PR
- **cn/test-delete-operation.md** and **jp/test-delete-operation.md** are deleted
- **docs.json** is updated to remove entries from all language sections

## Deletion Test

This file exists temporarily to validate that the surgical reconciliation system correctly handles file deletions across all language versions.

### Cleanup Validation

The deletion should:
- ✅ Remove physical files from all language directories
- ✅ Remove entries from docs.json navigation for all languages
- ✅ Update translation PR with deletion commit
- ✅ Maintain consistency across language versions
