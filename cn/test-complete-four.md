---
title: 完整流程测试 - 文件四
description: 测试格式保留的智能合并
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-complete-four.md)。</Note>

# 完整流程测试 - 文件四

第四个文件测试智能合并是否保留 docs.json 的格式。

## 预期行为

**更新工作流（格式保留合并）：**
- 智能合并使用 save_json_with_preserved_format()
- docs.json 差异应该是最小的（仅实际更改）
- 没有巨大的格式差异

**成功标准：**
✅ docs.json 中的格式已保留
✅ 干净、可读的差异
✅ cn/jp 导航中的所有四个条目