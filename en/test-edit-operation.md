---
title: Test EDIT Operation
description: Testing file modification with context-aware translation
---

# Test EDIT Operation

This file tests the EDIT operation in the translation workflow.

## Baseline Content - MODIFIED

This content has been significantly modified to test context-aware translation! The incremental update should use the existing translation plus the git diff.

### Context-Aware Translation

When this file is modified incrementally:
1. The analyze workflow detects the change
2. The update workflow uses **context-aware translation**
3. Translation uses: existing translation + git diff
4. More efficient than re-translating the entire file
5. **NEW**: This approach reduces API costs and translation time

## Updated Version (v2)

This is now version 2 of the test file with substantial modifications:

### New Section: How It Works

The context-aware translation system:
- Detects which parts of the file changed
- Provides the translator with the existing translation
- Shows the git diff to highlight changes
- Generates updated translation maintaining consistency

### Benefits

1. **Efficiency**: Only modified sections need re-translation
2. **Consistency**: Existing terminology is preserved
3. **Speed**: Faster than full re-translation
4. **Cost**: Reduces API token usage significantly
