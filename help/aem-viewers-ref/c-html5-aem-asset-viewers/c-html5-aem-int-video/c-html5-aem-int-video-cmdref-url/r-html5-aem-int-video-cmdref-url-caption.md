---
description: インタラクティブビデオビューアのURLコマンド。
seo-description: インタラクティブビデオビューアのURLコマンド。
seo-title: キャプション
solution: Experience Manager
title: キャプション
topic: Dynamic media
uuid: 602c8f64-e018-4916-8141-09b36003a99d
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# caption{#caption}

インタラクティブビデオビューアのURLコマンド。

` caption= *`ファイル`*[,0|1]`

Viewerは、ホストされているWebVTTファイルを使用したクローズドキャプションをサポートします。 キューと領域の重なりはサポートされていません。 次のキュー位置演算子がサポートされています。

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
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end </span> </p> </td> 
   <td colname="col4"> <p> テキストの整列を制御します。 </p> <p>初期設定は <span class="codeph"> middleで </span>す。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>テキスト位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションテキストの先頭に対するVideoPlayerコンポーネントへのインセットの割合。 </p> <p>初期設定は0%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>行サイズ </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションに使用するビデオの幅の割合。 </p> <p>初期設定は100%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> ページ上の行の位置を指定します。 </p> <p>整数（パーセント記号なし）で表した場合は、テキストが表示される上端からの行数です。 </p> <p>パーセント値（最後の文字がパーセント記号）の場合、キャプションテキストは表示領域からその割合だけ下に表示されます。 </p> <p>初期設定は100%です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTTファイルに存在するその他のWebVTT機能はサポートされていませんが、キャプションが妨げられることはありません。

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ファイ </span> ル </span> </p> </td> 
   <td colname="col2"> <p> WebVTTキャプションコンテンツのURLまたはパスを指定します。 画像サービングでWebVTTファイルを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> デフォルトのキャプション状態を指定します(有効 <span class="codeph"> な場合は1 </span>)。 </p> </td> 
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

