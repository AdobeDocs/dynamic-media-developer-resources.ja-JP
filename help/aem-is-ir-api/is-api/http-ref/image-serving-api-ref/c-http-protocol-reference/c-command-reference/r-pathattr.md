---
title: pathAttr
description: パス上のテキスト属性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 1%

---

# pathAttr{#pathattr}

パス上のテキスト属性。

` pathAttr= *`direction`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 方向 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 標準 </span> | <span class="codeph"> 逆 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>パス上のテキストの開始位置（実際の 0.0...1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>パス上のテキストの終了位置（実際の 0.0...&lt;2.0）。 </p> </td> 
 </tr> 
</table>

最初のパス頂点の近くでテキストを描画する場合は `norm` を指定し、最後の頂点の近くでテキストを描画する場合は `reverse` を指定します。

*`startPos`* および *`endPos`* を使用すると、パス上でテキストを描画する場所を調整できます。 0.0 はパス内の最初の頂点に、1.0 は最後の頂点に対応します。中間値は、最初と最後の頂点間のパスに沿った距離を表します。

## プロパティ {#section-80f266da4e2549d89f022a3f9ff4584d}

レイヤー属性。 レイヤーに `textPs=` コマンドと `textPath=` コマンドが含まれていない場合は無視されます。

*`startPos`* は、0 以上 1.0 未満である必要があります。*`endPos`* は、開いたパスに適用される場合は *`startPos`* 以上 1.0 以下、閉じたパスに適用される場合は（*`startPos`* + 1.0）以下である必要があります。

## 初期設定 {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## 関連項目 {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
