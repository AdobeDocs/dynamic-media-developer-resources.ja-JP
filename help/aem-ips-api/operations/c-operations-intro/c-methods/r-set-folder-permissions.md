---
description: フォルダーの権限を設定します。
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
TQID: 'https://experienceleague.adobe.com/r-WGRjE263vPSVKsBieklQ79SASbDQOx9hp5IzS0-O0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 12%

---

# setFolderPermissions{#setfolderpermissions}

フォルダーの権限を設定します。

構文

## 承認済みユーザータイプ {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-2a41135054954396b40f1228f2e63b42}

**入力（setFolderPermissionsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドル。 |
| folderHandle | `xsd:string` | はい | フォルダーハンドル。 |
| setChildren | `xsd:boolean` | はい | フォルダーに属する子に対する権限を設定します。 |
| permissionArray | `types:PermissionUpdateArray` | はい | 権限の配列： |

**Output （setFolderPermissionsReturn）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-01730da4be874553ab44e3241cdf6357}

このコードのサンプルでは、会社のハンドル、フォルダーハンドル、およびフォルダーに関する詳細情報を含む権限配列を指定します。 親フォルダーの子にも同じ権限が適用されます。

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

