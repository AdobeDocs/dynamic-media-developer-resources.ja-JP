---
description: ユーザーが認証できない場合に発生します。
solution: Experience Manager
title: authenticationFault
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 21%

---


# authenticationFault{#authenticationfault}

ユーザーが認証できない場合に発生します。

構文

## 障害の種類{#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | 障害 |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## 障害フィールド{#section-1fe84846a7154b03ab49552810ee9ac3}

| 名前 | 種類 | 説明 |
|---|---|---|
| `code` | `xsd:int` | 障害ID |
| `reason` | `xsd:string` | エラーを説明する情報メッセージです。 |
