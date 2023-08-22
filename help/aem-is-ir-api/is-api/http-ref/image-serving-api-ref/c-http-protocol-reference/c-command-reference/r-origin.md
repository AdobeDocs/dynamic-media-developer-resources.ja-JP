---
title: origin
description: 画層の原点。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# origin{#origin}

画層の原点。

`origin= *`コード`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> コード</span> </p></td> 
  <td class="stentry"> <p>レイヤー rect の左上隅からのピクセルオフセット（整数、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>レイヤーの直角の中心からの正規化されたオフセット（実数、実数）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>レイヤーの直接には、次の変更が常に含まれます。 `extend=`.

レイヤーの長方形の位置を定義します。レイヤーの長方形は、レイヤー 0 を基準にして配置されます。 `pos=`. `originN=0,0` 画層の原点を、画層の長方形の中心に配置します。 `originN=-0.5,-0.5` および `origin=0,0` は左上隅で、 `originN=0.5,0.5` は、レイヤーの長方形の右下隅です。

## プロパティ {#section-60f639e36ada43d1abc6bfc100afc925}

レイヤー属性。 現在の画層に適用されます。 `layer=comp`. レイヤー変換の影響を受けません ( `crop=`, `scale=`, `rotate=`, `flip=`) を適用します。 上書き `anchor=`. 効果画層で無視されます。

## 初期設定 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

次の場合 `origin=` を指定しない場合、レイヤーの原点は、レイヤー変換を画像アンカーに適用することで決定されます。 画像アンカーが不明な場合は、レイヤーの長方形の中心 ( `originN=0,0`) が使用されます。

## 例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

詳しくは、の例 A を参照してください。 [テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 関連項目 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
