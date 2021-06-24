---
description: フォルダーを新しい場所に移動します。
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 26%

---

# moveFolder{#movefolder}

フォルダーを新しい場所に移動します。

構文

## 許可されたユーザーの種類 {#section-7f1979fb5e504bdea3a8df01101b50c3}

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
| `*`companyHandle`*` | `xsd:string` | はい | 会社に取り扱う。 |
| `*`folderHandle`*` | `xsd:string` | はい | フォルダーハンドル。 |
| `*`destFolderHandle`*` | `xsd:string` | はい | 宛先フォルダーを処理します。 |

**出力(moveFolderReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | はい | 移動したフォルダーを処理します。 |

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
