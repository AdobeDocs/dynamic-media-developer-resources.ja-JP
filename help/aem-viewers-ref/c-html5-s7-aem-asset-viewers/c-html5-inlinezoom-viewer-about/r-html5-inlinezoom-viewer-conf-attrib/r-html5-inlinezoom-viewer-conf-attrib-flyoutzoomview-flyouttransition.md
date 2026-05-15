---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 3199d4a3-4799-40a2-b0a5-0e1ee4744fbe
TQID: 'https://experienceleague.adobe.com/FOK4Eoi3n-7LWZeJwciRFfkPTTnsrF-v-XI7APHiQIs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`showtime`*[, *`showdelay`*[, *`hidetime`*[, *`hidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|スライド|フェード </span> </span> </p> </td> 
   <td colname="col2"> <p> フライアウトビューを表示または非表示にするときに適用されるエフェクトのタイプを指定します。 <span class="codeph"> none </span>を指定すると、フライアウト画像はアクティブ化されて準備ができたときに即座に表示されます。<span class="codeph"> スライド </span>は、スライドアニメーションを左右方向に再生します。<span class="codeph"> フェード </span>は、フライアウト画像にアルファ遷移を適用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ショータイム </span> </span> </p> </td> 
   <td colname="col2"> <p> ショーのアニメーションが完了するまでの秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span> </span> </p> </td> 
   <td colname="col2"> <p> 表示アニメーションを開始するユーザーのアクションと、表示アニメーション自体の開始との間の遅延時間（秒単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">非表示</span> </span> </p> </td> 
   <td colname="col2"> <p> 非表示アニメーションが完了するまでの秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay </span> </span> </p> </td> 
   <td colname="col2"> <p> 非表示アニメーションを開始するユーザーアクションと、非表示アニメーション自体の開始との間の遅延時間（秒単位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

オプション。

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
