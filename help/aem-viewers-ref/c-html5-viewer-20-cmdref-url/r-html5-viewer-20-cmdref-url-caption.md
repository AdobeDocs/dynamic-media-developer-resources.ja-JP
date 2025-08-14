---
title: caption
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# caption{#caption}

すべてのビューアに共通のパラメーター。

>[!NOTE]
>
>このコマンドはビデオ画像ビューアには適用されません。

` caption= *` ファイル `*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ファイル </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTT キャプションコンテンツの URL またはパスを指定します。 画像サービングは WebVTT ファイルを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> キャプションのデフォルトの状態を指定します。 有効の <span class="codeph"> は 1</span> です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

このビューアは、ホストされた WebVTT ファイルを介したクローズドキャプションをサポートしています。 このパラメーターで指定されたキャプションは、メディアセットの最初のビデオに適用され、後続のビデオはキャプションなしで再生されます。 重なり合うキューと領域はサポートされていません。 サポートされるキュー位置指定演算子：

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
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
   <td colname="col2"> <p>テストの整合性 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end </span> </p> </td> 
   <td colname="col4"> <p> テキストの配置を制御します。 </p> <p>デフォルトは中 <span class="codeph"> で </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>テキストの位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションテキストの先頭の VideoPlayer コンポーネントへの挿入の割合。 </p> <p>デフォルトは <span class="codeph">0%</span> です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>ラインサイズ </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションに使用されるビデオ幅の割合。 </p> <p>デフォルトは <span class="codeph"> 100%</span> です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行の位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> ページ上の行の位置を指定します。 </p> <p>パーセント記号を含まない整数で表された場合は、テキストが表示される位置の上からの行数になります。 </p> <p>パーセントで表した場合は、パーセント記号が最後の文字になり、そのパーセントが表示領域の下方にキャプションのテキストが表示されます。 </p> <p>デフォルトは <span class="codeph"> 100%</span> です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTT ファイル内に他の WebVTT 機能がある場合は、サポートされていません。ただし、キャプションが中断されることはありません。

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ファイル </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTT キャプションコンテンツへの URL またはパスを指定します。 WebVTT ファイルは画像サービングによって提供されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> キャプションのデフォルトの状態を指定します。 </p> <p>有効の <span class="codeph"> は 1</span> です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

オプション。

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

なし

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
