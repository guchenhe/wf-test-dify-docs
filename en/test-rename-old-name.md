---
title: Test RENAME Operation (Old Name)
description: Testing file rename with surgical reconciliation
---

# Test RENAME Operation

This file tests the RENAME operation in surgical reconciliation.

## Purpose

This file will be:
1. Created with name `test-rename-old-name.md`
2. Translated to cn/jp with same base name
3. Renamed to `test-rename-new-name.md`
4. Rename should propagate to cn/jp files

## Expected Behavior

When this file is renamed incrementally:
- **Surgical reconciliation** detects the rename
- Renames performed: delete + add in same location
- **Extension preserved**: .md → .md (or .mdx → .mdx)
- **cn/test-rename-old-name.md** → **cn/test-rename-new-name.md**
- **jp/test-rename-old-name.md** → **jp/test-rename-new-name.md**

## Rename Detection

The system detects renames by:
- File deleted from docs.json
- File added in same location (same group_path)
- Same position in navigation array
- Extension type preserved
