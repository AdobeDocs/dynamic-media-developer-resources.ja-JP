---
title: caption
description: ビデオビューアの URL コマンド。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: a9af3335-ae18-4399-9014-47ec0306a087
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 5%

---

# caption{#caption}

ビデオビューアの URL コマンド。

` caption= *` ファイル `*[,0|1]`

ビューアは、ホストされた WebVTT ファイルを使用したクローズドキャプションをサポートしています。 重なり合うキューと領域はサポートされていません。 次のキュー位置指定演算子がサポートされています。

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
   <td colname="col4"> <p> テキストの配置を制御します。 </p> <p>デフォルトは中央 <span class="codeph"> す </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>テキストの位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションテキストの先頭の VideoPlayer コンポーネントへの挿入の割合。 </p> <p>デフォルトは 0% です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>ラインサイズ </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションに使用されるビデオ幅の割合。 </p> <p>デフォルトは 100% です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>行の位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> ページ上の行の位置を指定します。 </p> <p>整数（パーセント記号なし）で表される場合は、テキストが表示される位置の上からの行数になります。 </p> <p>パーセンテージ（パーセント記号は最後の文字）の場合、キャプションテキストがそのパーセントで表示領域の下方に表示されます。 </p> <p>デフォルトは 100% です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTT ファイルに存在するその他の WebVTT 機能はサポートされていませんが、キャプションを中断しないでください。

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> ファイル </span></span> </p> </td> 
   <td colname="col2"> <p> WebVTT キャプションコンテンツの URL またはパスを指定します。 ImageServing で WebVTT ファイルを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> デフォルトのキャプションの状態を指定します（有効は <span class="codeph"> 1</span>）。 </p> </td> 
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
