---
title: 最终验证测试 - 文件三
description: 测试保留所有先前条目的智能合并
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-final-three.md)。</Note>

# 最终验证测试 - 文件三

第三个文件测试 docs.json 的智能合并逻辑。

## 预期行为

**增量更新（使用智能合并更新工作流）：**
- 更新工作流合并 docs.json：
  - 来自 PR HEAD 的英文部分（所有 3 个文件）
  - 来自翻译分支的 cn/jp 部分（保留现有条目）
- 仅翻译此文件
- 翻译提交包括：
  - ✅ cn/test-final-three.md（已添加）
  - ✅ jp/test-final-three.md（已添加）
  - ✅ docs.json（已修改）包含：
    - cn/test-final-one（从第一次提交保留）
    - cn/test-final-two（从第二次提交保留）
    - cn/test-final-three（在此提交中添加）

## 成功标准

✅ 所有先前条目已保留（test-final-one、test-final-two）
✅ 新条目已添加（test-final-three）
✅ 不重新翻译现有文件
✅ 智能合并正常工作