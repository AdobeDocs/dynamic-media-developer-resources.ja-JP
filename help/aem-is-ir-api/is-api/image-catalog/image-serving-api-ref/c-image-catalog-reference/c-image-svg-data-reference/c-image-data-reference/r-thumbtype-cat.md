---
description: サムネールのタイプ。 この画像のサムネールを生成する方法を説明します。
solution: Experience Manager
title: ThubType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# ThubType{#thumbtype}

サムネールのタイプ。 この画像のサムネールを生成する方法を説明します。

次のサムネールのタイプがサポートされています。

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>切り抜き（1） </p></td> 
  <td class="stentry"> <p>サムネールの縦横比に画像を切り抜きます。 サムネールの長方形と画像のアスペクト比がまったく同じでない限り、サムネールの長方形全体に画像データが確実に入力されるように、画像の一部が切り抜かれます。 切り抜き長方形は、属性：:ThumbHorizAlign<span class="codeph"> 属性：:ThumbVertAlign</span> を使用して画像内 <span class="codeph"> 配置 </span> れます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>フィット （2） </p></td> 
  <td class="stentry"> <p>画像全体をサムネールの長方形に合わせます。 <span class="codeph"> 画像は、属性：:ThumbHorizAlign</span> 属性：:ThumbVertAlign<span class="codeph"> を使用してサムネールの長方形内に配置さ </span>、追加のスペースは属性：:ThumbBkgColor<span class="codeph"> で埋め </span> れます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>テクスチャ （3） </p></td> 
  <td class="stentry"> <p>解像度に基づいて画像を切り抜きます。 画像は、カタログ：:ThumbRes<span class="codeph"> とカタログ：:Resolution</span><span class="codeph"> 比率 </span> よって拡大縮小されます。 結果の画像がサムネールよりも大きい場合は、収まるように切り抜かれます。拡大縮小された画像がサムネールよりも小さい場合は、残りの領域が <span class="codeph"> の属性：:ThumbBkgColor</span> で塗りつぶされます。 <span class="codeph"> 属性：:ThumbHorizAlign</span> および <span class="codeph"> 属性：:ThumbVertAlign</span> を使用して、大きい画像の切り抜き長方形の位置またはサムネール内の小さい画像の位置を決定します。 </p></td> 
 </tr> 
</table>

クライアントは、`req=tmb` 要求で画像サムネールを要求します。

## プロパティ {#section-c58a8e67c2134ca3a0edd21b20dd3052}

列挙値。 有効な値は 1、2、3 で、それぞれ切り抜き、フィット、テクスチャのタイプに対応します。

## 初期設定 {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` は、フィールドが存在しない場合、値が 0 の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5)、[attribute::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e)、[attribute::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691)、[attribute::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f)、[catalog::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)、[catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)、[req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[&#x200B; サムネールの拡大縮小 &#x200B;](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
