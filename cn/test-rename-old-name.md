---
title: 测试重命名操作（旧名称）
description: 使用精确协调测试文件重命名
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](/en/test-rename-old-name)。</Note>

# 测试重命名操作

此文件测试精确协调中的重命名操作。

## 目的

此文件将：
1. 以名称 `test-rename-old-name.md` 创建
2. 使用相同的基本名称翻译为 cn/jp
3. 重命名为 `test-rename-new-name.md`
4. 重命名应传播到 cn/jp 文件

## 预期行为

当此文件进行增量重命名时：
- **精确协调**检测到重命名
- 执行的重命名：在同一位置删除 + 添加
- **扩展名保留**：.md → .md（或 .mdx → .mdx）
- **cn/test-rename-old-name.md** → **cn/test-rename-new-name.md**
- **jp/test-rename-old-name.md** → **jp/test-rename-new-name.md**

## 重命名检测

系统通过以下方式检测重命名：
- 文件从 docs.json 中删除
- 文件在同一位置添加（相同的 group_path）
- 在导航数组中的位置相同
- 扩展名类型保留