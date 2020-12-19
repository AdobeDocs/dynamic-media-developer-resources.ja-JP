---
description: ビデオビューアの設定属性。
seo-description: ビデオビューアの設定属性。
seo-title: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
topic: Dynamic media
uuid: 59d81a72-ac17-4c32-ab47-89bd14dc17a5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

ビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 再生中のビデオ開始の前の最初のフレームに表示する画像です。<span class="codeph"> serverurl</span>を基準に解決されます。 URLで指定する場合、次の内容をHTTPエンコードします。 </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> % <span class="codeph"> 3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p><span class="codeph"><span class="varname"> image_id</span></span>の値を省略すると、コンポーネントは、そのアセットの初期設定のポスター画像を代わりに使用しようとします。 </p> <p>ビデオをパスとして指定した場合、初期設定のポスター画像カタログIDは、ビデオパスから<span class="codeph">カタログID/画像ID</span>ペアに派生します。<span class="codeph">カタログID</span>はパス内の最初のトークンに対応し、<span class="codeph">画像_id</span>は拡張子が削除されたビデオの名前です。 そのIDの画像が存在しない場合、ポスター画像は表示されません。 </p> <p>初期設定のポスター画像が表示されないようにするには、ポスター画像の値として<span class="codeph"> none</span>を指定します。 <span class="codeph"><span class="varname"> isCommands</span></span>のみを指定した場合、画像が表示される前に、初期設定のポスター画像にコマンドが適用されます。 </p> </td> 
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

