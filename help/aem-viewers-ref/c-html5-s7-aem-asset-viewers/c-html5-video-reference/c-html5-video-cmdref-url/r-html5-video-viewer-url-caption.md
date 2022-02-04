---
title: caption
description: ビデオビューアの URL コマンド。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: a9af3335-ae18-4399-9014-47ec0306a087
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 9%

---

# caption{#caption}

ビデオビューアの URL コマンド。

` caption= *`ファイル`*[,0|1]`

ビューアは、ホストされている WebVTT ファイルによるクローズドキャプションをサポートしています。 キューおよび領域の重複はサポートされていません。 次のキュー位置指定演算子がサポートされます。

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
   <td colname="col4"> <p> テキストの整列を制御します。 </p> <p>デフォルトはです。 <span class="codeph"> 中</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>テキスト位置 </p> </td> 
   <td colname="col3"> <p> 0% ～ 100% </p> </td> 
   <td colname="col4"> <p> キャプションテキストの先頭に対する、VideoPlayer コンポーネントへのインセットの割合。 </p> <p>初期設定は 0%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>行のサイズ </p> </td> 
   <td colname="col3"> <p> 0% ～ 100% </p> </td> 
   <td colname="col4"> <p> キャプションに使用するビデオの幅の割合。 </p> <p>初期設定は 100%です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>行の位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> ページ上の行の位置を決定します。 </p> <p>整数（パーセント記号なし）で表した場合、テキストが表示される上からの行数になります。 </p> <p>割合（パーセント記号が最後の文字）の場合、キャプションテキストは表示領域のその割合まで下に表示されます。 </p> <p>初期設定は 100%です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTT ファイルに存在するその他の WebVTT 機能はサポートされませんが、キャプションを中断しないでください。

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> ファイル</span></span> </p> </td> 
   <td colname="col2"> <p> WebVTT キャプションコンテンツの URL またはパスを指定します。 ImageServing によって WebVTT ファイルを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 初期設定のキャプションの状態を指定します ( 有効にすると <span class="codeph"> 1</span>) をクリックします。 </p> </td> 
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
