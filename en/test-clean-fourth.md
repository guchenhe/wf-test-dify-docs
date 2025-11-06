---
title: Clean Incremental Test - Fourth File
description: Final verification with complete fix
---

# Clean Incremental Test - Fourth File

This is the **fourth file** to verify the complete fix works.

## All Fixes Applied

1. ✅ Branch existence check after repo checkout
2. ✅ English file removal with rm -rf before commit
3. ✅ Explicit git reset to unstage any en/ files

## Expected Result

Translation PR should get a third commit with ONLY:
- `cn/test-clean-fourth.md`
- `jp/test-clean-fourth.md`
- `docs.json`
- **NO** English files
