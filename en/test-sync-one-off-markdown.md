---
title: Test Sync One-Off Markdown
description: Test file for validating one-off markdown sync functionality
---

# Test Sync One-Off Markdown

This is a test document created to validate the automatic multi-language sync system.

## Purpose

This test verifies that:
- A new English markdown file triggers the sync workflow
- Translations are generated for Chinese (cn) and Japanese (jp)
- A sync PR is created automatically
- The docs.json is updated correctly

## Test Details

**Test Type**: One-off new markdown file
**Expected Behavior**: Sync PR should be created with cn + jp translations
**File Path**: `en/test-sync-one-off-markdown.md`

## Content Sections

### Section 1: Basic Text
This is a simple paragraph to test basic translation.

### Section 2: Code Example
```python
def hello_world():
    print("Hello, World!")
```

### Section 3: Lists
- Item 1
- Item 2
- Item 3

This test file should be translated and synchronized to other language directories.
