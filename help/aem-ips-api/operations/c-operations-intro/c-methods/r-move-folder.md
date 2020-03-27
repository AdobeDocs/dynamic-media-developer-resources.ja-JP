---
description: フォルダーを新しい場所に移動します。
seo-description: フォルダーを新しい場所に移動します。
seo-title: moveFolder
solution: Experience Manager
title: moveFolder
topic: Scene7 Image Production System API
uuid: 424858c3-5796-4ae9-b5ad-fd50ddbee702
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveFolder{#movefolder}

フォルダーを新しい場所に移動します。

構文

## 認証されたユーザータイプ {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-473c2e68bcc14a9ea2593bee26e679dd}

**入力(moveFolderParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社の取り扱い。 |
| ` *`folderHandle`*` | `xsd:string` | はい | フォルダハンドル |
| ` *`destFolderHandle`*` | `xsd:string` | はい | 宛先フォルダーへのハンドル。 |

**出力(moveFolderReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | はい | 移動したフォルダーのハンドル。 |

## 例 {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**リクエスト**

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**応答**

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```

