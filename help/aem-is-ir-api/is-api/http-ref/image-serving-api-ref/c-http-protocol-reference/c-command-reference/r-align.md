---
title: align
description: イメージをビューに位置合わせします。 wid=と hei=で定義されたビューの長方形内で、合成画像を位置合わせします（scl=が指定されている場合は、拡大縮小した後でも位置合わせできます）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# align{#align}

イメージをビューに位置合わせします。 wid=と hei=で定義されたビューの長方形内で、合成画像を位置合わせします（scl=が指定されている場合は、拡大縮小した後でも位置合わせできます）。

` align= *`horiz`*, *`vert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span> </span> </p> </td> 
  <td class="stentry"> <p>水平方向の位置揃え（実数、-1.0...1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span> </span> </p> </td> 
  <td class="stentry"> <p>垂直方向揃え（実数、-1.0...1.0） </p> </td> 
 </tr> 
</table>

合成画像の左上をビューの左上に位置合わせするには `align=-1,-1` を指定し、画像の右下をビューの右下に位置合わせするには `align=1,1` を指定します。 標準の画像リクエストおよびサムネールリクエストの場合、合成画像データでカバーされていないビューの領域はすべて `bgc=` で埋められます。

## プロパティ {#section-3fbec8206fc944eda4746d8be84f3b41}

ビュー属性。 （`align=` は、透かし画像と、透かしが適用される合成画像との間の位置揃えを定義する場合にも使用されます）。 現在のレイヤ設定に関係なく適用されます。 `wid=` と `hei=` の 1 つのみが指定され、`fit=constrain` または `fit=stretch` の場合は無視されます。

## 初期設定 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`：ビューの長方形の中心にイメージを配置します。

## 例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

次のリクエストは `myImage`200 x 200 ピクセルのビューの長方形に収まります。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

`myImage` が完全に正方形の場合は、ビューの長方形全体が塗りつぶされます。 アスペクト比が縦長の `myImage` 合は、高さが 200 ピクセルに調整され、ビュー内で水平方向に中央揃えされます。 アスペクト比が横長の `myImage` 合は、幅 200 ピクセルに調整され、ビューの上端に揃えられます。 いずれの場合も、返される画像のサイズは正確に 200 x 200 ピクセルです。拡大縮小された `myImage` で覆われていないスペースは、`attribute::BkgColor` で満たされます（背景色を動的に制御するには bgc=を指定します）。

## 関連項目 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [&#x200B; 透かし &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
