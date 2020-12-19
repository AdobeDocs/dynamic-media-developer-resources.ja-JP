---
description: インタラクティブビデオビューアのURLコマンド
seo-description: インタラクティブビデオビューアのURLコマンド
seo-title: caption
solution: Experience Manager
title: caption
topic: Dynamic media
uuid: 602c8f64-e018-4916-8141-09b36003a99d
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 8%

---


# caption{#caption}

インタラクティブビデオビューアのURLコマンド

` caption= *`ファイル`*[,0|1]`

ビューアでは、ホストされているWebVTTファイルを使用したクローズドキャプションがサポートされます。 キューと領域の重なりはサポートされていません。 サポートされるキュー位置の演算子は次のとおりです。

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
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|開始|end  </span> </p> </td> 
   <td colname="col4"> <p> テキストの整列方法を制御します。 </p> <p>初期設定は<span class="codeph"> middle </span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>テキスト位置 </p> </td> 
   <td colname="col3"> <p> 0% ～ 100% </p> </td> 
   <td colname="col4"> <p> VideoPlayerコンポーネント内でキャプションテキストの先頭に挿入される領域の割合。 </p> <p>初期設定は0%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>行サイズ </p> </td> 
   <td colname="col3"> <p> 0% ～ 100% </p> </td> 
   <td colname="col4"> <p> キャプションに使用するビデオの幅の割合。 </p> <p>初期設定は100%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行の位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> ページ上の行の位置を決定します。 </p> <p>整数値（パーセント記号なし）で表した場合は、テキスト表示位置の上端からの行数になります。 </p> <p>割合（末尾の文字がパーセント記号）の場合は、キャプションテキストは表示領域からその割合だけ下の位置に表示されます。 </p> <p>初期設定は100%です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTTファイルに存在するその他のWebVTT機能はサポートされませんが、キャプション設定に影響を及ぼすことはありません。

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTTキャプションコンテンツのURLまたはパスを指定します。 画像サービングからWebVTTファイルを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 初期設定のキャプション状態を指定します（有効になっているのは<span class="codeph"> 1 </span>です）。 </p> </td> 
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

