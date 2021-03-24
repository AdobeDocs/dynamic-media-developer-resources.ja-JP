---
description: システム内のリソースとタイプのユーザー。
solution: Experience Manager
title: ユーザ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
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
| `*`defaultRole`*` | `xsd:string` | 所属する各会社のユーザーの役割を設定します。 ただし、ユーザーロール`IpsAmin`は、他のユーザーロールよりも優先されます。 |
| `*`isValid`*` | `xsd:boolean` | ユーザーが有効かどうかを判定します。 |
| `*`passwordExpires`*` | `xsd:dateTime` | パスワードの有効期限を設定します。 |

