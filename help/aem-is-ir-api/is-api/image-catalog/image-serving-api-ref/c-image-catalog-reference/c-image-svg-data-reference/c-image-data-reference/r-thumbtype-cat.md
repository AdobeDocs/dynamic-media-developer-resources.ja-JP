---
description: サムネールのタイプ。 この画像のサムネールの生成方法を説明します。
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 1%

---

# ThumbType{#thumbtype}

サムネールのタイプ。 この画像のサムネールの生成方法を説明します。

次のサムネールタイプがサポートされています。

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>切り抜き(1) </p></td> 
  <td class="stentry"> <p>画像をサムネールの縦横比に切り抜きます。 サムネールの長方形と画像の縦横比が完全に同じでない限り、画像の一部が切り抜かれ、サムネールの長方形全体が画像データで埋められます。 切り抜き長方形は、 <span class="codeph"> attribute::ThumbHorizAlign</span>および<span class="codeph"> attribute::ThumbVertAlign</span>を使用して画像内に配置されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>フィット(2) </p></td> 
  <td class="stentry"> <p>画像全体をサムネールの長方形に合わせます。 画像は、 <span class="codeph"> attribute::ThumbHorizAlign</span>および<span class="codeph"> attribute::ThumbVertAlign</span>を使用してサムネールの長方形内に配置され、余分なスペースは<span class="codeph"> attribute::ThumbBkgColor</span>で埋められます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>テクスチャ(3) </p></td> 
  <td class="stentry"> <p>解像度に基づいて画像を切り抜きます。 画像は、<span class="codeph"> catalog::ThumbRes</span>と<span class="codeph"> catalog::Resolution</span>の比率で拡大/縮小されます。 結果の画像がサムネールより大きい場合は切り抜かれ、縮小された画像がサムネールより小さい場合は残りの領域が<span class="codeph">属性：:ThumbBkgColor</span>で塗りつぶされます。 <span class="codeph"> attribute::</span> ThumbHorizAlignand  <span class="codeph"> attribute::</span> ThumbVertAlignは、大きい画像内の切り抜き長方形の位置や、サムネール内の小さい画像の位置を決定するために使用されます。 </p></td> 
 </tr> 
</table>

クライアントは`req=tmb`リクエストを含むイメージサムネールを要求します。

## プロパティ {#section-c58a8e67c2134ca3a0edd21b20dd3052}

列挙値。 有効な値は、それぞれ[切り抜き]、[フィット]、[テクスチャ]の各タイプに対応する1、2、3です。

## 初期設定 {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` が使用されるのは、フィールドが存在しない場合、値が0の場合、またはフィールドが空の場合です。

## 関連項目 {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) 、 [attribute::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e)、 [attribute::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691)、 [attribute::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f)、 [catalog::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)、 [catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)、 [tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、 [Thumbnail Scaling Scaling Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
