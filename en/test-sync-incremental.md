---
title: Test Sync Incremental Updates
description: Test file for validating incremental sync with multiple commits
---

# Test Sync Incremental Updates

This is a test document to validate incremental sync functionality with multiple rapid commits.

## Commit 1: Initial Content

This is the initial version of the test file.

### Purpose
- Validate incremental sync with multiple commits
- Test concurrency control (first and last commit should sync, middle skipped)
- Verify Last-Processed-Commit tracking

## Content

This is commit 1 content. More commits will follow rapidly.

## Commit 2: Middle Update

This is the second commit. According to the concurrency control, this commit should be SKIPPED because a third commit will arrive before this finishes processing.

**Expected**: Cancellation notification posted to PR.
