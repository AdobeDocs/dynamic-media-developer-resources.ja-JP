---
description: メイン表示領域は、カタログ画像が表示される領域です。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。
seo-description: メイン表示領域は、カタログ画像が表示される領域です。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。
seo-title: メインビューア領域
solution: Experience Manager
title: メインビューア領域
topic: Dynamic media
uuid: 2ad21319-7a0e-44fd-8866-3055e8ff8913
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# メインビューア領域{#main-viewer-area}

メイン表示領域は、カタログ画像が表示される領域です。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer
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

例 — 白の背景(`#FFFFFF`)のビューアを設定し、サイズを512 x 288ピクセルにするには、次のように記述します。

```
.s7ecatalogsearchviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

