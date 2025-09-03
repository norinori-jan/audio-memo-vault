# audio-memo-vault

このVaultは、音声メモの記録・分類・再利用を目的とした構造化ノート群です。  
録音は `vaults/Recording` に一時保存され、用途に応じて本Vaultまたは他Vaultに振り分けられます。

## 構成
- `50_Templates/`：録音ログテンプレート群
- `60_Meta/`：タグ設計・分類ルール
- `98_Experiments/`：録音運用の試行記録
- `99_Scripts/`：振り分けスクリプト（PowerShell）

## 運用フロー
1. 録音は `vaults/Recording` に保存
2. ファイル名で用途判定（業務・思考・日常）
3. スクリプトで Vault に振り分け
4. Whisperで文字起こし → テンプレートノート生成
5. Dataviewで抽出・分析

## Git管理方針
- `.m4a` や `.obsidian/` は `.gitignore` により除外
- 管理対象はテンプレート・構造・スクリプトのみ

## 思考ログの昇格ルール

録音ログや思考メモのうち、以下の条件を満たすものは `chiteki-vault` に昇格させる：

- タグに `#問い`, `#抽象`, `#概念` が含まれる
- テンプレートに `vault-origin: audio-memo-vault` が記載されている
- `status: draft` → `status: promote` に変更されたもの
- Dataviewで抽出された「昇格候補」一覧に含まれる

昇格後は `chiteki-vault/01_Concepts/` または `03_Reflections/` に移動し、再構成される