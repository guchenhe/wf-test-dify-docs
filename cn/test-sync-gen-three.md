---
title: 同步计划生成器测试 - 文件三
description: 使用 Last-Processed-Commit 修复的最终测试
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-sync-gen-three.md)。</Note>

# 同步计划生成器测试 - 文件三

第三个文件测试了修复后的更新工作流，该工作流能够正确地从 git log 中提取 Last-Processed-Commit。

## 预期行为

修复后：
- 更新工作流从上一个提交 (f7be4407) 中提取 Last-Processed-Commit
- 比较范围：f7be4407...{new_commit}
- **仅此文件**应被翻译
- test-sync-gen-one.md 和 test-sync-gen-two.md 不应被重新翻译

## 成功标准

✅ 正确的比较范围（从上次处理的提交开始）
✅ 仅翻译新文件 (test-sync-gen-three.md)
✅ 不重新翻译之前的文件