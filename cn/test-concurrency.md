---
title: "并发测试"
description: "使用并发组测试快速更新"
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-concurrency.md)。</Note>

# 并发测试

此文件用于测试翻译工作流中的并发控制。

## 版本 5 - 测试 head_branch 修复

更新的内容 - 提交 5。测试使用 head_branch 修复的并发。

现在应该可以正常工作，因为：
- 并发组使用 `github.event.workflow_run.head_branch`
- 相同的 PR 分支 = 相同的并发组
- 工作流将正确排队
- 不再有取消的工作流