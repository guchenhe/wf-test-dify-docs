---
title: Clean Incremental Test - Second File
description: Testing incremental update after English file fix
---

# Clean Incremental Test - Second File

This is the **second file** to verify incremental translation works correctly.

## Expected Behavior

When this commit is pushed:
1. Translation PR should be **updated** with a new commit
2. New commit should ONLY contain:
   - `cn/test-clean-second.md`
   - `jp/test-clean-second.md`
   - `docs.json`
3. First file should NOT be re-translated
4. NO English files should appear
5. Git history preserved (no force-push)

## Success Criteria

✅ Translation PR has exactly 2 commits
✅ Second commit is clean (no English files, no unnecessary modifications)
✅ First translated files unchanged
✅ Proper Last-Processed-Commit tracking
