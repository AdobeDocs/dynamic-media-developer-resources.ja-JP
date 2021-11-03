---
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
title: SmartCropVideoPlayer.posterimage
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c09884e2-60a1-4fce-997a-29747b4ccb7b
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

スマート切り抜きビデオビューアの設定属性。

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> ビデオの再生開始前の最初のフレームに表示する画像で、これを基に解決されます <span class="codeph"> serverurl</span>. URL で指定する場合は、次の情報を HTTP エンコードします。 </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>この <span class="codeph"><span class="varname"> image_id</span></span> の値を省略した場合、コンポーネントはそのアセットのデフォルトのポスター画像を代わりに使用しようとします。 </p> <p>ビデオをパスとして指定した場合、デフォルトのポスター画像カタログ ID は、ビデオのパスから <span class="codeph"> catalog_id/image_id</span> ～との対 <span class="codeph"> catalog_id</span> は、パスの最初のトークンに対応し、 <span class="codeph"> image_id</span> は、拡張子が削除されたビデオの名前です。 その ID を持つ画像が存在しない場合、ポスター画像は表示されません。 </p> <p>初期設定のポスター画像を表示しない場合は、 <span class="codeph"> なし</span> をポスター画像の値として設定します。 この <span class="codeph"><span class="varname"> isCommands</span></span> を指定すると、初期設定のポスター画像が表示される前に、その画像に対してコマンドが適用されます。 </p> </td> 
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
