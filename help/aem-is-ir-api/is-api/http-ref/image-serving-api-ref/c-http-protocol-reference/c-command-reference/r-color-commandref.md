---
description: レイヤーの色 べた塗りレイヤーとエフェクトレイヤーの前景色と不透明度、およびテキストレイヤーのテキストボックスの塗りのカラーを指定します。
seo-description: レイヤーの色 べた塗りレイヤーとエフェクトレイヤーの前景色と不透明度、およびテキストレイヤーのテキストボックスの塗りのカラーを指定します。
seo-title: color
solution: Experience Manager
title: color
topic: Scene7 Image Serving - Image Rendering API
uuid: 46b93609-02c0-47bf-97c0-e7b2e416d292
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---


# color{#color}

レイヤーの色 べた塗りレイヤーとエフェクトレイヤーの前景色と不透明度、およびテキストレイヤーのテキストボックスの塗りのカラーを指定します。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>グレー、RGBまたはCMYKのカラー値（アルファ付き、アルファなし）。 </p> </td> 
 </tr> 
</table>

画像レイヤーおよびテキストレイヤーの場合、`color=`は、レイヤーの境界長方形内の透明で半透明の領域を、指定した色*で塗りつぶします（* `rotate=`と`extend=`が適用されます）。

## プロパティ {#section-d6e74c36a49547849212e4db8927e678}

レイヤー属性。 現在の画層に適用されます。`layer=comp`の場合は画層0に適用されます。

*`color`* は、のピクセルタイプに対応する作業カラースペースに存在すると見なされ *`color`*&#x200B;ます。*`color`* は、結合時にレイヤー画像のピクセルタイプが異なる場合、正確に変換されます。

## 初期設定 {#section-60611c72876b4c45b5c85ce35608e5ec}

べた塗りレイヤーとエフェクトレイヤーの初期設定はありません。色を指定する必要があります。 初期設定は0,0,0,0（完全に透明）です。

## 例 {#section-2d090493f4ec4e188bbc5565aa151a05}

次のテンプレートフラグメントでは、テキストの背景を不透明な50 %のカラーに設定し、同じカラーを使用して、レイヤー2画像の周囲に半透明の10ピクセルの境界線を追加します。

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 関連項目 {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [extend=, bgc=, bgc ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)  [, Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
