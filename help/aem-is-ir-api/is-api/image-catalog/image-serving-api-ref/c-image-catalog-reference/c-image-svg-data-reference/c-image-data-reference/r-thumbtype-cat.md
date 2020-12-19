---
description: サムネールの種類 この画像のサムネールの生成方法を説明します。
seo-description: サムネールの種類 この画像のサムネールの生成方法を説明します。
seo-title: ThumbType
solution: Experience Manager
title: ThumbType
topic: Scene7 Image Serving - Image Rendering API
uuid: b737b5a4-ad6d-4a9c-b48f-81cf170dd210
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---


# ThumbType{#thumbtype}

サムネールの種類 この画像のサムネールの生成方法を説明します。

次のサムネールタイプがサポートされています。

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>切り抜き(1) </p></td> 
  <td class="stentry"> <p>サムネールの縦横比に合わせて画像を切り抜きます。 サムネールの長方形と画像の縦横比が完全に同じでない限り、サムネールの長方形全体が画像データで埋まるように、画像の一部が切り抜かれます。 切り抜き長方形は、<span class="codeph"> attribute::ThumbHorizAlign</span> and <span class="codeph"> attribute::ThumbVertAlign</span>を使用して画像内に配置されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>フィット(2) </p></td> 
  <td class="stentry"> <p>画像全体をサムネールの長方形に合わせます。 画像は、<span class="codeph">属性：ThumbHorizAlign</span>と<span class="codeph">属性：:ThumbVertAlign</span>を使用してサムネールの長方形内に配置され、余分なスペースは<span class="codeph">属性：:ThumbBkgColor</span>で埋められます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>テクスチャ(3) </p></td> 
  <td class="stentry"> <p>解像度に基づいて画像を切り抜きます。 画像は、<span class="codeph"> catalog::ThumbRes</span>と<span class="codeph"> catalog::Resolution</span>の比率で拡大縮小されます。 結果の画像がサムネールより大きい場合は切り抜かれ、サイズ調整された画像がサムネールより小さい場合は、残りの領域が<span class="codeph">属性：:ThumbBkgColor</span>で塗りつぶされます。 <span class="codeph"> attribute::</span> ThumbHorizAlignand  <span class="codeph"> attribute::</span> ThumbVertAlignを使用して、大きい画像内の切り抜き長方形の位置、またはサムネール内の小さい画像の位置を決定します。 </p></td> 
 </tr> 
</table>

クライアントは`req=tmb`リクエストを含む画像サムネールを要求します。

## プロパティ {#section-c58a8e67c2134ca3a0edd21b20dd3052}

列挙値。 有効な値は1、2または3です。これらは、それぞれ切り抜き、フィット、テクスチャの各タイプに対応します。

## 初期設定 {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` は、フィールドが存在しない場合、値が0の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ,  [attribute::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e),  [:ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691):ThumbHorizAlign [](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f) [](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69) [](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) [](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) [:ThumbHorizAlignAlign, AlignAlignCatalog:Thumb Attribute Res, Res, Re, Mb, Mb, Scalog, Namnal](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
