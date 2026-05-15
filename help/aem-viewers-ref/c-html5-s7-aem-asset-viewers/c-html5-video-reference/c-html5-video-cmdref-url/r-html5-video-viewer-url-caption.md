---
title: caption
description: ビデオビューアのURL コマンド。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: a9af3335-ae18-4399-9014-47ec0306a087
TQID: 'https://experienceleague.adobe.com/OEXxm0r9wv92FTzfKdjUwfhhcXLaZ5jMkvVbvvAVQpY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 205
ht-degree: 8%

---

# caption{#caption}

ビデオビューアのURL コマンド。

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
