---
description: ビデオビューアの設定属性。
solution: Experience Manager
title: VideoPlayer.posterimage
feature: Dynamic Media Classic，ビューア，SDK/API，ビデオ
role: Developer,Business Practitioner
exl-id: c09884e2-60a1-4fce-997a-29747b4ccb7b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

ビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> ビデオの再生開始前に最初のフレームに表示する画像を指定します。この画像は<span class="codeph"> serverurl</span>に対して解決されます。 URLで指定する場合、次の内容をHTTPエンコードします。 </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> % <span class="codeph"> 3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> は% <span class="codeph"> 3D</span> </p> </li> 
     </ul> </p> <p><span class="codeph"><span class="varname"> image_id</span></span>の値を省略すると、コンポーネントはそのアセットのデフォルトのポスター画像を代わりに使用しようとします。 </p> <p>ビデオをパスとして指定した場合、デフォルトのポスター画像カタログIDは、ビデオパスから<span class="codeph"> catalog_id/image_id</span>のペアに導き出されます。<span class="codeph"> catalog_id</span>はパスの最初のトークン、<span class="codeph"> image_id</span>は拡張子が削除されたビデオの名前です。 そのIDを持つ画像が存在しない場合、ポスター画像は表示されません。 </p> <p>初期設定のポスター画像が表示されないようにするには、ポスター画像の値に<span class="codeph"> none</span>を指定します。 <span class="codeph"><span class="varname"> isCommands</span></span>のみを指定した場合は、画像が表示される前に、コマンドがデフォルトのポスター画像に適用されます。 </p> </td> 
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
