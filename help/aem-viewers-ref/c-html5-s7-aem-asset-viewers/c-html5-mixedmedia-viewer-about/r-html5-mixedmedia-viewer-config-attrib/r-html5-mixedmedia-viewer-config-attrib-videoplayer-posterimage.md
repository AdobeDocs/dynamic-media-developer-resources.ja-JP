---
title: VideoPlayer.posterimage
description: VideoPlayer.posterimage
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> ビデオの再生開始前の最初のフレームに表示する画像で、これを基に解決されます <span class="codeph"> serverurl</span>. URL で指定する場合は、次の情報を HTTP エンコードします。 </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>この <span class="codeph"><span class="varname"> image_id</span></span> の値を省略した場合、コンポーネントはそのアセットのデフォルトのポスター画像を代わりに使用しようとします。 </p> <p>ビデオをパスとして指定した場合、デフォルトのポスター画像カタログ ID は、ビデオパスから <span class="codeph"> catalog_id/image_id</span> ～との対 <span class="codeph"> catalog_id</span> は、パスの最初のトークンに対応します。 そして <span class="codeph"> image_id</span> は、拡張子が削除されたビデオの名前です。 その ID を持つ画像が存在しない場合、ポスター画像は表示されません。 </p> <p>初期設定のポスター画像を表示しない場合は、 <span class="codeph"> なし</span> をポスター画像の値として設定します。 この <span class="codeph"><span class="varname"> isCommands</span></span> を指定した場合、画像が表示される前に、初期設定のポスター画像にコマンドが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

なし

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
