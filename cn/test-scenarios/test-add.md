---
title: 测试添加文件
description: 这是一个测试文件，用于验证同步工作流是否正确处理新文件添加
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../../en/test-scenarios/test-add.md)。</Note>

# 测试添加文件

此文件测试同步工作流的能力：
- 为新文件创建同步 PR
- 将内容翻译为中文和日文
- 更新 docs.json 导航

## 测试内容

Lorem ipsum dolor sit amet, consectetur adipiscing elit. 此内容将被翻译为中文和日文。

### 要测试的功能

- 文件创建检测
- 翻译工作流执行
- docs.json 同步
- PR 评论生成

## 预期行为

当添加此文件时：
1. 同步工作流应该触发
2. 文件应该被翻译到 cn/test-scenarios/test-add.md 和 jp/test-scenarios/test-add.md
3. docs.json 应该更新导航条目
4. 应该创建包含适当评论的同步 PR