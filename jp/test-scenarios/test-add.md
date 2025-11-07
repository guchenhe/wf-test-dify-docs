---
title: ファイル追加のテスト
description: これは、同期ワークフローが新しいファイルの追加を正しく処理するかを検証するためのテストファイルです
---

<Note> ⚠️ このドキュメントはAIによって自動翻訳されています。不正確な部分がある場合は、[英語版](../../en/test-scenarios/test-add.md)を参照してください。</Note>

# ファイル追加のテスト

このファイルは、同期ワークフローの以下の機能をテストします：
- 新しいファイルに対する同期PRの作成
- コンテンツをcnとjpに翻訳
- docs.jsonナビゲーションの更新

## テストコンテンツ

Lorem ipsum dolor sit amet, consectetur adipiscing elit. このコンテンツは中国語と日本語に翻訳されます。

### テストする機能

- ファイル作成の検出
- 翻訳ワークフローの実行
- docs.jsonの同期
- PRコメントの生成

## 期待される動作

このファイルが追加されたとき：
1. 同期ワークフローがトリガーされる
2. ファイルがcn/test-scenarios/test-add.mdとjp/test-scenarios/test-add.mdに翻訳される
3. docs.jsonがナビゲーションエントリで更新される
4. 適切なコメント付きの同期PRが作成される