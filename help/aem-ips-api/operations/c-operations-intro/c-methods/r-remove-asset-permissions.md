---
description: 選択したアセットから権限を削除します。
seo-description: 選択したアセットから権限を削除します。
seo-title: removeAssetPermissions
solution: Experience Manager
title: removeAssetPermissions
topic: Scene7 Image Production System API
uuid: 5a351862-f412-4d89-90b7-9e70a26eacbc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 16%

---


# removeAssetPermissions{#removeassetpermissions}

選択したアセットから権限を削除します。

構文

## 認証済みユーザータイプ{#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**入力(removeAssetPermissionsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| ` *`assetHandle`*` | `xsd:string` | はい | 権限を削除するアセットのハンドル。 |

**出力(removeAssetPermissionsReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-238fa7bb091548f5ba72ced11fc92d4f}

このコードのサンプルを使用することで、アセットから権限を削除することができます。

**リクエスト**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**応答**

なし
