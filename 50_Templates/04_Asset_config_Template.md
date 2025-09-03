---
title: "Asset Config: {{title}}"
created: {{date}}
tags: [config設計, PowerShell連携, Vault構造]
related: [[50.templates/Asset_Config_Template]], [[README/{{title}}]], [[Workflow_Log/{{title}}]]
---

# 🗂️ 構成概要
Vault内の `config/assets/logs` フォルダ設計と運用方針を記述するテンプレート。

# 📁 フォルダ構成
（ここにフォルダツリー構造を記述）

# 🧾 命名規則
- ファイル名：`workflow_YYYYMMDD.log`, `vault_meta.md`, `asset_init.ps1`
- 拡張子：`.md`, `.json`, `.ps1`, `.env`
- 接頭辞：用途別に `workflow_`, `vault_`, `asset_` を使用

# ⚙️ PowerShell連携
- スクリプト例：`asset_init.ps1` により config/assets/logs を自動生成
- 実行タイミング：Vault初期化時、テンプレート分岐時
- 引数設計：`-vaultPath`, `-templateType`, `-logEnable`

# 🧠 運用方針
- `.gitignore` により `*.env`, `*.log` はGit管理から除外
- Push Protectionにより誤送信防止
- READMEに構造・思想・運用ルールを明記
- DraftやWorkflow_Logと連携し、構造変更履歴を記録

# 📌 備考
このテンプレートは構造設計のベースとして使用され、Vault運用の即時性・再利用性・説明責任を支える技術的基盤となります。