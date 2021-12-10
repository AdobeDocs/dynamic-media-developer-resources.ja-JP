---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`duration`*[, *`間隔`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide </span> </p> </td> 
   <td colname="col2"> <p>フレームの変更に適用する効果のタイプを指定します。 属性 <span class="codeph"> なし </span> は、何の移行も行わないことを意味します。フレームの変更がすぐに発生します。 属性 <span class="codeph"> フェード </span> は、前のフレームと新しいフレームの間のクロスフェードトランジションを意味します。 属性 <span class="codeph"> スライド </span> 前のフレームがビューからスライドアウトし、新しいフレームがスライドインするトランジションをアクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration </span> </span> </p> </td> 
   <td colname="col2"> <p>次の期間（秒）を指定します。 <span class="codeph"> フェード </span> または <span class="codeph"> スライド </span> 遷移効果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 間隔 </span> </span> </p> </td> 
   <td colname="col2"> <p>内の隣接するフレーム間の間隔 <span class="codeph"> スライド </span> トランジションの範囲は <span class="codeph"> 0 </span> 経由 <span class="codeph"> 1 </span> とは、コンポーネントの幅を基準とした相対パスです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
