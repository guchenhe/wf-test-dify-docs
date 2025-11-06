---
title: 同步计划生成器测试 - 文件一
description: 测试新的 SyncPlanGenerator 以实现一致的同步逻辑
---

<Note> ⚠️ 本文档由 AI 自动翻译。如有任何不准确之处，请参考[英文原版](../en/test-sync-gen-one.md)。</Note>

# 同步计划生成器测试 - 文件一

使用 `SyncPlanGenerator` 类测试重构后的同步计划生成。

## 变更内容

1. **集中化逻辑**：同步计划生成从内联 YAML 移至 Python 类
2. **一致的行为**：执行和更新工作流使用相同的逻辑
3. **适当的过滤**：仅翻译 A/M（添加/修改）文件

## 预期行为

**初始 PR：**
- 分析工作流使用 SyncPlanGenerator 生成 sync_plan
- 执行工作流使用生成的 sync_plan
- 仅使用此文件创建翻译 PR

**增量更新（下一个文件）：**
- 更新工作流使用 SyncPlanGenerator 生成 sync_plan
- 仅应翻译新文件
- 此文件（test-sync-gen-one.md）不应重新翻译