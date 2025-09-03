---
title: "Meeting Note: {{title}}"
created: {{date}}
tags: [meeting, 対話記録, draft候補]
related: [[50.templates/Meeting_Note_Template]], [[Draft/{{title}}]], [[Workflow_Log/{{title}}]]
---

# 🗓️ 基本情報
- 日付：{{date}}
- タイトル：{{title}}
- 参加者：nori, {{others}}
- 実施形式：対面 / オンライン / 音声入力（Whisper連携）

# 🧭 議題・目的
- 主な議題：
  - {{agenda_1}}
  - {{agenda_2}}
- 目的：
  - 情報共有 / 意思決定 / 構造化 / Draft化検討

# 📝 内容記録
- 要点・発言：
  - {{point_1}}
  - {{point_2}}
- 気づき・仮説：
  - {{insight_1}}
  - {{hypothesis_1}}

# ✅ 決定事項・アクション
- 決定事項：
  - [ ] {{decision_1}}
  - [ ] {{decision_2}}
- 次アクション：
  - [ ] Draft作成 → [[Draft/{{title}}]]
  - [ ] README更新 → [[README/{{title}}]]
  - [ ] タグ分岐 → `#{{tag}}`

# 🧠 関連テンプレート・タグ
- 使用テンプレート：`Meeting_Note_Template`
- 関連タグ：`#meeting`, `#draft候補`, `#workflow`
- 関連テンプレート：[[50.templates/Draft_Note]], [[50.templates/Workflow_Log_Template]]

# 📌 備考
このノートは対話の記録として保存され、Draft化・運用改善・タグ設計の起点として活用されます。Dataviewで `#meeting` タグを抽出することで、過去の対話履歴を一覧できます。