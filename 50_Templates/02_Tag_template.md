---
title: "Tag設計: {{title}}"
created: {{date}}
tags: [Tag設計, テンプレート分岐, 再利用性]
related: [[50.templates/Tag_Template]], [[README/{{title}}]], [[Draft/{{title}}]]
---

# 🏷️ タグ定義
- タグ名：`#{{title}}`
- 用途：このタグは {{title}} に関連するノート・テンプレート・Draft を分類・抽出するために使用します。
- 分類：`#draft`, `#workflow`, `#config`, `#idea`, `#失敗資産化` などと併用可能

# 🧩 関連テンプレート
- 使用テンプレート：[[50.templates/Draft_Note]], [[50.templates/Workflow_Log_Template]], [[50.templates/README_Template]]
- 分岐元：`#draft`
- 分岐理由：{{title}} に特化した運用・構造化が必要なため

# 🔍 Dataview連携例
```dataview
table title, status, created
from "Draft"
where contains(tags, "{{title}}")
sort created desc