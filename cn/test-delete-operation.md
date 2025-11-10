---
title: 测试 DELETE 操作
description: 使用修复的工作流测试文件删除
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](/en/test-delete-operation)。</Note>

# 测试 DELETE 操作

此文件测试修复后的删除处理的 DELETE 操作。

## 测试步骤

1. ✅ **初始提交**：添加此文件并在 docs.json 中添加条目
2. ⏳ **等待翻译**：翻译 PR 应创建 cn/jp 文件
3. ⏳ **删除提交**：删除此文件并从 docs.json 中移除
4. ⏳ **验证删除**：翻译 PR 应删除 cn/jp 文件

## 预期行为

删除修复确保：
- **始终处理删除**通过 `process_deleted_files()`
- **独立于 structure_changed** 标志
- **适用于仅删除的提交**（sync_required=False）

## 修复详情

修复了两个问题：
1. 删除逻辑现在始终运行，而不仅仅是在 docs.json 更改时
2. 仅删除的提交（无添加/编辑）现在可以正确处理

## 删除的文件

当此文件被删除时：
- ✓ `cn/test-delete-operation.md` 已删除
- ✓ `jp/test-delete-operation.md` 已删除
- ✓ 从 docs.json 中移除条目（所有语言）