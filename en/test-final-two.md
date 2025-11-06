---
title: Final Validation Test - File Two
description: Testing incremental update with docs.json fix
---

# Final Validation Test - File Two

This second file tests the incremental update workflow with the docs.json sync fix.

## Expected Behavior

**Incremental Update (Update Workflow):**
- Update workflow detects only this new file in comparison range
- Translates ONLY this file (no re-translation of test-final-one.md)
- Translation commit includes:
  - ✅ cn/test-final-two.md (Added)
  - ✅ jp/test-final-two.md (Added)
  - ✅ **docs.json (Modified)** - with cn/jp entries for this file

## Success Criteria

✅ Only new file translated
✅ docs.json properly synced with the fix
✅ No re-translation of first file
