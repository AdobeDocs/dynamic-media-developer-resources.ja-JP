---
description: 会社のメタデータフィールドを削除します。
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 8%

---

# deleteMetadataField{#deletemetadatafield}

会社のメタデータフィールドを削除します。

構文

## 許可されているユーザータイプ {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-73f12a30cc4340b6b32dd11effd5195e}

**入力（deleteMetadataFieldParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 削除するメタデータフィールドを含む会社へのハンドル。 |
| fieldHandle | `xsd:string` | はい | 削除するメタデータフィールドへのハンドル。 |

**出力（deleteMetadataFieldParam）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

このコードサンプルは、会社のメタデータフィールドを削除します。 このアクションを実行するには、IPS Web サービスサーバーに渡される `deleteMetadataFieldParam` のフィールドとして、会社ハンドルとメタデータハンドルを使用します。

**リクエスト**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**応答**

なし。0
