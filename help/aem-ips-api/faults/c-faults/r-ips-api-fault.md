---
description: 'null'
seo-description: 'null'
seo-title: ipsApiFault
solution: Experience Manager
title: ipsApiFault
topic: Scene7 Image Production System API
uuid: 010814a8-1d29-4b02-8449-cb26e4335e07
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '27'
ht-degree: 33%

---


# ipsApiFault{#ipsapifault}

構文

## 障害の種類{#section-425697675cac4b2ab5c48bd463956401}

| ID | 障害 |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## 障害フィールド{#section-37fe1aef1d5f4ca480071ca933aba826}

| 名前 | 種類 | 説明 |
|---|---|---|
| `code` | `xsd:int` | 障害ID |
| `reason` | `xsd:string` | エラーを説明する情報メッセージです。 |

