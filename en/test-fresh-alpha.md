---
title: Fresh Workflow Test - Alpha File
description: Testing the fully refactored Python-based translation workflow
---

# Fresh Workflow Test - Alpha File

This is a completely fresh test to verify the refactored translation system works end-to-end.

## Testing Objectives

1. ✅ Verify Python script creates translation branch correctly
2. ✅ Verify English files are properly removed from commits
3. ✅ Verify translations are generated for both cn and jp
4. ✅ Verify docs.json is updated correctly

## What We're Testing

The new `translate_pr.py` script consolidates all translation logic into a single, reusable Python script that both workflows use:

- **Execute workflow**: For new PRs (triggered by analyze workflow)
- **Update workflow**: For PR synchronize events (incremental updates)

## Expected Result

Translation PR should be created with:
- Clean commits (no English files)
- Proper translations in cn/ and jp/ directories
- Updated docs.json with correct navigation structure
- Proper commit message with Last-Processed-Commit tracking
