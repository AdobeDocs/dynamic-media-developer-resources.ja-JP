---
title: pathAttr
description: パス上テキスト属性：
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
TQID: 'https://experienceleague.adobe.com/A7uOgsYtOH6AmVOtbUfQDVJHwJEkCSXqBYavY9CbRkw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 1%

---

# pathAttr{#pathattr}

パス上テキスト属性：

` pathAttr= *`方向`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">方向</span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ノルム </span> | <span class="codeph"> リバース </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>パス上のテキスト開始位置（実数0.0...1.0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>パス上のテキスト終了位置（実数0.0...&lt;2.0） </p> </td> 
 </tr> 
</table>

最初のパスの頂点の近くで始まるテキストを描画するには`norm`を指定し、最後の頂点の近くで始まる反対方向にテキストを描画するには`reverse`を指定します。

*`startPos`*&#x200B;と&#x200B;*`endPos`*&#x200B;では、パス上のテキストの描画位置を調整できます。 0.0はパスの最初の頂点に対応し、1.0は最後の頂点に対応します。中間値は、最初と最後の頂点の間のパスに沿った距離を表します。

## プロパティ {#section-80f266da4e2549d89f022a3f9ff4584d}

レイヤー属性。 レイヤーに`textPs=`および`textPath=` コマンドが含まれていない場合は無視されます。

*`startPos`*&#x200B;は0以上1.0未満である必要があります。 *`endPos`*&#x200B;は、開いているパスに適用する場合は&#x200B;*`startPos`*&#x200B;より大きく1.0以下、閉じているパスに適用する場合は（*`startPos`* + 1.0）以下である必要があります。

## 初期設定 {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## 関連項目 {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)、[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
