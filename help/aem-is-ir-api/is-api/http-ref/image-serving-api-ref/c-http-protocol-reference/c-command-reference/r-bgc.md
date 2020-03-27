---
description: ビューの背景色 合成画像（ビュー画像）の背景色を指定します。
seo-description: ビューの背景色 合成画像（ビュー画像）の背景色を指定します。
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 3ea8291e-3223-45ff-a2ad-43fc212eff90
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bgc{#bgc}

ビューの背景色 合成画像（ビュー画像）の背景色を指定します。

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 色</span></span> </p> </td> 
  <td class="stentry"> <p>グレー、RGBまたはCMYKのカラー値。 </p></td> 
 </tr> 
</table>

ビューの背景に使用する不透明な塗りのカラーを指定します。 合成画像に透明な領域がある場合、または合成画像の縦横比が表示長方形と異なる場合にのみ表示されます。 またはの場合 `fmt=tif-alpha` は無 `fmt=png-alpha`視されま `req=mask`す。

>[!NOTE]
>
>「s」の色サフィックスはで無視されま `bgc=`す。 で指定したカラー値は、 `bgc=` 常に各出力カラースペースに関連付けられます。

## プロパティ {#section-b729b50b1ea7433b82ba34ecd61839cd}

属性を表示します。 現在のレイヤー設定に関係なく適用されます。 、、、、ま `req=mask`たはの場 `fmt=tif-alpha`合は `fmt=png-alpha`無視 `fmt=gif-alpha`されま `fmt=swf-alpha`す。

colorで指定されたアルファ値は無視されます。

*`color`* は出力カラースペース（で指定）に属していると見なされ、出力画像と同じ `icc=`ピクセルタイプを持つ必要があります。 ピクセルの種類が一致しない場合、は純粋な *`color`* 変換を使用して変換されます。

## 初期設定 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor` をクリックします。

## 例 {#section-7bcdfbc0e1274e86a69d39186b090789}

サムネール要求の明示的な背景色を指定します。

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 関連項目 {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [attribute::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)req, [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)req, [icc,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)neg, [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
