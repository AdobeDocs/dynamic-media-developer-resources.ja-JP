---
description: フォルダの権限を設定します。
seo-description: フォルダの権限を設定します。
seo-title: setFolderPermissions
solution: Experience Manager
title: setFolderPermissions
topic: Scene7 Image Production System API
uuid: 3a33034e-df2c-48ab-8ade-b76bea444388
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setFolderPermissions{#setfolderpermissions}

フォルダの権限を設定します。

構文

## 認証されたユーザータイプ {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-2a41135054954396b40f1228f2e63b42}

**入力(setFolderPermissionsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社の担当。 |
| ` *`folderHandle`*` | `xsd:string` | はい | フォルダハンドル |
| ` *`setChildren`*` | `xsd:boolean` | はい | フォルダーに属する子の権限を設定します。 |
| ` *`permissionArray`*` | `types:PermissionUpdateArray` | はい | 権限配列。 |

**出力(setFolderPermissionsReturn)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-01730da4be874553ab44e3241cdf6357}

このコード例では、会社のハンドル、フォルダハンドル、および権限配列を指定し、フォルダに関する詳細情報を指定します。 親フォルダーの子に同じ権限を適用します。

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
