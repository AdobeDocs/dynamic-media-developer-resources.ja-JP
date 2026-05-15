---
title: VideoPlayer.posterimage
description: VideoPlayer.posterimage
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
TQID: 'https://experienceleague.adobe.com/DAvANJggSrj6-wEEL8qYAMlOeuavo7usySKl1g-npVg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> ビデオの再生を開始する前の最初のフレームに表示する画像は、<span class="codeph"> serverurl</span>に対して解決されました。 URLで指定した場合は、次のHTTP エンコードを行います。 </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> <span class="codeph"> %3F</span>として </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p><span class="codeph"><span class="varname"> image_id</span></span>値が省略された場合、コンポーネントはそのアセットにデフォルトのポスター画像を代わりに使用しようとします。 </p> <p>ビデオがパスとして指定されている場合、デフォルトのポスター画像カタログ IDは、<span class="codeph"> catalog_id/image_id</span> ペアとしてビデオパスから派生します。このペアでは、<span class="codeph"> catalog_id</span>がパス内の最初のトークンに対応します。 また、<span class="codeph"> image_id</span>は、拡張子が削除されたビデオの名前です。 このIDの画像が存在しない場合、ポスター画像は表示されません。 </p> <p>デフォルトのポスター画像が表示されないようにするには、ポスター画像の値として<span class="codeph"> none</span>を指定します。 <span class="codeph"><span class="varname"> isCommands</span></span>のみが指定されている場合、画像が表示される前に、コマンドがデフォルトのポスター画像に適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

なし

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
