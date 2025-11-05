---
title: Testing Incremental Translation
description: This file tests the incremental translation workflow with commit-based change detection.
---

# Testing Incremental Translation

This is a test document to verify that the incremental translation workflow works correctly.

## First Addition

This content was added in the first commit. It should be translated when the PR is created.

### Key Features

- Commit-based change detection
- Incremental translation updates
- Preserved translation history
- 1:1 mapping between source and translation commits

## Benefits

The new incremental system provides:

1. **Efficiency**: Only translates changed files
2. **Traceability**: Clear commit mapping
3. **History**: No force-pushes, preserved timeline
4. **Robustness**: Handles force-pushes and rebases gracefully
