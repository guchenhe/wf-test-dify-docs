---
title: Final Validation Test - File One
description: Testing complete workflow with docs.json fix
---

# Final Validation Test - File One

This file tests the complete translation workflow with the docs.json sync fix applied.

## Expected Behavior

**Initial PR (Execute Workflow):**
- Analyze workflow generates sync_plan with this file
- Execute workflow creates translation PR
- Translation commit includes:
  - ✅ cn/test-final-one.md
  - ✅ jp/test-final-one.md
  - ✅ docs.json (with cn/jp entries for this file)

## Success Criteria

✅ Translation PR created
✅ docs.json properly synced in initial commit
