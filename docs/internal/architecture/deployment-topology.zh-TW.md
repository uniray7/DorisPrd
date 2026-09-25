---
doc_id: ARCH-DEPLOYMENT
document_type: System Architecture
audience: Internal
status: Draft
revision: 0.1
reviewer: Requester
applies_to: Apache Doris / Nomad / Consul / Vault; versions TBD
language: zh-TW
---

# 部署拓樸

[English](deployment-topology.en.md) · [內部文件](../README.zh-TW.md)

> 輕量骨架，記錄部署設計而非操作程序；不代表已驗證環境配置。

## 已確認的部署方向

來源：使用者確認。自建 bare-metal 機器承載 HashiCorp Nomad cluster，搭配 Consul 與 Vault。Doris FE、BE 以 Docker containers 形式，執行於 Nomad agent 上的 Docker daemon。

Doris 候選版本為 4.1.0 或 4.1.4，未選定且未驗證發布／相容性；其他元件版本未提供。

## 節點配置與排程

待補：角色、節點數、資源配置、故障域、placement 與共置規則；不推定 HA 拓樸。

## 網路、儲存與整合

待補：連線／發現方式、container 網路、持久化資料與儲存邊界，以及 Consul／Vault 的實際用途與整合介面。

## 相依與設計限制

待補：版本相容性、環境約束與已決定的失效影響；不包含部署、升級或復原 Runbook。

## 待釐清事項

- 如何選定 Doris 版本及驗證相容性？影響技術引用與配置。
- FE／BE 的節點數、資源與排程邊界為何？影響拓樸與故障域。
- 持久化資料與網路如何配置？影響資料／連線邊界。
- Consul、Vault 分別參與哪些流程？影響實際元件依賴。

## 相關文件與參考

- [系統總覽](system-overview.zh-TW.md)
- [參考資料規範](../../governance/reference-policy.zh-TW.md)

尚未加入外部版本證據或本地驗證紀錄。
