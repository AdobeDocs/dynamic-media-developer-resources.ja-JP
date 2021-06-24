---
description: レイヤーカラー べた塗りレイヤーと効果レイヤーの前景色と不透明度、およびテキストレイヤーのテキストボックスの塗りのカラーを指定します。
solution: Experience Manager
title: color
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 4%

---

# color{#color}

レイヤーカラー べた塗りレイヤーと効果レイヤーの前景色と不透明度、およびテキストレイヤーのテキストボックスの塗りのカラーを指定します。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>グレー、RGBまたはCMYKのカラー値（アルファ付きまたはアルファなし）。 </p> </td> 
 </tr> 
</table>

画像レイヤーとテキストレイヤーの場合、`color=`は、`rotate=`と`extend=`の前に指定された色*で、レイヤーの境界の長方形内の透明で半不透明な領域を塗りつぶします。

## プロパティ {#section-d6e74c36a49547849212e4db8927e678}

レイヤー属性。 現在の画層に適用され、 `layer=comp`の場合は画層0に適用されます。

*`color`* は、のピクセルタイプに対応する作業用カラースペースに存在すると見なされま *`color`*&#x200B;す。*`color`* は、マージ時にレイヤー画像のピクセルタイプが異なる場合、正確に変換されます。

## 初期設定 {#section-60611c72876b4c45b5c85ce35608e5ec}

べた塗りレイヤーとエフェクトレイヤーのデフォルトはありません。色を指定する必要があります。 初期設定は、画像レイヤーとテキストレイヤーの場合は0,0,0,0 （完全に透明）です。

## 例 {#section-2d090493f4ec4e188bbc5565aa151a05}

次のテンプレートフラグメントでは、テキストの背景を50%不透明なカラーに設定し、同じカラーを使用して、レイヤー2画像の周囲に半透明の10ピクセルの境界線を追加します。

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 関連項目 {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)、 [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)、 [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)、 [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)、 [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)、 [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
