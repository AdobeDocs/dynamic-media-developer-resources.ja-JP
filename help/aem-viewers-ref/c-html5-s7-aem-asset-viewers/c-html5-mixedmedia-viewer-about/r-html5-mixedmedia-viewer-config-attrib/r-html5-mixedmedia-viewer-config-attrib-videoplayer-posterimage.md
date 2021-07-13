---
description: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,User
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
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

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

なし

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
