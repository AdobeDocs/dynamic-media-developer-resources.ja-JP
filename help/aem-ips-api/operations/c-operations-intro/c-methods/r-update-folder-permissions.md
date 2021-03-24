---
description: フォルダーの権限を更新します。
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 17%

---


# updateFolderPermissions{#updatefolderpermissions}

フォルダーの権限を更新します。

構文

## 認証済みユーザータイプ{#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-339e6e17c5504e1ea79fbdc05f618050}

**入力(updateFolderPermissionsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社ハンドル |
| `*`folderHandle`*` | `xsd:string` | はい | フォルダーハンドル |
| `*`updateChildren`*` | `xsd:boolean` | はい | 最上位フォルダーの権限セットを持つ子を更新するかどうかを指定します。 |
| `*`updateArray`*` | `types:PermissionUpdateArray` | はい | フォルダーに適用する権限の更新の配列です。 |

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
