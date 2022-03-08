---
description: アセットの権限を更新します。
solution: Experience Manager
title: updateAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 12972a52-7b70-405c-9c73-e5ce6ab7dd9b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 24%

---

# updateAssetPermissions{#updateassetpermissons}

アセットの権限を更新します。

構文

## 認証済みユーザータイプ {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-392cb3076cf84790a32fd913f2b111a3}

**入力 (updateAssetPermissionsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社の取り扱い。 |
| assetHandle | `xsd:string` | はい | アセットハンドル。 |
| updateArray | `types:PermissionUpdateArray` | はい | アセットに適用する権限です。 |

**出力 (updateAssetPermissionsReturn)**

IPS API はこの操作に対する応答を返しません。

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
