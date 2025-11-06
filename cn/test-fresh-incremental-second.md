---
title: 全新增量测试 - 第二个文件
description: 使用修复的工作流测试增量翻译 - 第二个文件
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-fresh-incremental-second.md)。</Note>

# 全新增量翻译测试 - 第二个文件

这是我们全新增量翻译测试中的**第二个文件**。

## 预期行为

当此提交被推送时：
1. 翻译 PR #86 应该被**更新**（而非强制推送）
2. 翻译 PR 应该**总共有 2 个提交**
3. 第二个提交应该包含新的 `Last-Processed-Commit: <SHA>`
4. 第二个提交应该**仅**包含：
   - `cn/test-fresh-incremental-second.md`
   - `jp/test-fresh-incremental-second.md`
   - `docs.json`（如果导航发生变化）
5. 第二个提交**不应该**包含任何 `en/` 文件
6. 第一个文件**不应该**被重新翻译

## 成功标准

✅ 翻译 PR 有 2 个提交（而非 1 个）
✅ 两个提交有不同的 SHA
✅ Git 历史被保留（无强制推送）
✅ 任何提交中都没有英文源文件