---
title: bgc
description: 背景色を表示します。 合成画像（ビュー画像）の背景色を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
TQID: 'https://experienceleague.adobe.com/XE6I3hjg95AVJYiszVOlRsn19YSA3bhomHNxJlFmVDs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 2%

---

# bgc{#bgc}

背景色を表示します。 合成画像（ビュー画像）の背景色を指定します。

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> カラー</span></span> </p> </td> 
  <td class="stentry"> <p>グレー、RGB、またはCMYK カラー値。 </p></td> 
 </tr> 
</table>

ビューの背景に使用する不透明な塗りのカラーを指定します。 合成画像に透明な領域がある場合、または合成画像の縦横比がビューの長方形と異なる場合にのみ表示されます。 `fmt=tif-alpha`、`fmt=png-alpha`、または`req=mask`の場合は無視されます。

>[!NOTE]
>
>&#39;s&#39; カラーサフィックスは`bgc=`によって無視されます。 `bgc=`で指定されたカラー値は、常にそれぞれの出力カラースペースに関連付けられます。

## プロパティ {#section-b729b50b1ea7433b82ba34ecd61839cd}

ビュー属性。 現在のレイヤー設定に関係なく適用されます。 `req=mask`、`fmt=tif-alpha`、`fmt=png-alpha`、`fmt=gif-alpha`または`fmt=swf-alpha`の場合、無視されます。

colorで指定されたアルファ値は無視されます。

*`color`*&#x200B;は出力カラースペース（`icc=`で指定）に属していると見なされ、出力画像と同じピクセルタイプを持つ必要があります。 ピクセルタイプが一致しない場合、*`color`*&#x200B;はネイティブ変換を使用して変換されます。

## 初期設定 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## 例 {#section-7bcdfbc0e1274e86a69d39186b090789}

サムネールリクエストの明示的な背景色を指定します。

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 関連項目 {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [属性：:BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [ カラーマネジメント ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
