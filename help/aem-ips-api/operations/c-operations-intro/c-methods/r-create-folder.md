---
title: createFolder
description: フォルダを作成します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 16%

---

# [!DNL createFolder]{#createfolder}

フォルダを作成します。

>[!NOTE]
>
>会社のルートを示す `/` を指定した場合でも、新しいフォルダーは Images フォルダーの下位になります。

構文

## 許可されているユーザータイプ {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーには、親フォルダーに対する読み取り/書き込みアクセス権が必要です。

## パラメーター {#section-c00d8d89cf114886a535056f2a1bf892}

**入力（createFolder）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社へのハンドル |
| folderPath | `xsd:string` | はい | フォルダーとリーフレベルまでのすべてのサブフォルダーを取得するために使用されるルートフォルダー。 除外する場合は、会社ルートが使用されます。 |

**出力（createFolderParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| folderHandle | `xsd:string` | はい | 新しいフォルダーのハンドル。 |

## 例 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

このサンプルコードでは、会社のルートにフォルダーを作成します。 応答は、新しく作成されたフォルダーのハンドルを返します。

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
