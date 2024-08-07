---
description: システム内のリソースおよびタイプのユーザー。
solution: Experience Manager
title: ユーザ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 8%

---

# [!DNL User]{#user}

システム内のリソースおよびタイプのユーザー。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| userHandle | `xsd:string` | ユーザーハンドル。 |
| firstName | `xsd:string` | ユーザーの名。 |
| lastName | `xsd:string` | ユーザーの姓。 |
| 電子メール | `xsd:string` | メールアドレス。 |
| defaultRole | `xsd:string` | ユーザーが属する各会社のユーザーの役割を設定します。 ただし、ユーザーの役割 `IpsAmin` は他のユーザーの役割よりも優先されます。 |
| isValid | `xsd:boolean` | ユーザーが有効かどうかを判断します。 |
| passwordExpires | `xsd:dateTime` | パスワードの有効期限を設定します。 |
