---
description: レイヤー接触チャネル
seo-description: レイヤー接触チャネル
seo-title: 接触チャネル
solution: Experience Manager
title: 接触チャネル
topic: Scene7 Image Serving - Image Rendering API
uuid: a36fc0b6-7744-4c1c-b9f8-4aa31a886bff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 3%

---


# 接触チャネル{#origin}

レイヤー接触チャネル

`origin= *`共謀者`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 共謀者</span> </p></td> 
  <td class="stentry"> <p>レイヤーrectの左上隅からのピクセルオフセット(int、int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>レイヤーrectの中心からの正規化されたオフセット(real、real)。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>レイヤーrectには常に`extend=`による変更が含まれます。

レイヤーの長方形の位置を定義します。レイヤーの長方形は、`pos=`を介してレイヤー0を基準にして配置されます。 `originN=0,0` レイヤー接触チャネルを、レイヤーの長方形の中心に配置します。`originN=-0.5,-0.5` は左上隅 `origin=0,0` で、 `originN=0.5,0.5` はレイヤーの長方形の右下隅です。

## プロパティ {#section-60f639e36ada43d1abc6bfc100afc925}

レイヤー属性。 現在の画層に適用されます。`layer=comp`の場合は画層0に適用されます。 レイヤソースに適用されたレイヤ変換(`crop=`、`scale=`、`rotate=`、`flip=`)の影響を受けません。 `anchor=`を上書きします。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

`origin=`を指定しない場合、レイヤの接触チャネルは、レイヤの変換をイメージアンカーに適用することで決定されます。 画像アンカーが不明な場合は、レイヤーの長方形の中心(`originN=0,0`)が使用されます。

## 例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の例Aを参照してください。

## 関連項目 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
