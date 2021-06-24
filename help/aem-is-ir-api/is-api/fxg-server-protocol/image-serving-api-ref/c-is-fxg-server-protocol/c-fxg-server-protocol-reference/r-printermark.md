---
description: プリンタマークを表示します。 印刷マークの表示方法を指定します。
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 31%

---

# printerMark{#printermark}

プリンタマークを表示します。 印刷マークの表示方法を指定します。

` printerMark= *`trim marksbleed `*, *`marksregistration markscolor barspage `*, *`informationstyleline `*, *`weightlayer埋め`*, *``*, *``*, *``*, *`込み`*`

異なるマークのオフ/オンを切り替えることができます。 印刷マークのスタイルも制御できます。

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
  <td class="stentry"> <p>デフォルトはDefaultです。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>線の太さ= </p></td> 
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
