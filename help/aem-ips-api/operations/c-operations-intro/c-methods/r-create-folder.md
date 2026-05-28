---
title: createFolder
description: フォルダを作成します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
TQID: 'https://experienceleague.adobe.com/iQNFDdsbxhklGSfUb1pmcNhzIT8kJYc19xFglU7Blc8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 16%

---

# [!DNL createFolder]{#createfolder}

フォルダを作成します。

>[!NOTE]
>
>会社のルートを示すために`/`を指定した場合でも、新しいフォルダーはImages フォルダーの下位にあります。

構文

## 承認済みユーザータイプ {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、親フォルダーへの読み取り/書き込みアクセス権を持っている必要があります。

## パラメーター {#section-c00d8d89cf114886a535056f2a1bf892}

**入力（createFolder）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドル |
| folderPath | `xsd:string` | はい | フォルダーとすべてのサブフォルダーをリーフレベルに取得するために使用されるルートフォルダー。 除外した場合は、会社ルートが使用されます。 |

**出力（createFolderParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| folderHandle | `xsd:string` | はい | 新しいフォルダーのハンドル。 |

## 例 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

このサンプルコードは、会社のルートにフォルダーを作成します。 応答は、新しく作成したフォルダーのハンドルを返します。

**リクエスト**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**応答**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```
