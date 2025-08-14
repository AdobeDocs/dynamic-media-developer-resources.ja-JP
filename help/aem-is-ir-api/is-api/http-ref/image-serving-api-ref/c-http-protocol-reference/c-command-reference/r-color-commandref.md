---
title: color
description: レイヤーのカラー。 塗りつぶしレイヤーと効果レイヤーの前景色と不透明度、およびテキストレイヤーのテキストボックスの塗りつぶしカラーを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---

# color{#color}

レイヤーのカラー。 塗りつぶしレイヤーと効果レイヤーの前景色と不透明度、およびテキストレイヤーのテキストボックスの塗りつぶしカラーを指定します。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color </span> </span> </p> </td> 
  <td class="stentry"> <p>グレー、RGBまたは CMYK カラー値（アルファ付きまたはアルファなし）。 </p> </td> 
 </tr> 
</table>

画像レイヤーとテキストレイヤーがあ `color=` 場合は、レイヤーの境界長方形内の透明な領域と半不透明な領域を、指定した色*で塗りつぶします。その後、`rotate=` と `extend=` が適用されます。

## プロパティ {#section-d6e74c36a49547849212e4db8927e678}

レイヤー属性。 現在の画層、または `layer=comp` の場合は画層 0 に適用されます。

修飾子 *`color`* は、*`color`* のピクセルタイプに対応する作業カラースペースに存在すると想定されます。 また、レイヤー画像のピクセルタイプがマージ時に異なる場合は、*`color`* を正確に変換します。

## 初期設定 {#section-60611c72876b4c45b5c85ce35608e5ec}

単色レイヤーとエフェクトレイヤーのデフォルトはありません。色を指定する必要があります。 画像レイヤーとテキストレイヤーのデフォルトは 0,0,0,0 （完全に透明）です。

## 例 {#section-2d090493f4ec4e188bbc5565aa151a05}

次のテンプレートフラグメントでは、テキストの背景が 50% 不透明の色に設定されており、同じ色を使用してレイヤー 2 画像の周囲に半透明の 10 ピクセルの境界線を追加しています。

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 関連項目 {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [ カラーマネジメント ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
