---
title: 最终验证测试 - 文件二
description: 测试带有 docs.json 修复的增量更新
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-final-two.md)。</Note>

# 最终验证测试 - 文件二

第二个文件用于测试带有 docs.json 同步修复的增量更新工作流。

## 预期行为

**增量更新（更新工作流）：**
- 更新工作流仅检测比较范围内的这个新文件
- 仅翻译此文件（不重新翻译 test-final-one.md）
- 翻译提交包括：
  - ✅ cn/test-final-two.md（已添加）
  - ✅ jp/test-final-two.md（已添加）
  - ✅ **docs.json（已修改）** - 包含此文件的 cn/jp 条目

## 成功标准

✅ 仅翻译新文件
✅ docs.json 通过修复正确同步
✅ 不重新翻译第一个文件