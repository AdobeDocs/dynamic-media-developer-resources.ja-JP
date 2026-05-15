---
description: アセットの権限を更新します。
solution: Experience Manager
title: updateAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 12972a52-7b70-405c-9c73-e5ce6ab7dd9b
TQID: 'https://experienceleague.adobe.com/JXEADalEOeFlcIdwQF14ug1BvUIYGimwNI8wYDgO1yU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 54
ht-degree: 18%

---

# updateAssetPermissions{#updateassetpermissons}

アセットの権限を更新します。

構文

## 承認済みユーザータイプ {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-392cb3076cf84790a32fd913f2b111a3}

**入力（updateAssetPermissionsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドル。 |
| assetHandle | `xsd:string` | はい | アセットのハンドル： |
| updateArray | `types:PermissionUpdateArray` | はい | アセットに適用する権限。 |

**出力（updateAssetPermissionsReturn）**

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
