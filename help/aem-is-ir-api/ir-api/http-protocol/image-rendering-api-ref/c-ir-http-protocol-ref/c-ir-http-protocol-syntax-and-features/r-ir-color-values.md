---
title: カラー値
description: color=属性と bgc=属性のカラー値は、10 進数のコンポーネント値のリスト、コンマ区切りのコンポーネント値、またはHTMLと同様の 16 進表記を使用して指定できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 608ff0f1-4fbd-4e32-af07-3a62569d14c7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---

# カラー値{#color-values}

`color=` 属性と `bgc=` 属性のカラー値は、10 進数のコンポーネント値のリスト、コンマ区切りのコンポーネント値、またはHTMLと同様の 16 進表記を使用して指定できます。

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 色 </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{ {red , green , blue} |灰色 } | { [ 0x ] hex6 } | { 0xhex2 }</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i> 赤、緑、青、灰色 </i> </p></td> 
  <td class="stentry"> <p>カラーコンポーネント値（0...255、10 進数の整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex6</i> </p></td> 
  <td class="stentry"> <p>6 桁の 16 進数のRGB カラー値（RRGGBB）をパックしました。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex2</i> </p></td> 
  <td class="stentry"> <p>パックされた 2 桁の 16 進数の灰色の値（0...FF）。 </p></td> 
 </tr> 
</table>

## 例 {#section-a78732151d584e84abeb99f9ce8d7c24}

有効な色指定子と、それに対応するRGBの色の値の解釈の例を次に示します。

<table id="simpletable_837B3173020240A5B7B2DB2F4CC57352"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,100,200 </p></td> 
  <td class="stentry"> <p>（0,100,200） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>128 </p></td> 
  <td class="stentry"> <p>（128,128,128） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0x010203 </p></td> 
  <td class="stentry"> <p>（1,2,3） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>00b1c2 </p></td> 
  <td class="stentry"> <p>（160,177,194） </p></td> 
 </tr> 
</table>

## 関連項目 {#section-207d5cb918a94736a27445faa58917d3}

[color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa), [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0), [grout=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
