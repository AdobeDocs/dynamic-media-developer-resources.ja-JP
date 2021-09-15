---
title: caption
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 6%

---

# caption{#caption}

すべてのビューアに共通のパラメーター。

>[!NOTE]
>
>このコマンドは、ビデオ画像ビューアには適用されません。

` caption= *`ファイル`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTTキャプションコンテンツのURLまたはパスを指定します。 画像サービングはWebVTTファイルを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> デフォルトのキャプション状態を指定します。 <span class="codeph"> 1 </span>が有効です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

このビューアでは、ホストされているWebVTTファイルによるクローズドキャプションがサポートされます。 このパラメーターで指定されたキャプションは、メディアセットで最初に表示されるビデオに適用されます。後続のビデオはキャプションなしで再生されます。 キューおよび領域の重なりはサポートされていません。 サポートされるキュー位置の演算子：

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
   <td colname="col2"> <p>テストの整列 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end  </span> </p> </td> 
   <td colname="col4"> <p> テキストの整列を制御します。 </p> <p>初期設定は<span class="codeph">中央</span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>テキスト位置 </p> </td> 
   <td colname="col3"> <p> 0%～100% </p> </td> 
   <td colname="col4"> <p> キャプションテキストの先頭に対する、VideoPlayerコンポーネントに挿入される割合。 </p> <p>初期設定は<span class="codeph"> 0% </span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>行のサイズ </p> </td> 
   <td colname="col3"> <p> 0%～100% </p> </td> 
   <td colname="col4"> <p> キャプションに使用されるビデオの幅の割合。 </p> <p>初期設定は<span class="codeph"> 100% </span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> ページ上の行の位置を決定します。 </p> <p>パーセント記号のない整数で表した場合は、テキストが表示される上部からの行数になります。 </p> <p>割合（パーセント記号が最後の文字）で表した場合は、キャプションテキストが表示領域のその割合下に表示されます。 </p> <p>初期設定は<span class="codeph"> 100% </span>です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTTファイル内にその他のWebVTT機能が存在する場合、それらはサポートされません。しかし、キャプションを妨げることはありません。

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTTキャプションコンテンツのURLまたはパスを指定します。 WebVTTファイルは画像サービングから提供されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> デフォルトのキャプション状態を指定します。 </p> <p><span class="codeph"> 1 </span>が有効です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

（オプション）

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

なし

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
