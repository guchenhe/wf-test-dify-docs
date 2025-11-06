---
title: 全新增量测试 - 第一个文件
description: 使用修复的工作流测试增量翻译 - 第一个文件
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-fresh-incremental-first.md)。</Note>

# 全新增量翻译测试 - 第一个文件

这是我们全新增量翻译测试中的**第一个文件**，包含了英文文件移除修复。

## 预期行为

当创建此 PR 时：
1. 应创建翻译 PR
2. 此文件应被翻译到 `cn/` 和 `jp/`
3. 翻译提交应仅包含：
   - `cn/test-fresh-incremental-first.md`
   - `jp/test-fresh-incremental-first.md`
   - `docs.json`
4. 翻译提交不应包含任何 `en/` 文件
5. 提交消息应包含 `Last-Processed-Commit: <SHA>`

## 下一步

在创建翻译 PR 后，我们将推送**第二个文件**以验证增量更新是否正常工作。