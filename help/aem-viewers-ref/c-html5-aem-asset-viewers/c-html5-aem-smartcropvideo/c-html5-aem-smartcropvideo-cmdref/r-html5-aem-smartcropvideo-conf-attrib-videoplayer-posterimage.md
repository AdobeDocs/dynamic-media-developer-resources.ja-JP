---
title: SmartCropVideoPlayer.posterimage
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ff4f8e2c-b9c3-4fba-b3f0-fa1eaddcd8c0
TQID: 'https://experienceleague.adobe.com/tTBGmii-taSeo6W1AZ9CtgEpW6jFObLUTLsNiYgvOrA'
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
source-wordcount: '177'
ht-degree: 4%
---
# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

スマート切り抜きビデオビューアの設定属性。

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>]&#x200B;[?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> ビデオの再生を開始する前の最初のフレームに表示する画像は、<span class="codeph"> serverurl</span>に対して解決されました。 URLで指定した場合は、次のHTTP エンコードを行います。 </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> <span class="codeph"> %3F</span>として </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p><span class="codeph"><span class="varname"> image_id</span></span>値が省略された場合、コンポーネントはそのアセットにデフォルトのポスター画像を代わりに使用しようとします。 </p> <p>ビデオがパスとして指定されている場合、デフォルトのポスター画像カタログ IDは、ビデオパスから<span class="codeph"> catalog_id/image_id</span> ペアとして派生します。 <span class="codeph"> catalog_id</span>はパスの最初のトークンに対応し、<span class="codeph"> image_id</span>は拡張子が削除されたビデオの名前です。 このIDの画像が存在しない場合、ポスター画像は表示されません。 </p> <p>デフォルトのポスター画像が表示されないようにするには、ポスター画像の値として<span class="codeph"> none</span>を指定します。 <span class="codeph"><span class="varname"> isCommands</span></span>のみが指定されている場合、画像が表示される前に、コマンドがデフォルトのポスター画像に適用されます。 </p> </td> 
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
