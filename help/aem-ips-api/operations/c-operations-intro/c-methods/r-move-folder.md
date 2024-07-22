---
description: フォルダーを新しい場所に移動します。
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 23%

---

# moveFolder{#movefolder}

フォルダーを新しい場所に移動します。

構文

## 許可されているユーザータイプ {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-473c2e68bcc14a9ea2593bee26e679dd}

**入力（moveFolderParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社に渡す。 |
| folderHandle | `xsd:string` | はい | フォルダーハンドル。 |
| destFolderHandle | `xsd:string` | はい | 宛先フォルダーへのハンドル。 |

**出力（moveFolderReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| folderHandle | `xsd:string` | はい | 移動したフォルダーへのハンドル。 |

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
