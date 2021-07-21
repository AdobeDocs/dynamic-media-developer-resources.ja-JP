---
description: 権限アセットを使用して、単一のアセットの権限を設定します。
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 9%

---

# setAssetPermissions{#setassetpermissions}

権限アセットを使用して、単一のアセットの権限を設定します。

アセットは、デフォルトで親フォルダーの権限を継承します。 アセットに対する権限を設定すると、`removeAssetPermissions`を呼び出さない限り、親の権限は継承されなくなります。

## 許可されたユーザーの種類 {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-e05abbce6453450fb38747101cb5e228}

**入力(setAssetPermissionsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 操作するフォルダーを含む会社のハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | フォルダーハンドル。 |
| `*`permissionArray`*` | `types:PermissionsUpdateArray` | はい | 権限配列。 |

**出力(setAssetPermissionsReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-38955bc330bb4909b6b06027ef2b143e}

このコードサンプルは、アセットに権限を設定します。 会社とアセットハンドル、権限配列が含まれます。

**リクエスト**

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**応答**

なし
