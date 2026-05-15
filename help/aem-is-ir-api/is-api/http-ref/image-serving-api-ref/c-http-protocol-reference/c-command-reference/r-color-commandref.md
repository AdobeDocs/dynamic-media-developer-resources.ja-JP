---
title: color
description: レイヤーカラー： 単色レイヤーとエフェクトレイヤーの描画色と不透明度、およびテキストレイヤーのテキストボックスの塗りの色を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
TQID: 'https://experienceleague.adobe.com/tjiZfVTztBPgsIYS1SGtVeBxo0Wq1q8Ur-kq3Xtm6og'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 3%

---

# color{#color}

レイヤーカラー： 単色レイヤーとエフェクトレイヤーの描画色と不透明度、およびテキストレイヤーのテキストボックスの塗りの色を指定します。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> カラー</span> </span> </p> </td> 
  <td class="stentry"> <p>アルファの有無にかかわらず、グレー、RGB、またはCMYK カラー値。 </p> </td> 
 </tr> 
</table>

画像とテキストのレイヤーがある場合、`color=`は、指定した色* `rotate=`と`extend=`が適用される前に、レイヤーのバウンディング矩形内の透明および半不透明な領域を塗りつぶします。

## プロパティ {#section-d6e74c36a49547849212e4db8927e678}

レイヤー属性。 現在のレイヤーまたは`layer=comp`のレイヤー0に適用されます。

修飾子&#x200B;*`color`*&#x200B;は、*`color`*&#x200B;のピクセルタイプに対応する作業用カラースペースに存在すると想定されます。 また、結合時にレイヤー画像のピクセルタイプが異なる場合は、*`color`*&#x200B;が正確に変換されます。

## 初期設定 {#section-60611c72876b4c45b5c85ce35608e5ec}

単色レイヤーとエフェクトレイヤーのデフォルトはありません。カラーを指定する必要があります。 画像レイヤーとテキストレイヤーのデフォルトは0,0,0,0 （完全に透明）です。

## 例 {#section-2d090493f4ec4e188bbc5565aa151a05}

次のテンプレートフラグメントでは、テキストの背景が50%不透明カラーに設定され、同じカラーを使用して、レイヤー2の画像の周囲に半透明の10 ピクセルの境界線を追加します。

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 関連項目 {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)、[bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)、[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)、[extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)、[bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)、[&#x200B; カラーマネジメント &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
