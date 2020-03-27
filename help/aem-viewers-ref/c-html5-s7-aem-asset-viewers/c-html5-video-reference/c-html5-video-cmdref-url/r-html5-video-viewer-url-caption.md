---
description: ビデオビューアのURLコマンド。
seo-description: ビデオビューアのURLコマンド。
seo-title: キャプション
solution: Experience Manager
title: キャプション
topic: Dynamic media
uuid: 670d83c2-bfc5-411a-8581-5103a62aa8cf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# caption{#caption}

ビデオビューアのURLコマンド。

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
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>テキストの整列 </p> </td> 
   <td colname="col3"> <p><span class="codeph"> left|right|middle|start|end</span> </p> </td> 
   <td colname="col4"> <p> テキストの整列を制御します。 </p> <p>初期設定は <span class="codeph"> middleです</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>テキスト位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションテキストの先頭に対するVideoPlayerコンポーネントへのインセットの割合。 </p> <p>初期設定は0%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>行サイズ </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションに使用するビデオの幅の割合。 </p> <p>初期設定は100%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
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
   <td colname="col1"> <p><span class="codeph"><span class="varname"> ファイル</span></span> </p> </td> 
   <td colname="col2"> <p> WebVTTキャプションコンテンツのURLまたはパスを指定します。 ImageServingでWebVTTファイルを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> デフォルトのキャプション状態を指定します(有効な場合は1 <span class="codeph"></span>)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```

