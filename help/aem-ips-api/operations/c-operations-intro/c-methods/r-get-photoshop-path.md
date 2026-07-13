---
description: 指定されたPhotoshop パスを囲む四角形の座標を返します。
solution: Experience Manager
title: getPhotoshopPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 46d88547-bb60-4370-9c79-bd281b40ba28
TQID: 'https://experienceleague.adobe.com/oYuZ7LC10b-3r3VvI-Kg4tlD7rMtshcswi3hctp6aUM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 16%

---

# getPhotoshopPath{#getphotoshoppath}

指定されたPhotoshop パスを囲む四角形の座標を返します。

構文

## 承認済みユーザータイプ {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## パラメーター {#section-ebffe496284c4ced9f329f78127be199}

**入力（getPhotoshopPathParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 取り扱う画像を持つ会社に処理します。 |
| assetHandle | `xsd:string` | はい | 画像アセットへのハンドル。 |
| pathName | `xsd:string` | はい | 返すPhotoshop パスの名前。 |

**出力（getPhotoshopPathReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| perspectiveQuad | `types:PerspectiveQuad` | はい | パスに基づいて画像座標を返します。 [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)を参照してください。 |

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

