---
description: 権限アセットを使用して、単一のアセットの権限を設定します。
seo-description: 権限アセットを使用して、単一のアセットの権限を設定します。
seo-title: setAssetPermissions
solution: Experience Manager
title: setAssetPermissions
topic: Scene7 Image Production System API
uuid: 38f26482-bce9-4d2c-9714-e8c3ae40c2d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 8%

---


# setAssetPermissions{#setassetpermissions}

権限アセットを使用して、単一のアセットの権限を設定します。

アセットは、デフォルトで親フォルダーの権限を継承します。 アセットに権限を設定すると、`removeAssetPermissions`を呼び出さない限り、親の権限は継承されなくなります。

## 認証済みユーザータイプ{#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-e05abbce6453450fb38747101cb5e228}

**Input (setAssetPermissionsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 操作する会社ーを含むフォルダーへのハンドルです。 |
| ` *`assetHandle`*` | `xsd:string` | はい | フォルダーハンドル |
| ` *`permissionArray`*` | `types:PermissionsUpdateArray` | はい | 権限配列。 |

**Output (setAssetPermissionsReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-38955bc330bb4909b6b06027ef2b143e}

このコードのサンプルを使用して、アセットに権限を設定します。 会社とアセットハンドル、権限配列が含まれます。

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
