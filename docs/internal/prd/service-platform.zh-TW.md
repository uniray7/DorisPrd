---
doc_id: PRD-PLATFORM
document_type: PRD
audience: Internal
status: Draft
revision: 0.1
reviewer: Requester
applies_to: OLAP Service / Data Ingestion Pipeline; version TBD
language: zh-TW
---

# 整體服務 PRD

[English](service-platform.en.md) · [內部文件](../README.zh-TW.md)

> 輕量骨架。`service-platform` 不是正式產品名稱；以下背景不等於完整規格或上線承諾。

## 背景與問題

已確認產品方向：公司內部提供以 Apache Doris 為基礎的 OLAP Service 與 Data Ingestion Pipeline，供其他部門使用。具體待解決問題與現有痛點待補。

## 使用者與核心情境

已知讀者／使用者群體為其他部門的服務使用者及團隊內部人員。角色、核心工作流程與優先情境待釐清。

## 目標、範圍與非目標

- 產品範圍包含 OLAP、Data Ingestion，以及內外部 monitoring／logs。
- 外部 monitoring／logs 主要用於調查與問題排查，部分資訊須遮蔽或不提供；詳細政策待定。
- Pipeline 既有設計已核准，實作接近完成，可作為文件現況基準；本 repository 不包含其機密原始文件，詳細需求暫留白。
- 產品非目標、首版範圍與成功條件待決定。維運文件不在本 repository 範圍內，不代表產品不需要維運。

## 需求與優先順序

待補：以穩定 requirement ID 記錄需求、理由、優先順序、狀態及對應 Feature Spec。尚未建立具體功能承諾。

## 已知設計約束

- Doris 候選版本為 4.1.0 或 4.1.4，尚未選定；發布狀態與相容性未驗證。
- 部署設計為自建 bare-metal Nomad cluster，搭配 Consul 與 Vault；FE／BE 以 Docker containers 執行於 Nomad agent 上的 Docker daemon。
- 詳細拓樸、資源配置及整合方式留在[部署拓樸](../architecture/deployment-topology.zh-TW.md)決定。

## 成功條件與驗收

待補：產品成功指標、量測方式、首版驗收範圍；不自行填入 SLA／SLO 或效能數值。

## 未來方向

可能對使用者開放 metrics，讓其串接自己的 alert。尚未承諾功能、介面或時程，也不代表服務代管 alerting。

## 待釐清事項

- 優先服務哪些部門／角色？目前最需要解決的問題是什麼？影響首版情境與優先順序。
- OLAP、Ingestion、monitoring／logs 是否一起申請，或分別取得使用權？影響產品與申請邊界。
- 首版提供哪些能力，哪些明確不提供？影響 Feature Spec 與對外承諾。
- 如何判定首版成功及可開放？影響驗收與 Service Spec。

## 來源與相關文件

來源：使用者在本次產品背景與文件架構討論中的確認，非外部技術驗證。Pipeline 文件未經檢閱。

- [內部文件索引](../README.zh-TW.md)
- [文件組織決策](../../../README.zh-TW.md)
