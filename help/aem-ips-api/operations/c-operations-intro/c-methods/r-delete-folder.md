---
description: フォルダーを削除します。
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
TQID: 'https://experienceleague.adobe.com/OfZbcMyLmLvg6x088Y5y0DBM7-C--jW7oPtOfIaSwDk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 9%

---

# deleteFolder{#deletefolder}

フォルダーを削除します。

構文

## 承認済みユーザータイプ {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、フォルダーとそのすべての子に対する読み取りおよび削除アクセス権を持っている必要があります。

## パラメーター {#section-a793c98a481a4f26ab50bc69b16b57e7}

**入力（deleteFolderParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | フォルダーが属する会社へのハンドル。 |
| folderHandle | `xsd:string` | はい | 削除するフォルダーへのハンドル。 |

**出力（deleteFolderParam）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-9d4617b322e8442d80e59be0f8714841}

このサンプルコードは、会社のルートからフォルダーを削除します。 フォルダーハンドルが必要です。これは別の操作から取得する必要があります。

**リクエスト**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

なし

