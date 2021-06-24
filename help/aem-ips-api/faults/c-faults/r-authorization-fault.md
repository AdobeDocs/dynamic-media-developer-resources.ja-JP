---
description: 認証済みユーザーがタスクを実行する権限が不十分な場合に発生します。
solution: Experience Manager
title: authorizationFault
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: 76965735-92d8-46be-b589-67cad3b987dc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 25%

---

# authorizationFault{#authorizationfault}

認証済みユーザーがタスクを実行する権限が不十分な場合に発生します。

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

## フォルトフィールド {#section-4e3e41f41fea402a9ae314bfd05f663e}

| 名前 | 種類 | 説明 |
|---|---|---|
| `code` | `xsd:int` | 障害ID |
| `reason` | `xsd:string` | 障害を説明する情報メッセージ。 |
