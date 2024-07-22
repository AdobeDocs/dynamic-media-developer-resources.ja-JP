---
description: 画像マップを削除します。
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

---

# deleteImageMap{#deleteimagemap}

画像マップを削除します。

構文

## 許可されているユーザータイプ {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーには、アセットへの読み取りおよび書き込みアクセス権が必要です。

## パラメーター {#section-28de12bab79045a5977c68855e37ae3d}

**入力（deleteImageMapParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 削除する画像マップを含む会社へのハンドル。 |
| imageMapHandle | `xsd:string` | はい | 削除する画像マップへのハンドル。 |

**出力（deleteImageMapParam）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

このコードサンプルでは、会社から画像マップを削除します。 別の操作から画像マップハンドルを取得する必要があります。

**リクエスト**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**応答**

なし
