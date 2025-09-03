---
title: "Workflow Log: {{title}}"
created: {{date}}
tags: [workflow, 運用改善, 失敗資産化]
related: [[50.templates/Workflow_Log_Template]], [[Draft/{{title}}]], [[README/{{title}}]]
---

# 📝 実施内容
- 実施日：{{date}}
- 実施者：nori
- 内容概要：{{title}} に関する運用・構成・連携などの実施内容を記録

# ⚠️ 課題・失敗
- 発生した課題：
  - [ ] 技術的な問題（例：Whisper連携が失敗）
  - [ ] 運用上の不整合（例：タグ分岐が未反映）
- 原因分析：
  - DraftやREADMEとの連携不足
  - テンプレート設計の粒度が不適切

# 🔧 改善案・対応方針
- 改善案：
  - Draftテンプレートに `Whisper連携` セクションを追加
  - Tag_Template に `#workflow` を追加し抽出性向上
- 対応方針：
  - 次回運用時にテンプレート分岐を明示
  - READMEに運用方針を追記

# 🧠 関連Draft・テンプレート
- Draftリンク：[[Draft/{{title}}]]
- 使用テンプレート：[[50.templates/Draft_Note]], [[50.templates/README_Template]]
- 関連タグ：`#workflow`, `#失敗資産化`, `#運用改善`

# 📌 備考
このログは運用改善の記録として保存され、再発防止・再利用・説明責任のために活用されます。Dataviewで抽出・可視化可能。