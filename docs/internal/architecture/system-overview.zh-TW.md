---
doc_id: ARCH-SYSTEM
document_type: System Architecture
audience: Internal
status: Draft
revision: 0.1
reviewer: Requester
applies_to: OLAP Service / Data Ingestion Pipeline; version TBD
language: zh-TW
---

# 系統架構總覽

[English](system-overview.en.md) · [內部文件](../README.zh-TW.md)

> 輕量骨架；尚未繪製完整架構圖，避免推定未決元件或資料路徑。

## 系統目的與邊界

已知方向見[整體 PRD](../prd/service-platform.zh-TW.md)。待補：使用者入口、服務責任與外部相依系統邊界。

## 元件與介面

已知基礎為 Apache Doris FE／BE，以及 Nomad、Consul、Vault 的部署設計。待補：元件責任、介面與實際整合方式；不由工具名稱推定功能。

## 架構圖與責任分工

待確認互動與部署邊界後補圖，標示內容狀態。Pipeline 內部設計留白；若需要跨服務連線，只詢問必要介面資訊。

## 失效邊界與設計決策

待補：已決定的相依失效影響、隔離及可用性設計；此處描述設計，不撰寫維運 Runbook。

## 待釐清事項

- 使用者從哪裡進入各服務，哪些元件負責存取判定？影響介面與責任圖。
- 各元件與外部相依系統的責任為何？影響故障邊界。
- 哪些可用性／隔離要求已決定？影響架構方案與 RFC。

## 相依與來源

來源：使用者確認的產品與部署背景，非實際部署驗證。

- [部署拓樸](deployment-topology.zh-TW.md)
- [Observability Architecture](observability.zh-TW.md)
- [OLAP Query Flow](../data-flows/olap-query.zh-TW.md)
