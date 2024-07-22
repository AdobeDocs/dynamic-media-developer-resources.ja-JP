---
description: トンボを表示します。 トンボの表示方法を指定します。
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 18%

---

# printerMark{#printermark}

トンボを表示します。 トンボの表示方法を指定します。

` printerMark= *` トリムマーク `*, *` 裁ち落としマーク `*, *` 登録マーク `*, *` カラーバー `*, *` ページ情報 `*, *` スタイル `*, *` 線幅 `*, *` レイヤーの埋め込み `*`

異なるマークは、オフまたはオンにすることができます。 プリンタマークのスタイルも制御できます。

有効な値は次のとおりです。

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>トリムマーク= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>裁ちトンボ= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>登録記号= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>カラーバー= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ページ情報= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>初期設定 </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>デフォルトはデフォルトです </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>線幅= </p></td> 
  <td class="stentry"> <p>0.125 ～ 2.0 の範囲の任意の値（両方とも値を含む）。 </p></td> 
  <td class="stentry"> <p>初期設定は 0.25。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>レイヤーの埋め込み= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 1。 </p></td> 
 </tr> 
</table>

## 例 {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
