---
title: 起源
description: レイヤーの原点。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---

# 起源{#origin}

レイヤーの原点。

`origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>レイヤー長方形の左上隅からのピクセルオフセット （int、int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>レイヤーの中心からの正規化されたオフセット（実際、実際）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>レイヤー rect には、`extend=` による変更が常に含まれます。

レイヤーの長方形の位置合わせポイントを定義します。レイヤーの長方形は、`pos=` を介してレイヤー 0 を基準にレイヤーの長方形を配置するために使用されます。 レイヤーの原点 `originN=0,0` レイヤーの長方形の中心に配置します。 `originN=-0.5,-0.5` と `origin=0,0` はレイヤーの左上隅、`originN=0.5,0.5` はレイヤーの長方形の右下隅です。

## プロパティ {#section-60f639e36ada43d1abc6bfc100afc925}

レイヤー属性。 現在の画層、または `layer=comp` の場合は画層 0 に適用されます。 レイヤーソースに適用されるレイヤー変換（`crop=`、`scale=`、`rotate=`、`flip=`）の影響を受けません。 `anchor=` を上書きします。 エフェクトレイヤーで無視されます。

## 初期設定 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

`origin=` が指定されていない場合、レイヤーの原点は、レイヤーの変換を画像アンカーに適用することによって決定されます。 画像アンカーが不明な場合は、レイヤーの長方形の中心（`originN=0,0`）が使用されます。

## 例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) の例 A を参照してください。

## 関連項目 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
