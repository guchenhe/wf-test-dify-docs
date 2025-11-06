---
title: 完整流程测试 - 文件二
description: 测试智能合并保留文件一
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-complete-two.md)。</Note>

# 完整流程测试 - 文件二

第二个文件测试增量更新的智能合并逻辑。

## 预期行为

**更新工作流（智能合并）：**
- 合并 docs.json：英文来自 PR，中文/日文来自翻译分支
- 仅翻译此文件
- docs.json 应包含：
  - cn/test-complete-one（保留）
  - cn/test-complete-two（新增）

**成功标准：**
✅ 文件一在中文/日文导航中保留
✅ 文件二添加到中文/日文导航