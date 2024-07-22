---
description: フォルダーを削除します。
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 9%

---

# deleteFolder{#deletefolder}

フォルダーを削除します。

構文

## 許可されているユーザータイプ {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーには、フォルダーとそのすべての子に対する読み取りおよび削除アクセス権が必要です。

## パラメーター {#section-a793c98a481a4f26ab50bc69b16b57e7}

**入力（deleteFolderParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | フォルダーが属する会社へのハンドル。 |
| folderHandle | `xsd:string` | はい | 削除するフォルダーへのハンドル。 |

**出力（deleteFolderParam）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-9d4617b322e8442d80e59be0f8714841}

このサンプルコードでは会社のルートからフォルダーを削除します。 別の操作から取得する必要があるフォルダーハンドルが必要です。

**リクエスト**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

なし
