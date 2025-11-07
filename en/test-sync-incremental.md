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

## Commit 3: Final Update

This is the third and final commit. This should trigger the Update workflow and successfully sync to the existing sync PR.

**Expected**:
- Update workflow runs successfully
- Incremental translation from commit 2 to commit 3
- Sync PR updated with new translations
- Success notification posted to both PRs

### Verification Points
1. Commit 1 created the sync PR
2. Commit 2 was cancelled (with notification)
3. Commit 3 updated the sync PR
4. Last-Processed-Commit updated to commit 3 SHA
