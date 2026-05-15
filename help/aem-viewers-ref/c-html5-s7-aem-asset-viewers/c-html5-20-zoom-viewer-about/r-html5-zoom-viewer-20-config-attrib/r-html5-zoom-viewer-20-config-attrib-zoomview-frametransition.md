---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
TQID: 'https://experienceleague.adobe.com/bnR4MQtKYsqMEDEyJN2iFpJNLMWcsc-s9mK4XQW5qpE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 4%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`期間`*[, *`間隔`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|フェード|スライド </span> </p> </td> 
   <td colname="col2"> <p>フレーム変更に適用されるエフェクトのタイプを指定します。 属性<span class="codeph"> none </span>は遷移を表しません。フレームの変更は即座に行われます。 属性<span class="codeph"> フェード </span>は、古いフレームと新しいフレームの間のクロスフェード移行を意味します。 属性<span class="codeph"> スライド </span>は、古いフレームがビューからスライドし、新しいフレームがスライドするトランジションをアクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">期間</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> フェード </span>または<span class="codeph"> スライド </span>のトランジション エフェクトのデュレーション （秒）を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">の間隔</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> スライド </span>のトランジションの隣接するフレーム間の間隔は、<span class="codeph"> 0 </span> ～ <span class="codeph"> 1 </span>の範囲で、コンポーネントの幅に対して相対的です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
