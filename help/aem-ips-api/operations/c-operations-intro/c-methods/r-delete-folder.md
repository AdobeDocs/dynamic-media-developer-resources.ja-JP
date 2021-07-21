---
description: フォルダーを削除します。
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 10%

---

# deleteFolder{#deletefolder}

フォルダーを削除します。

構文

## 許可されたユーザーの種類 {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、フォルダーとそのすべての子に対する読み取りおよび削除アクセス権を持っている必要があります。

## パラメータ {#section-a793c98a481a4f26ab50bc69b16b57e7}

**入力(deleteFolderParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | フォルダーが属する会社へのハンドル。 |
| `*`folderHandle`*` | `xsd:string` | はい | 削除するフォルダーのハンドル。 |

**出力(deleteFolderParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-9d4617b322e8442d80e59be0f8714841}

このサンプルコードでは、会社のルートからフォルダーを削除します。 別の操作から取得する必要があるフォルダーハンドルが必要です。

**リクエスト**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

なし
