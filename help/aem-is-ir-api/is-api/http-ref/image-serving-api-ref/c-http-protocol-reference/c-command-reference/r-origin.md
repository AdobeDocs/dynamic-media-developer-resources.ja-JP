---
description: レイヤーの原点。
seo-description: レイヤーの原点。
seo-title: 起源
solution: Experience Manager
title: 起源
topic: Scene7 Image Serving - Image Rendering API
uuid: a36fc0b6-7744-4c1c-b9f8-4aa31a886bff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 起源{#origin}

レイヤーの原点。

`origin= *`コード`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> コード</span> </p></td> 
  <td class="stentry"> <p>レイヤーrectの左上隅からのピクセルオフセット（整数、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>レイヤーrectの中心からの正規化されたオフセット（実数、実数）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>レイヤーrectには、常に、による変更が含まれま `extend=`す。

レイヤーの長方形の位置を定義します。レイヤーの長方形は、レイヤー0を基準にして配置されま `pos=`す。 `originN=0,0` レイヤーの原点をレイヤーの長方形の中央に配置します。 `originN=-0.5,-0.5` とは `origin=0,0` 、レイヤーの長方形の左上 `originN=0.5,0.5` 隅、および右下隅のことです。

## プロパティ {#section-60f639e36ada43d1abc6bfc100afc925}

レイヤー属性。 現在のレイヤに適用されます。レイヤ0の場合は適用されま `layer=comp`す。 レイヤソースに適用されたレ `crop=`イヤ変 `scale=`換(、、 `rotate=`、 `flip=`など)の影響を受けません。 Overrides `anchor=`. エフェクトレイヤーでは無視されます。

## 初期設定 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

を指定 `origin=` しない場合、レイヤの原点は、レイヤ変換をイメージアンカーに適用することで決まります。 画像アンカーが不明な場合は、レイヤーの長方形の中央( `originN=0,0`)が使用されます。

## 例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

テンプレートの例Aを参照し [てくださ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)い。

## 関連項目 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
