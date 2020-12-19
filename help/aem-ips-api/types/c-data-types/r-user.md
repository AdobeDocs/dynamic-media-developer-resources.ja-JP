---
description: システム内のリソースとタイプのユーザー。
seo-description: システム内のリソースとタイプのユーザー。
seo-title: ユーザ
solution: Experience Manager
title: ユーザ
topic: Scene7 Image Production System API
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 10%

---


# ユーザ{#user}

システム内のリソースとタイプのユーザー。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`userHandle`*` | `xsd:string` | ユーザーハンドル。 |
| ` *`firstName`*` | `xsd:string` | ユーザーの名。 |
| ` *`lastName`*` | `xsd:string` | ユーザーの姓。 |
| ` *`電子メール`*` | `xsd:string` | 電子メールアドレス。 |
| ` *`defaultRole`*` | `xsd:string` | 所属する各会社のユーザーの役割を設定します。 ただし、ユーザーロール`IpsAmin`は、他のユーザーロールよりも優先されます。 |
| ` *`isValid`*` | `xsd:boolean` | ユーザーが有効かどうかを判定します。 |
| ` *`passwordExpires`*` | `xsd:dateTime` | パスワードの有効期限を設定します。 |

