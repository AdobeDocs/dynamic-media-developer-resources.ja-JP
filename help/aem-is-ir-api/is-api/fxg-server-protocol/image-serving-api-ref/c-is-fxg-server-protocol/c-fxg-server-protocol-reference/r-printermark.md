---
description: プリンタマークを表示します。 プリンタマークの表示方法を指定します。
seo-description: プリンタマークを表示します。 プリンタマークの表示方法を指定します。
seo-title: printerMark
solution: Experience Manager
title: printerMark
topic: Scene7 Image Serving - Image Rendering API
uuid: 3e5699ce-3ccd-4f85-91dd-c40c252a758d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# printerMark{#printermark}

プリンタマークを表示します。 プリンタマークの表示方法を指定します。

` printerMark= *`trim marksbleed`*, *`marksregistration markscolor`*, *`barspage`*, *`informationstyleline`*, *`weightlayer埋め込`*, *``*, *``*, *`みマーク`*`

異なるマークのオフ/オンを切り替えることができます。 プリンタマークのスタイルも制御できます。

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
  <td class="stentry"> <p>デフォルトはDefault </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>線の太さ= </p></td> 
  <td class="stentry"> <p>0.125 ～ 2.0の範囲の任意の値（両方の値を含む）。 </p></td> 
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
