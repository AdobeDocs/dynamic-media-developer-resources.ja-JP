---
description: 権限アセットを使用して、単一のアセットの権限を設定します。
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 7%

---

# setAssetPermissions{#setassetpermissions}

権限アセットを使用して、単一のアセットの権限を設定します。

Assetsは、デフォルトで親フォルダーの権限を継承します。 アセットに権限を設定すると、`removeAssetPermissions` を呼び出さない限り、その親の権限は継承されなくなります。

## 許可されているユーザータイプ {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-e05abbce6453450fb38747101cb5e228}

**入力（setAssetPermissonsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 使用するフォルダーが含まれている会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | フォルダーハンドル。 |
| permissionArray | `types:PermissionsUpdateArray` | はい | 権限配列。 |

**出力（setAssetPermissonsReturn）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-38955bc330bb4909b6b06027ef2b143e}

このコードサンプルでは、アセットに権限を設定します。 会社とアセットハンドル、権限の配列が含まれています。

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
