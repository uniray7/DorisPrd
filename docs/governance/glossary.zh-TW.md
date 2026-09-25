---
doc_id: GOV-GLOSSARY
document_type: Glossary
audience: Contributors
status: Draft
revision: 0.1
reviewer: Requester
applies_to: Repository
language: zh-TW
---

# 共用術語表

[English](glossary.en.md)

## 文件用語

| 術語 | 本 repository 的意義 |
| --- | --- |
| 內部 / Internal | 設計、實作與維運服務的團隊。 |
| 對外 / External | 公司其他部門的服務使用者，不指公開網際網路。 |
| Requester | 提出需求並做文件最終審閱與決策的使用者，不自動代表服務申請審核者。 |
| PRD | Product Requirements Document；定義為何做、為誰做及產品範圍。 |
| Feature Spec | 定義功能的具體行為、規則與驗收條件。 |
| RFC | Request for Comments；記錄設計方案、取捨與決策。 |
| Service Spec | 對使用者說明服務能力、限制及已核准承諾。 |
| TBD | To Be Determined；尚待釐清或決定。 |

## 服務用語

| 術語 | 本 repository 的用法 |
| --- | --- |
| OLAP | Online Analytical Processing；本服務以 Apache Doris 為基礎。 |
| Data Ingestion Pipeline | 產品中的資料匯入部分；詳細文件目前留白。 |
| FE / BE | Apache Doris Frontend / Backend 元件名稱；本表不定義部署數量或拓樸。 |
| Monitoring | 使用者或團隊用來觀察服務／工作負載狀態的能力；具體功能待定。 |
| Logs | 用於調查與問題排查的紀錄；可見資訊與遮蔽規則待定。 |
| Metrics | 可供量測與整合的指標資料；對使用者開放仍是未來可能方向。 |
| Alerting | 告警行為；未來使用者自行串接 metrics 不等於服務提供代管告警。 |

## 待釐清事項

- 正式產品名稱、使用者角色名稱與資源範圍用語，待 PRD／Feature Spec 決定後加入。
- 來源為目前的使用者討論及文件組織約定；不是特定版本 Doris 行為的證據。
