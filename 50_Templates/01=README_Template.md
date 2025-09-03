---
title: "README: Vault運用テンプレート設計思想"
created: {{date}}
tags: [README, 設計思想, Vault運用]
related: 
  - [[50.templates/README_Template]]
  - [[50.templates/テンプレート設計メモ]]
  - [[50.templates/テンプレート分岐記録]]
  - [[Tag/設計思想]]
---

# 🧭 概要
このREADMEは、Vault運用におけるテンプレート設計・タグ分岐・構造化思想・失敗資産化の方針を明文化するものです。Draft育成型ワークフローを軸に、現場主義・即時性・再利用性・説明責任を支える構造を構築します。

# 🏗️ Vault構造とテンプレート群
- テンプレート群：`50.templates/01〜10`
- 構造設計：`config/assets/logs` を中心に PowerShell連携で自動生成
- 音声入力：Whisper → Markdown → Vault保存の自動化
- テンプレート分岐：Draft → README → Tag → Workflow_Log → Failure

# 🧩 テンプレート一覧（概要）

| No. | テンプレート名 | 用途 | 関連タグ |
|-----|----------------|------|-----------|
| 01  | README_Template | 設計思想の明文化 | `#README`, `#設計思想` |
| 02  | Tag_Template | タグ設計と分岐管理 | `#Tag設計`, `#再利用性` |
| 03  | Workflow_Log_Template | 運用改善・失敗記録 | `#workflow`, `#失敗資産化` |
| 04  | Asset_Config_Template | Vault構造・命名規則 | `#config設計`, `#PowerShell連携` |
| 05  | Idea_Template | Draft化前の思考記録 | `#idea`, `#draft候補` |
| 06  | Meeting_Note_Template | 対話記録・意思決定 | `#meeting`, `#workflow` |
| 07  | Reference_Template | 外部資料の構造化 | `#reference`, `#draft候補` |
| 08  | Failure_Template | 失敗の記録と資産化 | `#failure`, `#運用改善` |
| 09  | テンプレート設計メモ | テンプレート思想の記録 | `#template設計`, `#meta記録` |
| 10  | テンプレート分岐記録 | 分岐履歴と変更点 | `#template分岐`, `#設計履歴` |

# 🔧 運用方針
- `.gitignore` により `*.env`, `*.log` はGit管理から除外
- Push Protectionにより誤送信防止
- READMEに設計思想・構造・運用ルールを明記
- DraftやWorkflow_Logと連携し、構造変更履歴を記録
- Dataviewによりテンプレート群・タグ・Draftの育成状況を可視化

# 🔍 Dataview連携（例）

```dataview
table title, created, tags
from "50.templates"
where contains(tags, "template")
sort created desc