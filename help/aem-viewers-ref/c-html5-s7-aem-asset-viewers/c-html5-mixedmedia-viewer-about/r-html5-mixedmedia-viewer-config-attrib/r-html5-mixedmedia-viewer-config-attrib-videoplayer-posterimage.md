---
description: 'null'
seo-description: 'null'
seo-title: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
topic: Dynamic media
uuid: 28663f44-11cb-4522-bd12-d6bec17b4173
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> ビデオの再生開始前に最初のフレームに表示する画像で、serverurlを基準に解決さ <span class="codeph"> れます</span>。 URLで指定する場合は、次をHTTPエンコードします。 </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> % <span class="codeph"> 3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> %</span> 26と <span class="codeph"> して(&amp;A)</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>image_idの値を <span class="codeph"><span class="varname"> 省略すると</span></span> 、コンポーネントはそのアセットの初期設定のポスター画像を使用しようとします。 </p> <p>ビデオをパスとして指定すると、初期設定のポスター画像カタログIDは、ビデオパスから <span class="codeph"> catalog_id/image_id</span> ( <span class="codeph"></span><span class="codeph"></span> catalog_idはパス内の最初のトークンに対応し、image_idは拡張子が削除されたビデオの名前)になります。 そのIDの画像が存在しない場合、ポスター画像は表示されません。 </p> <p>初期設定のポスター画像が表示されないようにするには、ポスター画像の <span class="codeph"> 値に</span> 「なし」を指定します。 isCommandsのみを指定し <span class="codeph"><span class="varname"> た場合</span></span> 、画像が表示される前に、初期設定のポスター画像にコマンドが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

なし

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
