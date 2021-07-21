---
description: フォルダーの名前を変更します。
solution: Experience Manager
title: renameFolder
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: 2d4f1059-8018-4efb-a1ec-8eb560b1a58f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 20%

---

# renameFolder{#renamefolder}

フォルダーの名前を変更します。

構文

## 許可されたユーザーの種類 {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、アセットに対する読み取りおよび書き込みアクセス権を持っている必要があります。

## パラメータ {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**入力(renameFolderParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 名前を変更するフォルダを持つ会社に対して処理します。 |
| `*`folderHandle`*` | `xsd:string` | はい | フォルダーを処理します。 |
| `*`folderName`*` | `xsd:string` | はい | 新しいフォルダー名。 |

**出力(renameFolderReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | はい | 名前を変更したフォルダーを処理します。 |

## 例 {#section-98bdd2f88d164f488676e90aba1dc864}

このコードサンプルは、フォルダーの名前を変更します。

**リクエスト**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**応答**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```
