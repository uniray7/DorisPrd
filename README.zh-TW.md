---
doc_id: DOC-ROOT
document_type: Index
audience: Contributors
status: Draft
revision: 0.1
reviewer: Requester
applies_to: Repository
language: zh-TW
---

# OLAP Service 與 Data Ingestion Pipeline 文件

[English](README.en.md)

本 repository 管理以 Apache Doris 為基礎的公司內部 OLAP Service 與 Data Ingestion Pipeline 文件。

## 閱讀入口

- [對外文件](docs/external/README.zh-TW.md)：給公司其他部門的使用者，涵蓋服務規格、申請、審核、使用與排查。
- [內部文件](docs/internal/README.zh-TW.md)：給團隊，涵蓋整體 PRD、Feature Spec、RFC、Architecture 與 Data Flow。
- [文件生成流程](docs/governance/authoring-workflow.zh-TW.md)、[參考資料規範](docs/governance/reference-policy.zh-TW.md)、[術語表](docs/governance/glossary.zh-TW.md)。
- [OpenCode skill](.opencode/skills/service-documentation/SKILL.zh-TW.md)：AI 文件協作入口。

## 目錄地圖

```text
docs/
├── governance/                 文件流程、來源規範與術語
├── external/
│   ├── service-specs/          對外能力與服務限制
│   ├── getting-started/        申請、審核與首次使用
│   ├── user-guides/            OLAP、monitoring 與 logs 操作
│   ├── policies/              使用規範
│   └── support/               問題排查
└── internal/
    ├── prd/                   一份整體 PRD
    ├── feature-specs/         功能行為與驗收
    ├── rfcs/                  設計決策與取捨
    ├── architecture/          系統與部署設計
    └── data-flows/            資料路徑與行為
```

## 文件狀態與維護

- 使用者已確認目錄架構；各文件目前為 `Draft`。文件骨架不代表規格已核准、實作已驗證或功能已上線。
- 文件以 `.zh-TW.md`／`.en.md` 成對維護；每對共用文件 ID、revision 與狀態。中文保留英文技術術語。
- 採一份整體 PRD；本 repository 不納入維運 Runbook。
- `external` 表示公司其他部門，不表示公開網際網路。對外目錄內的草稿尚未發布。
- Pipeline 四個預留目錄僅放 `.gitkeep`，不填入機密原始文件或推測內容。其他功能有依賴時，再向使用者詢問必要且適合記錄的資訊。
- 各文件自行記錄待釐清事項；跨文件的重要設計決策才開 RFC。

## 已確認的文件決策

來源：使用者於本次文件架構討論中的確認；審閱者為 Requester。此處記錄的是文件組織決策，不是產品規格核准。

| ID | 決策 | 理由／背景 |
| --- | --- | --- |
| DOC-DEC-001 | 依讀者分層，再依文件用途分類 | 區分使用者文件與團隊設計文件。 |
| DOC-DEC-002 | 使用一份整體 PRD | 使用者選定的 PRD 粒度。 |
| DOC-DEC-003 | 不納入維運文件 | 使用者確認的 repository 範圍。 |
| DOC-DEC-004 | 建立雙語輕量骨架，Pipeline 保持空白 | 可看見文件缺口，同時保留機密文件邊界。 |

## 待釐清事項與下一步

- 正式產品名稱尚未決定，`service-platform` 只是整體 PRD 的檔名。
- 從[整體 PRD](docs/internal/prd/service-platform.zh-TW.md) 釐清使用者、核心情境、範圍與優先順序，再補齊相關規格。
