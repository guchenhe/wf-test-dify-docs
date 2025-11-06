---
title: Fresh Workflow Test - Beta File
description: Testing incremental translation updates with the refactored workflow
---

# Fresh Workflow Test - Beta File

This is the second file added to test incremental translation updates.

## Incremental Update Testing

When this file is added to the existing PR #96, it should trigger the **Update workflow** (`sync_docs_update.yml`) which will:

1. Find the existing translation PR #97
2. Determine the incremental update range (last processed commit → new commit)
3. Translate only the new/changed files
4. Update the translation PR with a new commit
5. Ensure no English files leak into the commit

## Expected Behavior

The translation PR should receive a second commit containing:
- cn/test-fresh-beta.md
- jp/test-fresh-beta.md
- Updated docs.json
- **NO English files (en/test-fresh-beta.md)**

## Success Criteria

✅ Both workflows use the same `translate_pr.py` script
✅ English file removal works in both workflows
✅ Incremental updates work correctly
✅ Commit history is clean and trackable
