---
description: プリンターマークを表示します。 プリンターマークの表示方法を指定します。
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
TQID: 'https://experienceleague.adobe.com/tit-a3stXGj0fZoMgi15lPIk-MtZSvUDOqlcayfNlwk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 24%

---

# printerMark{#printermark}

プリンターマークを表示します。 プリンターマークの表示方法を指定します。

` printerMark= *` トリムマーク `*, *`裁ち落としマーク `*, *` レジストレーションマーク `*, *` カラーバー`*, *` ページ情報`*, *` スタイル `*, *`線の太さ`*, *` レイヤー埋め込み`*`

様々なマークはオフまたはオンにすることができます。 プリンターマークのスタイルも制御できます。

以下は有効な値です。

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>トリムマーク= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0 です </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>裁ち落としマーク= </p></td> 
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
  <td class="stentry"> <p>ページ情報= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>初期設定は 0 です </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>初期設定 </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>Default is Default </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>線の太さ= </p></td> 
  <td class="stentry"> <p>0.125 ～ 2.0の範囲の任意の値（両方とも値を含む）。 </p></td> 
  <td class="stentry"> <p>デフォルトは0.25です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>デフォルトは1です。 </p></td> 
 </tr> 
</table>

## 例 {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
