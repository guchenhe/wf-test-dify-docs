---
title: 测试同步一次性 Markdown
description: 用于验证一次性 markdown 同步功能的测试文件
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-sync-one-off-markdown.md)。</Note>

# 测试同步一次性 Markdown

这是一个用于验证自动多语言同步系统的测试文档。

## 目的

此测试验证以下内容：
- 新的英文 markdown 文件触发同步工作流
- 为中文（cn）和日文（jp）生成翻译
- 自动创建同步 PR
- 正确更新 docs.json

## 测试详情

**测试类型**：一次性新建 markdown 文件
**预期行为**：应创建包含 cn + jp 翻译的同步 PR
**文件路径**：`en/test-sync-one-off-markdown.md`

## 内容部分

### 第 1 部分：基础文本
这是一个用于测试基本翻译的简单段落。

### 第 2 部分：代码示例
```python
def hello_world():
    print("Hello, World!")
```

### 第 3 部分：列表
- 项目 1
- 项目 2
- 项目 3

此测试文件应被翻译并同步到其他语言目录。