---
title: Test Sync PR Closure
description: Test file for validating PR closure and cleanup workflow
---

# Test Sync PR Closure

This is a test document to validate the PR closure cleanup workflow.

## Purpose

This test validates:
- Cleanup workflow triggers when original PR is closed
- Sync PR is automatically closed with appropriate message
- Different messages for merged vs closed PRs
- Reopening behavior (if applicable)

## Test Procedure

### Step 1: Create PR
Create this PR with English docs changes.

### Step 2: Wait for Sync PR
Wait for the Execute workflow to create the sync PR.

### Step 3: Close Original PR
Close this PR **without merging** to test the cleanup workflow.

### Step 4: Verify Cleanup
Verify that:
- Cleanup workflow detects the closure
- Sync PR is automatically closed
- Appropriate comment is posted to sync PR
- Comment indicates original PR was closed (not merged)

### Step 5: Reopen (Optional)
If testing reopen behavior:
- Reopen this PR
- Verify sync workflow resumes

## Expected Cleanup Message

When closed without merging:
> ❌ Original PR #XXX was closed. If it reopens, sync will resume automatically.

When merged:
> ✅ Original PR #XXX was merged. You can still merge this sync PR independently if translations are ready.

## Content

This is test content that will be translated to demonstrate the full workflow before closure testing.
