---
title: 同期プラン生成テスト - ファイル2
description: 再翻訳なしの増分更新のテスト
---

<Note> ⚠️ このドキュメントはAIによって自動翻訳されています。不正確な部分がある場合は、[英語版](../en/test-sync-gen-two.md)を参照してください。</Note>

# 同期プラン生成テスト - ファイル2

この2つ目のファイルは、`SyncPlanGenerator`を使用した増分更新をテストします。

## 期待される動作

このファイルが追加された場合：
- 更新ワークフローはSyncPlanGeneratorを使用してsync_planを生成する必要があります
- **このファイルのみ**がfiles_to_sync（Aステータス）に含まれる必要があります
- test-sync-gen-one.mdは**再翻訳されない**必要があります
- 翻訳PR #104は以下の1つのコミットを受け取る必要があります：
  - ✅ cn/test-sync-gen-two.md（追加）
  - ✅ jp/test-sync-gen-two.md（追加）
  - ❌ cn/test-sync-gen-one.md（変更されないこと）
  - ❌ jp/test-sync-gen-one.md（変更されないこと）

## 成功基準

✅ A/Mファイルのみが翻訳される
✅ 変更されていないファイルの再翻訳がない
✅ 適切なdocs.jsonの同期（構造が変更された場合）