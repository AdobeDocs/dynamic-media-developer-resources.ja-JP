---
description: アセットの権限を更新します。
solution: Experience Manager
title: updateAssetPermissions
feature: Dynamic Mediaクラシック，SDK/API，アセット管理
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 20%

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
