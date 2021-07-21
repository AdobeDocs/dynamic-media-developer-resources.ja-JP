---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 48be47f6-4c1c-4f19-afa7-f643e504c287
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '30'
ht-degree: 30%

---

# ipsApiFault{#ipsapifault}

構文

## 障害タイプ {#section-425697675cac4b2ab5c48bd463956401}

| ID | 障害 |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## フォルトフィールド {#section-37fe1aef1d5f4ca480071ca933aba826}

| 名前 | 種類 | 説明 |
|---|---|---|
| `code` | `xsd:int` | 障害ID |
| `reason` | `xsd:string` | 障害を説明する情報メッセージ。 |
