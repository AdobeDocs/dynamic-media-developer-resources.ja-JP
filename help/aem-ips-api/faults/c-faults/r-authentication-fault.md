---
description: ユーザーが認証できない場合に発生します。
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: fce5c227-9291-4d17-801f-4ef4b8d43eb4
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 19%

---

# authenticationFault{#authenticationfault}

ユーザーが認証できない場合に発生します。

構文

## 障害タイプ {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | 障害 |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## フォルトフィールド {#section-1fe84846a7154b03ab49552810ee9ac3}

| 名前 | 種類 | 説明 |
|---|---|---|
| `code` | `xsd:int` | 障害ID |
| `reason` | `xsd:string` | 障害を説明する情報メッセージ。 |
