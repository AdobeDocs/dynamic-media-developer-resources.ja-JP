---
description: プリンタマークを表示します。 プリンタマークの表示方法を指定します。
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 30%

---


# printerMark{#printermark}

プリンタマークを表示します。 プリンタマークの表示方法を指定します。

` printerMark= *`trim `*, *`marksbleed `*, *`marksregistration `*, *`markscolor `*, *`barspage `*, *``*, *`informationstyleline `*, *`weightlayer embed`*`

異なるマークは、オフまたはオンにすることができます。 プリンタマークのスタイルも制御できます。

有効な値は次のとおりです。

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>trim marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0 です </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>bleed marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0 です </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>registration marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0 です </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>color bars= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0 です </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page information= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0 です </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>初期設定 </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>初期設定はDefaultです。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>行重み付け= </p></td> 
  <td class="stentry"> <p>0.125 ～ 2.0の範囲の任意の値。両方の値を含みます。 </p></td> 
  <td class="stentry"> <p>初期設定は 0.25 です </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 1 です </p></td> 
 </tr> 
</table>

## 例 {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
