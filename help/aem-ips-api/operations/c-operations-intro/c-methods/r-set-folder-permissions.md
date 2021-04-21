---
description: フォルダの権限を設定します。
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 14%

---


# setFolderPermissions{#setfolderpermissions}

フォルダの権限を設定します。

構文

## 認証済みユーザータイプ{#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-2a41135054954396b40f1228f2e63b42}

**入力(setFolderPermissionsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社ハンドル |
| `*`folderHandle`*` | `xsd:string` | はい | フォルダーハンドル |
| `*`setChildren`*` | `xsd:boolean` | はい | フォルダーに属する子に権限を設定します。 |
| `*`permissionArray`*` | `types:PermissionUpdateArray` | はい | 権限配列。 |

**出力(setFolderPermissionsReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-01730da4be874553ab44e3241cdf6357}

このコードの例では、会社ハンドル、フォルダハンドル、権限配列を指定し、そのフォルダに関する詳細情報を示します。 親フォルダーの子に同じ権限を適用します。

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
