---
title: "{{title}}"
created: {{date}}
tags: [draft, idea, #未分類]
status: "🟡 育成中"
related: [[README/ワークフロー概要]], [[Tag/設計思想]]
---

## 🧠 アイデア概要
{{title}} に関する初期アイデア・仮説・背景などを記述。

## 🔍 育成履歴
- {{date}}: Draft作成
- {{date}}: 初期構造化
- {{date}}: タグ分岐検討

## 🧵 関連テンプレート・タグ
- 使用テンプレート: `Draft Note`
- 関連タグ: `#draft`, `#idea`, `#失敗資産化`

## 🔊 Whisper連携設定
- 使用API：OpenAI Whisper  
- 設定ファイル：`whisper_config.env`  
- 保存場所：Vault内 `99_Scripts/whisper_config.env`  
- 管理方針：  
  - `.gitignore` によりGit管理から除外  
  - READMEに運用思想を明記  
  - Push Protection対策済み  
- 備考：音声入力 → Whisper → Markdown化の自動化ワークフローに使用

## 📌 メモ・補足
自由記述欄。失敗・気づき・再利用ポイントなど。