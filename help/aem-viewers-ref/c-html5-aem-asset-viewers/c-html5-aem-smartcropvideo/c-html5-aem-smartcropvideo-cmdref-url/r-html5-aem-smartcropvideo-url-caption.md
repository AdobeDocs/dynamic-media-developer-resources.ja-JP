---
title: caption
description: スマート切り抜きビデオビューアのURL コマンド。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0d7000d0-9181-4c6e-a94e-31ab5ad17fa4
TQID: 'https://experienceleague.adobe.com/yh1XHiqp8t6dB8AjQ769yMSBs0ew5x5dERv-8buuZ4k'
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
source-wordcount: '209'
ht-degree: 8%
---
# caption{#caption}

スマート切り抜きビデオビューアのURL コマンド。

` caption= *` ファイル `*[,0|1]`

ビューアは、ホストされたWebVTT ファイルを使用したクローズドキャプションをサポートしています。 重なり合うキューとリージョンはサポートされていません。 サポートされるキューのポジショニングオペレーターには次のものがあります。

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>キー </p> </th> 
   <th colname="col2" class="entry"> <p>名前 </p> </th> 
   <th colname="col3" class="entry"> <p>値 </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>テキスト整列 </p> </td> 
   <td colname="col3"> <p><span class="codeph"> left|right|middle|start|end</span> </p> </td> 
   <td colname="col4"> <p> テキストの整列を制御します。 </p> <p>デフォルトは<span class="codeph"> middle</span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>テキストの位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションテキストの先頭のVideoPlayer コンポーネントへのインセットの割合。 </p> <p>デフォルトは0%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>行サイズ </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションに使用されるビデオ幅の割合。 </p> <p>デフォルトは100%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> ページ上の行位置を指定します。 </p> <p>整数（パーセント記号なし）で表される場合は、テキストが表示される上からの行数です。 </p> <p>パーセント値（パーセント記号は最後の文字）の場合、キャプションテキストは表示領域のパーセント単位で表示されます。 </p> <p>デフォルトは100%です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTT ファイルに存在するその他のWebVTT機能はサポートされていませんが、キャプションを中断しないでください。

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> ファイル </span></span> </p> </td> 
   <td colname="col2"> <p> WebVTT キャプションコンテンツのURLまたはパスを指定します。 ImageServingでWebVTT ファイルを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> デフォルトのキャプション状態を指定します（有効なのは<span class="codeph"> 1</span>）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
