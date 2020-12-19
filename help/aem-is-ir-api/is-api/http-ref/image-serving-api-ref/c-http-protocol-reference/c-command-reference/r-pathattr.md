---
description: テキストオンパス属性
seo-description: テキストオンパス属性
seo-title: pathAttr
solution: Experience Manager
title: pathAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b0ca5821-ee08-4c18-919d-775b75f19acd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 3%

---


# pathAttr{#pathattr}

テキストオンパス属性

` pathAttr= *``*[, *``*[, *`directionstartPosendPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 方向 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norm  </span> |  <span class="codeph"> reverse  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos  </span> </p> </td> 
  <td class="stentry"> <p>パス上のテキスト開始の位置（実数0.0 ～ 1.0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos  </span> </p> </td> 
  <td class="stentry"> <p>パス上のテキストの終了位置（実数0.0 ～ &lt;2.0） </p> </td> 
 </tr> 
</table>

最初のパスの頂点の近くで文字を描画する場合は`norm`を指定し、最後の頂点の近くで、逆方向に文字を描画する場合は`reverse`を指定します。

*`startPos`* パス上のテキストの描画位置を調整で *`endPos`* きます。0.0はパスの最初の頂点に対応し、1.0は最後の頂点に対応します。中間値は、最初と最後の頂点の間のパスに沿った距離を表します。

## プロパティ {#section-80f266da4e2549d89f022a3f9ff4584d}

レイヤー属性。 レイヤーに`textPs=`コマンドと`textPath=`コマンドが含まれていない場合は無視されます。

*`startPos`* は、0以上1.0未満である必要があります。開いているパスに適用する場合は1.0 *`endPos`* 以下、閉じているパスに適用する場合は *`startPos`*  *`startPos`* + 1.0以下である必要があります。

## 初期設定 {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## 関連項目 {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) 、 [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
