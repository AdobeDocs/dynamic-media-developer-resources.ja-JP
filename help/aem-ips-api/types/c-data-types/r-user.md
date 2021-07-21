---
description: システム内のリソースとタイプのユーザー。
solution: Experience Manager
title: ユーザ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 10%

---

# ユーザ{#user}

システム内のリソースとタイプのユーザー。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | ユーザーハンドル。 |
| `*`firstName`*` | `xsd:string` | ユーザーの名。 |
| `*`lastName`*` | `xsd:string` | ユーザーの姓。 |
| `*`電子メール`*` | `xsd:string` | 電子メールアドレス。 |
| `*`defaultRole`*` | `xsd:string` | 所属する各会社のユーザーの役割を設定します。 ただし、ユーザーの役割`IpsAmin`は他のユーザーの役割より優先されます。 |
| `*`isValid`*` | `xsd:boolean` | ユーザーが有効かどうかを判断します。 |
| `*`passwordExpires`*` | `xsd:dateTime` | パスワードの有効期限を設定します。 |
