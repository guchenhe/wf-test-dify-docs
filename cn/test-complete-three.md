---
title: 完整流程测试 - 文件三
description: 最终验证所有条目已保留
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-complete-three.md)。</Note>

# 完整流程测试 - 文件三

第三个文件完成端到端验证。

## 预期行为

**更新工作流（最终测试）：**
- 智能合并保留所有先前条目
- docs.json 应包含：
  - cn/test-complete-one（从提交 1 中保留）
  - cn/test-complete-two（从提交 2 中保留）
  - cn/test-complete-three（在此提交中添加）

**成功标准：**
✅ 所有三个文件都保留在 cn/jp 导航中
✅ 完整工作流端到端验证完成