---
description: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 5%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *``*[, *`durationspacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide  </span> </p> </td> 
   <td colname="col2"> <p>フレームの変更時に適用する効果のタイプを指定します。 <span class="codeph"> none </span> は、トランジションなしを表します。フレームの変更は即座に行われます。<span class="codeph"> fadeは、前のフ </span> レームと次のフレームの間にクロスフェードのトランジションを設定します。<span class="codeph"> slideは、 </span> 前のフレームがビューからスライドアウトし、新しいフレームがスライドインするトランジションをアクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">フェード</span>または<span class="codeph">スライド</span>のトランジション効果の時間（秒単位）を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spacing  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">スライド</span>トランジション内の隣接するフレーム間の間隔は、<span class="codeph"> 0 </span>と<span class="codeph"> 1 </span>の間の範囲で、コンポーネントの幅を基準にした値です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
