---
description: 表示の背景色 合成画像(表示画像)の背景色を指定します。
seo-description: 表示の背景色 合成画像(表示画像)の背景色を指定します。
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3ea8291e-3223-45ff-a2ad-43fc212eff90
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 3%

---


# bgc{#bgc}

表示の背景色 合成画像(表示画像)の背景色を指定します。

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span></span> </p> </td> 
  <td class="stentry"> <p>グレー、RGBまたはCMYKのカラー値 </p></td> 
 </tr> 
</table>

表示の背景に使用する不透明な塗りのカラーを指定します。 合成画像に透明な領域がある場合、または合成表示の縦横比が画像の長方形と異なる場合にのみ表示されます。 `fmt=tif-alpha`、`fmt=png-alpha`、または`req=mask`の場合は無視されます。

>[!NOTE]
>
>&#39;s&#39;色のサフィックスは`bgc=`で無視されます。 `bgc=`で指定されたカラー値は、常に各出力カラースペースに関連付けられます。

## プロパティ {#section-b729b50b1ea7433b82ba34ecd61839cd}

表示属性。 現在のレイヤー設定に関係なく適用されます。 `req=mask`、`fmt=tif-alpha`、`fmt=png-alpha`、`fmt=gif-alpha`、または`fmt=swf-alpha`の場合は無視されます。

colorで指定したアルファ値はすべて無視されます。

*`color`* は、出力カラースペース（で指定）に属していると見なされ、出力画像と同じピクセルタイプを持つ `icc=`必要があります。ピクセルタイプが一致しない場合、*`color`*&#x200B;は純粋な変換を使用して変換されます。

## 初期設定 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor` をクリックします。

## 例 {#section-7bcdfbc0e1274e86a69d39186b090789}

サムネール要求の明示的な背景色を指定します。

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 関連項目 {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [attribute::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8),  [fmt=req=, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)icc=leq,  [icc=loged ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)logent,  [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517) [logColor Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
