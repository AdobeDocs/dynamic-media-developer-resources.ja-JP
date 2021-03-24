---
description: フォルダの名前を変更します。
solution: Experience Manager
title: renameFolder
feature: Dynamic Mediaクラシック，SDK/API，アセット管理
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 20%

---


# renameFolder{#renamefolder}

フォルダの名前を変更します。

構文

## 認証済みユーザータイプ{#section-5a252b00937d4befbec76fa23fbae9df}

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
| `*`companyHandle`*` | `xsd:string` | はい | 名前を変更する会社ーを処理します。 |
| `*`folderHandle`*` | `xsd:string` | はい | フォルダーへのハンドル。 |
| `*`folderName`*` | `xsd:string` | はい | 新しいフォルダー名。 |

**出力(renameFolderReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | はい | 名前を変更したフォルダーへのハンドル。 |

## 例 {#section-98bdd2f88d164f488676e90aba1dc864}

このコードのサンプルを使用すると、フォルダーの名前を変更できます。

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

