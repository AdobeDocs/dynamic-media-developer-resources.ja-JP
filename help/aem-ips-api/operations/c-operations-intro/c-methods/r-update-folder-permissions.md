---
description: フォルダーの権限を更新します。
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 4e4f382e-4339-4b9d-a721-d33a4fa8be6b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 18%

---

# updateFolderPermissions{#updatefolderpermissions}

フォルダーの権限を更新します。

構文

## 許可されたユーザーの種類 {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-339e6e17c5504e1ea79fbdc05f618050}

**入力(updateFolderPermissionsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社の担当。 |
| `*`folderHandle`*` | `xsd:string` | はい | フォルダーハンドル。 |
| `*`updateChildren`*` | `xsd:boolean` | はい | 最上位のフォルダーに設定された権限を持つ子を更新するかどうかを指定します。 |
| `*`updateArray`*` | `types:PermissionUpdateArray` | はい | フォルダーに適用する権限の更新の配列。 |

**出力(updateFolderPermissionsReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-c3fe4d4388674870a3856c35ef66b631}

**リクエスト**

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**応答**

なし
