---
title: caption
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
TQID: 'https://experienceleague.adobe.com/ydZxVPE4iwQMlJLnmCFXeAzkVX2cSGiuDzeNeEi5iaU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 5%

---

# caption{#caption}

すべてのビューアに共通のパラメーター。

>[!NOTE]
>
>このコマンドは、ビデオ画像ビューアには適用されません。

` caption= *` ファイル `*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ファイル </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTT キャプションコンテンツのURLまたはパスを指定します。 画像サービングは、WebVTT ファイルを提供します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> デフォルトのキャプション状態を指定します。 有効なのは<span class="codeph"> 1 </span>です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

このビューアは、ホストされているWebVTT ファイルを使用してクローズドキャプションをサポートします。 このパラメーターで指定されたキャプションは、メディアセットの最初のビデオに適用されます。後続のビデオはキャプションなしで再生されます。 重なり合うキューとリージョンはサポートされていません。 サポートされているキューのポジショニング演算子：

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
   <td colname="col2"> <p>テスト整列 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end </span> </p> </td> 
   <td colname="col4"> <p> テキストの整列を制御します。 </p> <p>デフォルトは<span class="codeph">です（中</span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>テキストの位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションテキストの先頭のVideoPlayer コンポーネントへのインセットの割合。 </p> <p>デフォルトは<span class="codeph"> 0% </span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>行サイズ </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> キャプションに使用されるビデオ幅の割合。 </p> <p>デフォルトは<span class="codeph"> 100% </span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> ページ上の行位置を指定します。 </p> <p>パーセント記号のない整数で表される場合は、テキストが表示される上からの行数です。 </p> <p>パーセントで表されている場合 – パーセント記号は最後の文字です – キャプションテキストは表示領域のパーセントで表示されます。 </p> <p>デフォルトは<span class="codeph"> 100% </span>です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTT ファイル内に他のWebVTT機能が存在する場合は、サポートされませんが、キャプションを中断することはありません。

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ファイル </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTT キャプションコンテンツのURLまたはパスを指定します。 WebVTT ファイルは、画像サービングによって提供されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> デフォルトのキャプション状態を指定します。 </p> <p>有効なのは<span class="codeph"> 1 </span>です。 </p> </td> 
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
