---
description: 認証済みユーザーがタスクを実行するのに十分な権限を持っていない場合にスローされます。
solution: Experience Manager
title: authorizationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 76965735-92d8-46be-b589-67cad3b987dc
TQID: 'https://experienceleague.adobe.com/oDM8k3LLSl2AD8i2vtLirkHl9J5pz8PxzgMjKLCl7do'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 54
ht-degree: 27%

---

# authorizationFault{#authorizationfault}

認証済みユーザーがタスクを実行するのに十分な権限を持っていない場合にスローされます。

構文

## 障害タイプ {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | 障害 |
|---|---|
| 20000 | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY` |
| 20001 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME` |
| 20002 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER` |
| 20003 | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION` |
| 20004 | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION` |
| 20005 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE` |
| 20006 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY` |
| 20007 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER` |
| 20008 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP` |
| 20009 | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION` |

## フォールトフィールド {#section-4e3e41f41fea402a9ae314bfd05f663e}

| 名前 | 種類 | 説明 |
|---|---|---|
| `code` | `xsd:int` | 障害ID |
| `reason` | `xsd:string` | 障害を説明する有益なメッセージ。 |

