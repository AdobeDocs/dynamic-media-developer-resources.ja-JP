---
description: 会社のメタデータフィールドを削除します。
seo-description: 会社のメタデータフィールドを削除します。
seo-title: deleteMetadataField
solution: Experience Manager
title: deleteMetadataField
topic: Scene7 Image Production System API
uuid: 06ec434a-2793-4227-ac93-ae3871c38ab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteMetadataField{#deletemetadatafield}

会社のメタデータフィールドを削除します。

構文

## 認証されたユーザータイプ {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-73f12a30cc4340b6b32dd11effd5195e}

**入力(deleteMetadataFieldParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 削除するメタデータフィールドを含む会社のハンドル。 |
| ` *`fieldHandle`*` | `xsd:string` | はい | 削除するメタデータフィールドのハンドル。 |

**出力(deleteMetadataFieldParam)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

このコードサンプルを使用すると、会社のメタデータフィールドを削除できます。 この操作は、会社のハンドルとメタデータハンドルを、IPS Webサー `deleteMetadataFieldParam` バに渡されるフィールドとして使用して実行されます。

**リクエスト**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**応答**

なし。0
