---
description: 画像アセットの画像データを置き換えます。
seo-description: 画像アセットの画像データを置き換えます。
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
topic: Scene7 Image Production System API
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# replaceImage{#replaceimage}

画像アセットの画像データを置き換えます。

構文

## 認証されたユーザータイプ {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**入力(replaceImageParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | はい | 置き換える画像を持つ会社へのハンドル。 |
| ` *`assetHandle`*` | `xsd:string` | はい | 置き換えるアセットのハンドル。 |
| ` *`urlModifier`*` | `xsd:string` | はい | 新しい画像データを生成するImage Serverコマンド。 |

**出力(replaceImageReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | はい | 新しいアセットの処理。 |

## 例 {#section-cebb93576bde4cb98cb27356ca66783b}

このコード例では、画像を置き換え、置き換え時にImage Server `urlModifier` が何も行わないことを示すコマンドを適用します。

**リクエスト**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**応答**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```

