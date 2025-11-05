---
title: Fresh Incremental Test
description: Testing incremental translation with a fresh PR
---

# Fresh Incremental Translation Test

This is a fresh test PR to verify the incremental translation workflow works correctly.

## Expected Behavior

1. Translation PR should be created
2. This file should be translated to cn/ and jp/
3. Commit message should include `Last-Processed-Commit: <SHA>`
4. After translation PR is created, we'll push a second commit to verify incremental updates work
