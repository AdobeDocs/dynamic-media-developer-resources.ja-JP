---
title: caption
description: インタラクティブビデオビューア用のURLコマンド。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 8eb2aa50-52b9-4b63-9789-87e492f34a22
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 8%

---

# caption{#caption}

インタラクティブビデオビューア用のURLコマンド。

` caption= *`ファイル`*[,0|1]`

ビューアは、ホストされているWebVTTファイルを介したクローズドキャプションをサポートします。 キューおよび領域の重なりはサポートされていません。 次のキュー位置の演算子がサポートされています。

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
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>テキストの整列 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end  </span> </p> </td> 
   <td colname="col4"> <p> テキストの整列を制御します。 </p> <p>初期設定は<span class="codeph">中央</span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>テキスト位置 </p> </td> 
   <td colname="col3"> <p> 0%～100% </p> </td> 
   <td colname="col4"> <p> キャプションテキストの先頭に対する、VideoPlayerコンポーネントに挿入される割合。 </p> <p>初期設定は0%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>行のサイズ </p> </td> 
   <td colname="col3"> <p> 0%～100% </p> </td> 
   <td colname="col4"> <p> キャプションに使用されるビデオの幅の割合。 </p> <p>初期設定は100%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> ページ上の行の位置を決定します。 </p> <p>整数（パーセント記号なし）で表した場合は、テキストが表示される上部からの行数になります。 </p> <p>割合（パーセント記号が最後の文字）の場合、キャプションテキストは表示領域からその割合だけ下に表示されます。 </p> <p>初期設定は100%です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTTファイルに存在するその他のWebVTT機能はサポートされませんが、キャプション設定が中断されることはありません。

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTTキャプションコンテンツのURLまたはパスを指定します。 画像サービングによってWebVTTファイルを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> デフォルトのキャプションの状態を指定します（有効な状態は<span class="codeph"> 1 </span> ）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.caption.vtt,1
```
