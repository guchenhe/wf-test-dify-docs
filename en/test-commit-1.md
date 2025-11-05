---
title: First Commit Test
description: Testing incremental translation with the first commit.
---

# First Commit Test

This is the **first commit** to verify the new incremental translation workflow.

## What Should Happen

1. Translation PR should be created
2. This file should be translated to cn/ and jp/
3. Commit message should include `Last-Processed-Commit: <SHA>`

## Next Step

After this PR is created, we'll push a second commit with another file to verify that only the new file gets translated (not this one again).
