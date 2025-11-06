---
title: Sync Plan Generator Test - File Two
description: Testing incremental update with no re-translation
---

# Sync Plan Generator Test - File Two

This second file tests the incremental update with `SyncPlanGenerator`.

## Expected Behavior

When this file is added:
- Update workflow should generate sync_plan using SyncPlanGenerator
- **ONLY this file** should be in files_to_sync (A status)
- test-sync-gen-one.md should **NOT** be re-translated
- Translation PR #104 should receive ONE commit with:
  - ✅ cn/test-sync-gen-two.md (Added)
  - ✅ jp/test-sync-gen-two.md (Added)
  - ❌ cn/test-sync-gen-one.md (Should NOT be modified)
  - ❌ jp/test-sync-gen-one.md (Should NOT be modified)

## Success Criteria

✅ Only A/M files are translated
✅ No re-translation of unchanged files
✅ Proper docs.json sync (if structure changed)
