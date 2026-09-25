---
doc_id: INT-INDEX
document_type: Index
audience: Internal
status: Draft
revision: 0.1
reviewer: Requester
applies_to: OLAP Service / Data Ingestion Pipeline; version TBD
language: zh-TW
---

# 團隊文件入口

[English](README.en.md) · [Repository 首頁](../../README.zh-TW.md)

本目錄記錄需求、功能規則、架構與設計決策，目前為輕量骨架。採一份整體 PRD，不包含維運 Runbook。

## 需求與規格

- [整體 PRD](prd/service-platform.zh-TW.md)：產品目標、使用者與服務邊界。
- [申請與審核](feature-specs/service-application-and-approval.zh-TW.md)。
- [Access Control](feature-specs/access-control.zh-TW.md)。
- [OLAP Service](feature-specs/olap-service.zh-TW.md)。
- [Monitoring](feature-specs/monitoring.zh-TW.md)。
- [Logging 與資訊揭露](feature-specs/logging-and-information-exposure.zh-TW.md)。

## 決策、架構與資料流

- [RFC 索引](rfcs/README.zh-TW.md)。
- [系統總覽](architecture/system-overview.zh-TW.md)、[部署拓樸](architecture/deployment-topology.zh-TW.md)、[Observability Architecture](architecture/observability.zh-TW.md)。
- [OLAP Query Flow](data-flows/olap-query.zh-TW.md)、[Telemetry Flow](data-flows/telemetry.zh-TW.md)。

## Pipeline 邊界

`feature-specs/data-ingestion/` 與 `data-flows/data-ingestion/` 暫留空白。既有機密設計不匯入；有相依需求時，只向使用者詢問必要且可記錄的資訊。

## 待釐清事項與閱讀順序

先處理 PRD 的產品問題，再依相依關係補齊 Feature Spec、RFC、架構與資料流。各文件內的待釐清事項為後續討論入口，對外文件須待規格及開放狀態確認後補齊。
