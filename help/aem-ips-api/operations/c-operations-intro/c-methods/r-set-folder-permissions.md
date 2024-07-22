---
description: フォルダー権限を設定します。
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 12%

---

# setFolderPermissions{#setfolderpermissions}

フォルダー権限を設定します。

構文

## 許可されているユーザータイプ {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-2a41135054954396b40f1228f2e63b42}

**入力（setFolderPermissionsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社ハンドル。 |
| folderHandle | `xsd:string` | はい | フォルダーハンドル。 |
| setChildren | `xsd:boolean` | はい | フォルダーに属する子に権限を設定します。 |
| permissionArray | `types:PermissionUpdateArray` | はい | 権限配列。 |

**出力（setFolderPermissionsReturn）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-01730da4be874553ab44e3241cdf6357}

このコードサンプルでは、フォルダーの詳細情報を使用して、会社ハンドル、フォルダーハンドル、権限配列を指定しています。 親フォルダーの子に同じ権限を適用します。

**リクエスト**

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**応答**

なし
