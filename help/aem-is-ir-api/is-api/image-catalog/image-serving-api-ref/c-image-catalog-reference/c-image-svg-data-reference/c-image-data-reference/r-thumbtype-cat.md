---
description: サムネールタイプ： この画像のサムネールの生成方法を示します。
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
TQID: 'https://experienceleague.adobe.com/NLLvcORaHjSiRO1sVJL7BzZfXpXkTOC2NkyPaJ4-3cs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 1%

---

# ThumbType{#thumbtype}

サムネールタイプ： この画像のサムネールの生成方法を示します。

次のサムネールタイプがサポートされています。

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>切り抜き（1） </p></td> 
  <td class="stentry"> <p>画像をサムネールの縦横比に切り抜きます。 サムネール長方形と画像の縦横比がまったく同じでない限り、画像のサイズの一部が切り抜かれ、サムネール長方形全体に画像データが表示されます。 切り抜き長方形は、<span class="codeph">属性：:ThumbHorizAlign</span>と<span class="codeph">属性：:ThumbVertAlign</span>を使用して画像内に配置されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>フィット （2） </p></td> 
  <td class="stentry"> <p>画像全体をサムネール長方形に合わせます。 画像は、<span class="codeph">属性：:ThumbHorizAlign</span>および<span class="codeph">属性：:ThumbVertAlign</span>を使用してサムネール長方形の中に配置され、追加のスペースには<span class="codeph">属性：:ThumbBkgColor</span>が入力されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>テクスチャ （3） </p></td> 
  <td class="stentry"> <p>解像度に基づいて画像を切り抜きます。 画像は、<span class="codeph"> カタログ：:ThumbRes</span>と<span class="codeph"> カタログ：:Resolution</span>の比率で拡大・縮小されます。 結果の画像がサムネールよりも大きい場合は、画像が収まるように切り抜かれます。拡大・縮小された画像がサムネールよりも小さい場合、残りの領域には<span class="codeph">属性：:ThumbBkgColor</span>が表示されます。 <span class="codeph">属性：:ThumbHorizAlign</span>および<span class="codeph">属性：:ThumbVertAlign</span>は、サムネール内の大きな画像内の切り抜き長方形の位置または小さな画像内の小さな画像の位置を決定するために使用されます。 </p></td> 
 </tr> 
</table>

クライアントは、`req=tmb`件のリクエストを含む画像のサムネールをリクエストします。

## プロパティ {#section-c58a8e67c2134ca3a0edd21b20dd3052}

列挙値。 有効な値は1、2、3で、それぞれ切り抜き、フィット、テクスチャの種類に対応します。

## 初期設定 {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType`は、フィールドが存在しない場合、値が0の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-fc1a79d3e6274b4381a17da159649a07}

[属性：:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5)、[属性：:ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e)、[属性：:ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691)、[属性：:ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f)、[ カタログ：:ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)、[ カタログ：Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)、[req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
