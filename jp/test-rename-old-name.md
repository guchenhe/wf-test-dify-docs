---
title: RENAME操作のテスト（旧名称）
description: 外科的照合によるファイル名変更のテスト
---

<Note> ⚠️ このドキュメントはAIによって自動翻訳されています。不正確な部分がある場合は、[英語版](/en/test-rename-old-name)を参照してください。</Note>

# RENAME操作のテスト

このファイルは、外科的照合におけるRENAME操作をテストします。

## 目的

このファイルは以下のように処理されます：
1. `test-rename-old-name.md`という名前で作成
2. 同じベース名でcn/jpに翻訳
3. `test-rename-new-name.md`に名前変更
4. 名前変更はcn/jpファイルに伝播されるべき

## 期待される動作

このファイルが段階的に名前変更される場合：
- **外科的照合**が名前変更を検出
- 実行される名前変更：同じ場所で削除+追加
- **拡張子が保持される**：.md → .md（または.mdx → .mdx）
- **cn/test-rename-old-name.md** → **cn/test-rename-new-name.md**
- **jp/test-rename-old-name.md** → **jp/test-rename-new-name.md**

## 名前変更の検出

システムは以下の方法で名前変更を検出します：
- docs.jsonからファイルが削除される
- 同じ場所（同じgroup_path）にファイルが追加される
- ナビゲーション配列内の同じ位置
- 拡張子タイプが保持される