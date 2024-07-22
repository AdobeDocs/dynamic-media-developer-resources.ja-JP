---
description: フォルダーの名前を変更します。
solution: Experience Manager
title: renameFolder
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 2d4f1059-8018-4efb-a1ec-8eb560b1a58f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 18%

---

# renameFolder{#renamefolder}

フォルダーの名前を変更します。

構文

## 許可されているユーザータイプ {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーには、アセットへの読み取りおよび書き込みアクセス権が必要です。

## パラメーター {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**入力（renameFolderParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 名前を変更するフォルダーがある会社にハンドルします。 |
| folderHandle | `xsd:string` | はい | フォルダーへのハンドル。 |
| folderName | `xsd:string` | はい | 新しいフォルダー名。 |

**出力（renameFolderReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| folderHandle | `xsd:string` | はい | 名前を変更したフォルダーへのハンドル。 |

## 例 {#section-98bdd2f88d164f488676e90aba1dc864}

このコードのサンプルでは、フォルダーの名前を変更します。

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
