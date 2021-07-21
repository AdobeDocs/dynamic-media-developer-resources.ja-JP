---
description: 画像マップを削除します。
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 12%

---

# deleteImageMap{#deleteimagemap}

画像マップを削除します。

構文

## 許可されたユーザーの種類 {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、アセットに対する読み取りおよび書き込みアクセス権を持っている必要があります。

## パラメータ {#section-28de12bab79045a5977c68855e37ae3d}

**入力(deleteImageMapParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 削除する画像マップを含む会社へのハンドル。 |
| `*`imageMapHandle`*` | `xsd:string` | はい | 削除する画像マップのハンドル。 |

**出力(deleteImageMapParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

このコードサンプルは、会社から画像マップを削除します。 別の操作から画像マップハンドルを取得する必要があります。

**リクエスト**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**応答**

なし
