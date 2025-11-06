---
title: "并发测试"
description: "使用并发组测试快速更新"
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-concurrency.md)。</Note>

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处,请参考[英文原版](../en/test-concurrency.md)。</Note>

# 并发测试

此文件用于测试翻译工作流中的并发控制。

## 版本 7 - 第三次快速测试

更新的内容 - 提交 7。第三次连续提交。

最终验证:
- 三个工作流按顺序排队(提交 5、6、7)
- 全部使用并发组: `docs-translation-test/concurrency-rapid-updates`
- 应该全部完成而不被取消
- 翻译 PR 应该成功创建/更新