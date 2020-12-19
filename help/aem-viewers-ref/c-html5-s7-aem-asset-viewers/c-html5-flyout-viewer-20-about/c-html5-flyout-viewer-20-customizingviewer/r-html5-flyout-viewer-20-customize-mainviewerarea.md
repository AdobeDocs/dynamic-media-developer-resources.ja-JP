---
description: メイン表示領域は、フライアウト表示とスウォッチが表示される領域です。
seo-description: メイン表示領域は、フライアウト表示とスウォッチが表示される領域です。
seo-title: メインビューア領域
solution: Experience Manager
title: メインビューア領域
topic: Dynamic media
uuid: bc0beeaf-3e7d-4ede-9a7d-04afb1724e44
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 2%

---


# メインビューア領域{#main-viewer-area}

メイン表示領域は、フライアウト表示とスウォッチが表示される領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7flyoutviewer
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ビューアの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ビューアの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 白の背景(`#FFFFFF`)のフライアウトビューアを設定し、サイズを260 x 500ピクセルにするには、次のように記述します。

```
.s7flyoutviewer { 
 background-color: #FFFFFF; 
 width: 260px; 
 height: 500px;  
}
```

