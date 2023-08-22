---
title: bgc
description: 背景色を表示します。 合成画像（表示画像）の背景色を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# bgc{#bgc}

背景色を表示します。 合成画像（表示画像）の背景色を指定します。

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> カラー</span></span> </p> </td> 
  <td class="stentry"> <p>グレー、RGB、CMYK のカラー値。 </p></td> 
 </tr> 
</table>

ビューの背景に使用する不透明な塗りのカラーを指定します。 合成画像に透明な領域がある場合、または合成画像の縦横比が表示の長方形と異なる場合にのみ表示されます。 次の場合は無視 `fmt=tif-alpha` または `fmt=png-alpha`または `req=mask`.

>[!NOTE]
>
>「s」のカラーサフィックスは次の条件で無視されます： `bgc=`. で指定したカラー値 `bgc=` は、常にそれぞれの出力カラースペースに関連付けられます。

## プロパティ {#section-b729b50b1ea7433b82ba34ecd61839cd}

属性を表示します。 現在の画層設定に関係なく適用されます。 次の場合は無視 `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha`または `fmt=swf-alpha`.

color で指定されたすべてのアルファ値は無視されます。

*`color`* は出力カラースペースに属していると見なされます ( `icc=`) およびは、出力画像と同じピクセルタイプにする必要があります。 ピクセルタイプが一致しない場合、 *`color`* は純粋な変換を使用して変換されます。

## 初期設定 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor` をクリックします。

## 例 {#section-7bcdfbc0e1274e86a69d39186b090789}

サムネール要求の明示的な背景色を指定します。

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 関連項目 {#section-1e55f9f98f1847918a1725836a27cfaa}

[カラー](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [attribute::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [カラーマネジメント](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
