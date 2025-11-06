---
title: Complete Flow Test - File Two
description: Testing smart merge preserves file one
---

# Complete Flow Test - File Two

This second file tests the smart merge logic for incremental updates.

## Expected Behavior

**Update Workflow (Smart Merge):**
- Merge docs.json: English from PR, cn/jp from translation branch
- Translate only this file
- docs.json should have:
  - cn/test-complete-one (preserved)
  - cn/test-complete-two (added)

**Success Criteria:**
✅ File one preserved in cn/jp navigation
✅ File two added to cn/jp navigation
