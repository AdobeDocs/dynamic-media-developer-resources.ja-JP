---
description: ユーザーが認証できないときにスローされます。
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fce5c227-9291-4d17-801f-4ef4b8d43eb4
TQID: 'https://experienceleague.adobe.com/GfcblqhZ2ToX6I6MBbnO4QUmeMBG0dz1v-uvp7Rv8a8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 37
ht-degree: 21%

---

# authenticationFault{#authenticationfault}

ユーザーが認証できないときにスローされます。

構文

## 障害タイプ {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | 障害 |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## フォールトフィールド {#section-1fe84846a7154b03ab49552810ee9ac3}

| 名前 | 種類 | 説明 |
|---|---|---|
| `code` | `xsd:int` | 障害ID |
| `reason` | `xsd:string` | 障害を説明する有益なメッセージ。 |

