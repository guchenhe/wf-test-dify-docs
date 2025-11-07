---
title: Test Add File
description: This is a test file to verify sync workflow handles new file additions correctly
---

# Test Add File

This file tests the sync workflow's ability to:
- Create sync PRs for new files
- Translate content to cn and jp
- Update docs.json navigation

## Test Content

Lorem ipsum dolor sit amet, consectetur adipiscing elit. This content will be translated to Chinese and Japanese.

### Features to Test

- File creation detection
- Translation workflow execution
- docs.json synchronization
- PR comment generation

## Expected Behavior

When this file is added:
1. Sync workflow should trigger
2. File should be translated to cn/test-scenarios/test-add.md and jp/test-scenarios/test-add.md
3. docs.json should be updated with navigation entries
4. Sync PR should be created with appropriate comments
