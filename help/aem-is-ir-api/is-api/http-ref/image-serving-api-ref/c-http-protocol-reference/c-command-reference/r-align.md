---
title: 整列
description: 画像を表示に合わせます。 wid=および hei=で定義されたビューの長方形内で、合成画像を揃えます（scl=が指定されている場合もあります）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# 整列{#align}

画像を表示に合わせます。 wid=および hei=で定義されたビューの長方形内で、合成画像を揃えます（scl=が指定されている場合もあります）。

` align= *`horiz`*, *`vert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span> </span> </p> </td> 
  <td class="stentry"> <p>水平方向の整列（実数、-1.0 ～ 1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span> </span> </p> </td> 
  <td class="stentry"> <p>垂直方向の整列（実数、-1.0 ～ 1.0） </p> </td> 
 </tr> 
</table>

指定 `align=-1,-1` 合成画像の左上をビューの左上に揃えるには、次のように指定します。 `align=1,1` 画像の右下をビューの右下に揃えます。 標準の画像要求およびサムネール要求の場合、合成画像データで覆われていないビューの領域は、 `bgc=`.

## プロパティ {#section-3fbec8206fc944eda4746d8be84f3b41}

属性を表示します。 ( `align=` は、透かし画像と透かしが適用される合成画像との位置合わせを定義する場合にも使用します )。 現在の画層設定に関係なく適用されます。 次のいずれか 1 つのみの場合は無視 `wid=` および `hei=` が指定され、 `fit=constrain` または `fit=stretch`.

## 初期設定 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`：画像をビューの長方形の中央に配置します。

## 例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

次のリクエストが適合します `myImage` を 200x200 ピクセル表示の長方形に変換します。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

次の場合 `myImage` が正方形の場合は、ビューの長方形全体を塗りつぶします。 次の場合 `myImage` 縦長の縦横比の場合は、高さが 200 ピクセルになるように拡大縮小され、ビューの水平方向の中央に配置されます。 次の場合 `myImage` 横長の縦横比の場合は、幅が 200 ピクセルに拡大縮小され、ビューの上端に合わせて整列します。 どの場合も、返される画像のサイズはちょうど 200 x 200 ピクセルで、拡大/縮小された画像で覆われていない領域です `myImage` が次の値でいっぱい： `attribute::BkgColor` （背景色を動的に制御するには bgc=を指定します）。

## 関連項目 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [透かし](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
