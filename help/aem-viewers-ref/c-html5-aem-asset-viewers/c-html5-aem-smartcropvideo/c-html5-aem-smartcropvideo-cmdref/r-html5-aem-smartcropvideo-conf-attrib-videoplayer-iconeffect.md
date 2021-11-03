---
title: SmartCropVideoPlayer.iconeffect
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: b283b495-ee28-4f9d-ad4d-b14ac2f9a1a2
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

スマート切り抜きビデオビューアの設定属性。

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`フェード`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> ビデオが一時停止されたときに、IconEffect がビデオの上部に表示されるようにします。 一部のデバイスでは、ネイティブのコントロールが使用されます。 この場合、 <span class="codeph"> iconeffect</span> 修飾子は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffect の表示および再表示の最大回数を指定します。 値： <span class="codeph"> -1</span> は、アイコンが無期限に再表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> フェード</span> </span> </p> </td> 
   <td colname="col2"> <p> 表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffect が自動的に非表示になるまでの表示秒数を設定します。 つまり、フェードインアニメーションの完了後、フェードアウトアニメーションの開始前の時間です。 設定 <span class="codeph"> 0</span> 自動非表示の動作を無効にします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
