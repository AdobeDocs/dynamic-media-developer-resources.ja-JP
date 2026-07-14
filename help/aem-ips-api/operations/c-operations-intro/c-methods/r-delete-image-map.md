---
description: 画像マップを削除します。
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
TQID: 'https://experienceleague.adobe.com/6r-EiZLM0tRUpzoTJyTt3rAkyABfNH9DQvDJq-XsqPY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 9%

---

# deleteImageMap{#deleteimagemap}

画像マップを削除します。

構文

## 承認済みユーザータイプ {#section-41fd188af16a40d4b07923165bcf15d8}

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

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

このコードサンプルは、企業から画像マップを削除します。 別の操作から画像マップハンドルを取得する必要があります。

**リクエスト**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**応答**

なし

