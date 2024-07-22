---
title: VideoPlayer.posterimage
description: ビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c09884e2-60a1-4fce-997a-29747b4ccb7b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

ビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> ビデオの再生を開始する前の最初のフレームに表示される画像。serverurl</span> で解決 <span class="codeph"> れます。 URL で指定されている場合は、次の内容が HTTP エンコードされます。 </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph">?</span> as <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p><span class="codeph"><span class="varname"> image_id</span></span> の値が省略された場合、コンポーネントはそのアセットに対してデフォルトのポスター画像を代わりに使用しようとします。 </p> <p>ビデオをパスとして指定すると、デフォルトのポスター画像カタログ ID は、<span class="codeph"> catalog_id/image_id</span> のペアとしてビデオパスから取得されます。ここで <span class="codeph"> catalog_id</span> は、パスの最初のトークンに対応します。 また、image_id</span><span class="codeph">、拡張子が削除されたビデオの名前です。 その ID の画像が存在しない場合は、ポスター画像は表示されません。 </p> <p>デフォルトのポスター画像が表示されないようにするには、「なし」 <span class="codeph"> ポスター画像値 </span> して指定します。 <span class="codeph"><span class="varname"> isCommands</span></span> のみが指定されている場合、コマンドは画像が表示される前にデフォルトのポスター画像に適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
