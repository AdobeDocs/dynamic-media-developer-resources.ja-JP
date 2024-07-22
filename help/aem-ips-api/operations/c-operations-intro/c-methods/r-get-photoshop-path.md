---
description: 指定されたPhotoshop パスを含む四辺形の座標を返します。
solution: Experience Manager
title: getPhotoshopPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 46d88547-bb60-4370-9c79-bd281b40ba28
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 16%

---

# getPhotoshopPath{#getphotoshoppath}

指定されたPhotoshop パスを含む四辺形の座標を返します。

構文

## 許可されているユーザータイプ {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* “

## パラメーター {#section-ebffe496284c4ced9f329f78127be199}

**入力（getPhotoshopPathParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 操作する画像を持つ会社にハンドルします。 |
| assetHandle | `xsd:string` | はい | 画像アセットへのハンドル。 |
| pathName | `xsd:string` | はい | 返すPhotoshop パスの名前。 |

**出力（getPhotoshopPathReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| perspectiveQuad | `types:PerspectiveQuad` | はい | パスに基づいて画像座標を返します。 [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204) を参照してください。 |

## 例 {#section-1f0461cbdc184c8d8925336d5279db47}

**リクエスト**

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**応答**

```java
<getPhotoshopPathReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <perspectiveQuad>
    <x0>932.19</x0>
    <y0>296.592</y0>
    <x1>968.769</x1>
    <y1>320.16</y1>
    <x2>1119.56</x2>
    <y2>1200.0</y2>
    <x3>900.43</x3>
    <y3>1200.0</y3>
  </perspectiveQuad>
</getPhotoshopPathReturn>
```

>[!MORELIKETHIS]
>
>* [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)
