---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`duration`*[, *`spacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|フェード|スライド </span> </p> </td> 
   <td colname="col2"> <p>フレーム変更時に適用する効果のタイプを指定します。 アトリビュート <span class="codeph">none はトランジション </span> ないことを表し、フレームの変更は即座に行われます。 フェード </span> のアトリビュート <span class="codeph">、古いフレームと新しいフレームの間のクロス フェードのトランジションを意味します。 スライド </span> の属性 <span class="codeph"> は、古いフレームがビューからスライドし、新しいフレームがスライドするトランジションがアクティブになります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration </span> </span> </p> </td> 
   <td colname="col2"> <p>フェード </span> またはスライド切り替え効果 <span class="codeph"> デュレーション （秒） <span class="codeph"> 指定 </span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spacing </span> </span> </p> </td> 
   <td colname="col2"> <p>スライド </span> トランジション内の隣接 <span class="codeph"> るフレーム間の間隔は、0 </span> ～ <span class="codeph"> 1 </span> の範囲 <span class="codeph"> あり、コンポーネントの幅に対して相対的です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
