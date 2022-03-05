---
description: テキストオンパスの属性。
solution: Experience Manager
title: pathAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---

# pathAttr{#pathattr}

テキストオンパスの属性。

` pathAttr= *`方向`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 方向 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norm </span> | <span class="codeph"> 逆 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>パス上のテキストの開始位置（実数 0.0 ～ 1.0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>パス上のテキストの終了位置（実数 0.0...&lt;2.0）。 </p> </td> 
 </tr> 
</table>

指定 `norm` 最初のパスの頂点の近くからテキストを描画し、 `reverse` を指定すると、最後の頂点の近くから、反対の方向にテキストが描画されます。

*`startPos`* および *`endPos`* パス上のテキストの描画位置を調整できます。 0.0 はパスの最初の頂点に、1.0 は最後の頂点に対応します。中間値は、最初の頂点と最後の頂点の間のパスに沿った距離を表します。

## プロパティ {#section-80f266da4e2549d89f022a3f9ff4584d}

レイヤー属性。 画層が含まれない場合は無視 `textPs=` および `textPath=` コマンド

*`startPos`* は、0 以上 1.0 未満である必要があります。 *`endPos`* は、より大きい値にする必要があります *`startPos`* 開いたパスに適用される場合は 1.0 以下、または（以下） *`startPos`* + 1.0) を閉じたパスに適用した場合。

## 初期設定 {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## 関連項目 {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
