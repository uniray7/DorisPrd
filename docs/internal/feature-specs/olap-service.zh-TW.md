---
doc_id: FEAT-OLAP
document_type: Feature Spec
audience: Internal
status: Draft
revision: 0.1
reviewer: Requester
applies_to: OLAP Service; version TBD
language: zh-TW
---

# OLAP Service Feature Spec

[English](olap-service.en.md) · [內部文件](../README.zh-TW.md)

> 輕量骨架；產品以 Apache Doris 為基礎，具體服務行為尚待決定。

## 目的、支援範圍與介面

待補：使用情境、查詢與其他允許操作、介面／用戶端、輸入輸出，以及明確不支援項目。

## 資源規則與執行行為

待補：資源範圍、配額、並行／逾時等限制是否需要及如何執行。數值須經決策與適用版本驗證。

## 例外與可見結果

待補：權限拒絕、超限、取消、失敗與重試語意，依選定能力定義，不推定支援行為。

## 驗收條件

待補：正常、邊界與失敗案例，以及能力／限制的驗證方法。

## 待釐清事項

- 首版提供哪些查詢與資料操作？影響功能邊界與介面。
- 資源分配與限制以何種範圍生效？影響隔離、驗收及 Service Spec。
- Doris 版本如何選定？影響功能與相容性驗證。
- 查詢對資料可見性／新鮮度有何需求？涉及 Pipeline 的必要部分向使用者詢問，不推定端到端保證。

## 相依與來源

- [整體 PRD](../prd/service-platform.zh-TW.md)
- [Access Control](access-control.zh-TW.md)
- [OLAP Query Flow](../data-flows/olap-query.zh-TW.md)
- 衍生文件：[OLAP Service Spec](../../external/service-specs/olap-service.zh-TW.md)。

已知產品方向來自使用者確認；技術能力與版本依據待查證。
