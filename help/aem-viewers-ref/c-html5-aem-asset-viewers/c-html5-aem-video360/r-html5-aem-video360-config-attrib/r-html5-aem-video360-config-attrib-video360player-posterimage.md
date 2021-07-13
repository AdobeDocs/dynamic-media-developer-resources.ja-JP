---
description: ビデオ360ビューアの設定属性。
solution: Experience Manager
title: Video360Player.posterimage
feature: Dynamic Media Classic，ビューア，SDK/API,360 VRビデオ
role: Developer,User
exl-id: fffd0976-0aeb-4e61-981f-b84e9076f35f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 12%

---

# Video360Player.posterimage{#video-player-posterimage}

ビデオ360ビューアの設定属性。

` [Video360Player.|<containerId>_video360Player.]posterimage=none|[? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> ポスター画像の外観を制御する画像サービング修飾子 URLで指定する場合、次の内容をHTTPエンコードします。 </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> % <span class="codeph"> 3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> は% <span class="codeph"> 3D</span> </p> </li> 
     </ul> </p> <p> この修飾子は、Dynamic Media ClassicまたはAEM Dynamic Mediaでホストされるビデオコンテンツに対して機能します。 </p> <p>初期設定のポスター画像が表示されないようにするには、ポスター画像の値に<span class="codeph"> none</span>を指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
