---
title: Clean Incremental Test - Third File
description: Final verification of incremental translation
---

# Clean Incremental Test - Third File

This is the **third file** to verify incremental translation works after all fixes.

## Expected Behavior

When this commit is pushed:
1. Translation PR gets a **second commit** (not a new single commit)
2. Second commit should ONLY contain:
   - `cn/test-clean-third.md`
   - `jp/test-clean-third.md`
   - `docs.json`
3. Previous translated files should remain unchanged
4. NO English files in commit
5. Git history preserved

## Final Success Criteria

✅ Translation PR has exactly 2 commits
✅ Second commit is clean and incremental
✅ No force-push occurred
✅ All fixes working correctly
