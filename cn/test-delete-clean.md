---
title: 测试 DELETE 操作（清理）
description: 测试文件删除与自动清理
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](/en/test-delete-clean)。</Note>

# 测试 DELETE 操作

这是对修复后工作流的 DELETE 操作的全新测试。

## 目的

此文件将：
1. 在初始提交中创建
2. 翻译为 cn/jp
3. 在增量提交中删除
4. 清理应传播到翻译 PR

## 预期行为

当此文件被增量删除时：
- **分析工作流**触发（无路径过滤器阻止）
- **更新工作流**从翻译 PR 中删除文件
- **cn/test-delete-clean.md** 和 **jp/test-delete-clean.md** 被删除
- **docs.json** 更新以从所有语言部分删除条目

## 测试步骤

1. ✅ 初始提交：添加此文件 + docs.json 条目
2. ⏳ 等待翻译 PR
3. ⏳ 增量：删除文件 + 从 docs.json 中移除
4. ⏳ 验证翻译 PR 已更新删除内容