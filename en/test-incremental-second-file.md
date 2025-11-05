---
title: Second Test File - Incremental Update
description: This file tests incremental translation by being added in a second commit.
---

# Second Test File

This document was added in the **second commit** to verify incremental translation.

## Purpose

When this file is pushed, the workflow should:

1. Detect only this file as changed (not the first file)
2. Translate only this new file
3. Append a new commit to the translation PR (not force-push)
4. Update the `Last-Processed-Commit` tracker

## Expected Behavior

The translation PR should:
- Have **2 commits** (initial + this update)
- NOT re-translate the first file
- Include a comment with the new commit SHA

## Verification

Check the translation PR commit history to verify:
- Commit 1: Initial translations
- Commit 2: Update translations for this commit only
