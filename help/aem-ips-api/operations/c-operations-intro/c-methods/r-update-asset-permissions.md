---
description: アセットの権限を更新します。
seo-description: アセットの権限を更新します。
seo-title: updateAssetPermissions
solution: Experience Manager
title: updateAssetPermissions
topic: Dynamic Media Image Production System API
uuid: feb2faf3-81de-436e-82de-1e41df03508f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 22%

---


# updateAssetPermissions{#updateassetpermissons}

アセットの権限を更新します。

構文

## 認証済みユーザータイプ{#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-392cb3076cf84790a32fd913f2b111a3}

**入力(updateAssetPermissionsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社ハンドル |
| `*`assetHandle`*` | `xsd:string` | はい | アセットハンドル |
| `*`updateArray`*` | `types:PermissionUpdateArray` | はい | アセットに適用する権限。 |

**Output (updateAssetPermissionsReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**リクエスト**

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**応答**

なし
