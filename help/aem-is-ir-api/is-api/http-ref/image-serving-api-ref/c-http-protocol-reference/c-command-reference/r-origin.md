---
description: 画層の原点
solution: Experience Manager
title: origin
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---

# origin{#origin}

画層の原点

`origin= *`コード`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> コード</span> </p></td> 
  <td class="stentry"> <p>レイヤーrectの左上隅からのピクセルオフセット（整数、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>レイヤーレクトの中心からの正規化オフセット（実数、実数）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>レイヤーの直接には、常に`extend=`による変更が含まれます。

レイヤーの長方形の配置ポイントを定義します。このポイントを使用して、`pos=`を介してレイヤー0を基準にレイヤーの長方形を配置します。 `originN=0,0` は、画層の原点を画層の長方形の中心に配置します。`originN=-0.5,-0.5` と `origin=0,0` は、レイヤーの長方形 `originN=0.5,0.5` の左上隅、右下隅です。

## プロパティ {#section-60f639e36ada43d1abc6bfc100afc925}

レイヤー属性。 現在の画層に適用され、 `layer=comp`の場合は画層0に適用されます。 レイヤソースに適用されたレイヤ変換(`crop=`、`scale=`、`rotate=`、`flip=`)の影響を受けません。 `anchor=`を上書きします。 エフェクトレイヤでは無視されます。

## 初期設定 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

`origin=`を指定しない場合、レイヤーの原点は、レイヤー変換をイメージアンカーに適用することで決定されます。 画像アンカーが不明な場合は、レイヤーの長方形の中心(`originN=0,0`)が使用されます。

## 例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の例Aを参照してください。

## 関連項目 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
