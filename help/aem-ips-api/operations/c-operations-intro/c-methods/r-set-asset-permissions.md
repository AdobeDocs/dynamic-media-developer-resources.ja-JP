---
description: 権限アセットを使用して、単一アセットの権限を設定します。
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
TQID: 'https://experienceleague.adobe.com/dd96ai2DgoCqZ1NR-2rixSHDEaBSgk6ioQIqmG-1RoE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 7%

---

# setAssetPermissions{#setassetpermissions}

権限アセットを使用して、単一アセットの権限を設定します。

Assetsは、デフォルトで親フォルダーの権限を継承します。 アセットに対して権限を設定すると、`removeAssetPermissions`を呼び出さない限り、親の権限は継承されなくなります。

## 承認済みユーザータイプ {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-e05abbce6453450fb38747101cb5e228}

**入力（setAssetPermissonsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 一緒に作業するフォルダーを含む会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | フォルダーハンドル。 |
| permissionArray | `types:PermissionsUpdateArray` | はい | 権限の配列： |

**出力（setAssetPermissonsReturn）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-38955bc330bb4909b6b06027ef2b143e}

このコードのサンプルでは、アセットに対する権限を設定します。 会社とアセットのハンドル、および権限配列が含まれます。

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

