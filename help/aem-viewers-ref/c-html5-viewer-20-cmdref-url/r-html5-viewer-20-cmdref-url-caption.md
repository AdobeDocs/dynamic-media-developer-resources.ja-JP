---
description: すべてのビューアに共通のパラメータ。
seo-description: すべてのビューアに共通のパラメータ。
seo-title: caption
solution: Experience Manager
title: caption
topic: Dynamic media
uuid: e5a715c4-9b5b-48fc-8228-5e7416e2b71a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 6%

---


# caption{#caption}

すべてのビューアに共通のパラメータ。

>[!NOTE]
>
>このコマンドはビデオ画像ビューアには適用されません。

` caption= *`ファイル`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTTキャプションコンテンツのURLまたはパスを指定します。 画像サービングはWebVTTファイルを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 初期設定のキャプション状態を指定します。 有効は<span class="codeph"> 1 </span>です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

このビューアでは、ホストされているWebVTTファイルによるクローズドキャプションがサポートされます。 このパラメーターで指定されたキャプションは、メディアセットの最初のビデオに適用されます。後続のビデオはキャプションなしで再生されます。 キューと領域の重なりはサポートされていません。 サポートされるキュー位置の演算子：

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
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|開始|end  </span> </p> </td> 
   <td colname="col4"> <p> テキストの配置を制御します。 </p> <p>初期設定は<span class="codeph"> middle </span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>テキスト位置 </p> </td> 
   <td colname="col3"> <p> 0% ～ 100% </p> </td> 
   <td colname="col4"> <p> VideoPlayerコンポーネント内でキャプションテキストの先頭に挿入される領域の割合。 </p> <p>初期設定は<span class="codeph"> 0% </span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>行サイズ </p> </td> 
   <td colname="col3"> <p> 0% ～ 100% </p> </td> 
   <td colname="col4"> <p> キャプションに使用するビデオの幅の割合。 </p> <p>初期設定は<span class="codeph"> 100% </span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行の位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> ページ上の行の位置を決定します。 </p> <p>パーセント記号なしの整数で表した場合は、テキスト表示位置の上端からの行数になります。 </p> <p>割合（パーセント記号が最後の文字）で表した場合は、キャプションテキストは表示領域からその割合下の位置に表示されます。 </p> <p>初期設定は<span class="codeph"> 100% </span>です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTTファイルにその他のWebVTT機能が存在する場合、それらはサポートされないことに注意してください。ただし、キャプション設定は妨げられません。

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTTキャプションコンテンツへのURLまたはパスを指定します。 WebVTTファイルは、画像サービングから提供されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 初期設定のキャプション状態を指定します。 </p> <p>有効は<span class="codeph"> 1 </span>です。 </p> </td> 
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

