---
title: 同步计划生成器测试 - 文件二
description: 测试增量更新且不重新翻译
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-sync-gen-two.md)。</Note>

# 同步计划生成器测试 - 文件二

此第二个文件测试使用 `SyncPlanGenerator` 的增量更新。

## 预期行为

当添加此文件时：
- 更新工作流应使用 SyncPlanGenerator 生成 sync_plan
- **仅此文件**应在 files_to_sync 中（A 状态）
- test-sync-gen-one.md **不应**被重新翻译
- 翻译 PR #104 应收到一个提交，包含：
  - ✅ cn/test-sync-gen-two.md（已添加）
  - ✅ jp/test-sync-gen-two.md（已添加）
  - ❌ cn/test-sync-gen-one.md（不应被修改）
  - ❌ jp/test-sync-gen-one.md（不应被修改）

## 成功标准

✅ 仅翻译 A/M 文件
✅ 不重新翻译未更改的文件
✅ 正确同步 docs.json（如果结构发生变化）