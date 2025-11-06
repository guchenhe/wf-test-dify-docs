---
title: Final Validation Test - File Three
description: Testing smart merge that preserves all previous entries
---

# Final Validation Test - File Three

This third file tests the smart merge logic for docs.json.

## Expected Behavior

**Incremental Update (Update Workflow with Smart Merge):**
- Update workflow merges docs.json:
  - English section from PR HEAD (all 3 files)
  - cn/jp sections from translation branch (preserving existing entries)
- Translates ONLY this file
- Translation commit includes:
  - ✅ cn/test-final-three.md (Added)
  - ✅ jp/test-final-three.md (Added)
  - ✅ docs.json (Modified) with:
    - cn/test-final-one (preserved from first commit)
    - cn/test-final-two (preserved from second commit)
    - cn/test-final-three (added in this commit)

## Success Criteria

✅ All previous entries preserved (test-final-one, test-final-two)
✅ New entry added (test-final-three)
✅ No re-translation of existing files
✅ Smart merge working correctly
