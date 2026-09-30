---
title: SmartCropVideoPlayer.iconeffect
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 369e389c-f0e2-405e-b4aa-2f6b9ac8b8ea
TQID: 'https://experienceleague.adobe.com/xgBGHFv7Zssfc7tbONV97-Tsbvl-Jn5y2oUU8X26dBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%
---
# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

スマート切り抜きビデオビューアの設定属性。

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`個のカウント `*][, *`個のフェード `*][, *`個の自動非表示`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> ビデオを一時停止したときに、IconEffectをビデオの上に表示できるようにします。 一部のデバイスでは、ネイティブコントロールが使用されています。 このような場合、<span class="codeph"> iconeffect</span>修飾子は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> カウント </span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffectが表示され、再表示される最大回数を指定します。 値<span class="codeph"> -1</span>は、アイコンが無期限に再表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> フェード </span> </span> </p> </td> 
   <td colname="col2"> <p> アニメーションを表示または非表示にする時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffectが自動的に非表示になるまでの表示時間を秒単位で設定します。 つまり、フェードインアニメーションが完了してからフェードアウトアニメーションが開始されるまでの時間です。 <span class="codeph"> 0</span>を設定すると、自動非表示の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
