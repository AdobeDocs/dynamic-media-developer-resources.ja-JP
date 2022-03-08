---
description: 選択したアセットから権限を削除します。
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c47d9853-91b1-45fe-b8ff-aaa1239ca0d1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---

# removeAssetPermissions{#removeassetpermissions}

選択したアセットから権限を削除します。

構文

## 認証済みユーザータイプ {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**入力 (removeAssetPermissionsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い。 |
| assetHandle | `xsd:string` | はい | 削除する権限を持つアセットへのハンドル。 |

**出力 (removeAssetPermissionsReturn)**

IPS API はこの操作に対する応答を返しません。

## 例 {#section-238fa7bb091548f5ba72ced11fc92d4f}

このコードサンプルを使用すると、アセットから権限を削除できます。

**リクエスト**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**応答**

なし
