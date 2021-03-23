---
description: 会社のメタデータフィールドを削除します。
seo-description: 会社のメタデータフィールドを削除します。
seo-title: deleteMetadataField
solution: Experience Manager
title: deleteMetadataField
uuid: 06ec434a-2793-4227-ac93-ae3871c38ab9
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 9%

---


# deleteMetadataField{#deletemetadatafield}

会社のメタデータフィールドを削除します。

構文

## 認証済みユーザータイプ{#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-73f12a30cc4340b6b32dd11effd5195e}

**入力(deleteMetadataFieldParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 削除するメタデータフィールドを含む会社へのハンドル。 |
| `*`fieldHandle`*` | `xsd:string` | はい | 削除するメタデータフィールドへのハンドル。 |

**出力(deleteMetadataFieldParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

このコードサンプルは、会社のメタデータフィールドを削除します。 この操作は、IPS Webサービスサーバに渡される`deleteMetadataFieldParam`内のフィールドとして、会社ハンドルとメタデータハンドルを使用して、この操作を実行します。

**リクエスト**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**応答**

なし。0
