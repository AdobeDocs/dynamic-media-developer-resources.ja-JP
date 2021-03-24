---
description: 画像アセットの画像データを置換します。
solution: Experience Manager
title: replaceImage
feature: Dynamic Mediaクラシック，SDK/API，アセット管理
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 15%

---


# replaceImage{#replaceimage}

画像アセットの画像データを置換します。

構文

## 認証済みユーザータイプ{#section-e2aad71fb2a54612badc7b16f82ed544}

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
| `*`companyName`*` | `xsd:string` | はい | 置き換える会社を含む画像へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | 置き換えるアセットのハンドル。 |
| `*`urlModifier`*` | `xsd:string` | はい | 新しい画像データを生成するImage Serverコマンド。 |

**出力(replaceImageReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | はい | 新しいアセットのハンドル。 |

## 例 {#section-cebb93576bde4cb98cb27356ca66783b}

次のコードのサンプルを使用すると、画像を置き換え、`urlModifier`を置き換え時にImage Serverが何も行わないことを示すコマンドに適用できます。

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

