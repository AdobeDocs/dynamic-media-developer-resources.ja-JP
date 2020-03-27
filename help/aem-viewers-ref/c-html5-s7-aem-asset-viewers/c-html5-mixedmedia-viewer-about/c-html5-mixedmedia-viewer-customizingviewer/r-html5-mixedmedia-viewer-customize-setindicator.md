---
description: 設定インジケーターは、タッチデバイスでビューアを使用した場合に、メインスウォッチの上にレンダリングされる一連のドットです。 このドットは、スクロールボタンが使用できない場合に、サムネールのページ間を移動するのに役立ちます。
seo-description: 設定インジケーターは、タッチデバイスでビューアを使用した場合に、メインスウォッチの上にレンダリングされる一連のドットです。 このドットは、スクロールボタンが使用できない場合に、サムネールのページ間を移動するのに役立ちます。
seo-title: インジケータの設定
solution: Experience Manager
title: インジケータの設定
topic: Dynamic media
uuid: e62fac7c-28b6-40bf-83cc-8bcfbaa0dfa3
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# インジケータの設定{#set-indicator}

設定インジケーターは、タッチデバイスでビューアを使用した場合に、メインスウォッチの上にレンダリングされる一連のドットです。 このドットは、スクロールボタンが使用できない場合に、サムネールのページ間を移動するのに役立ちます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**設定インジケーターのCSSプロパティ**

設定インジケーターコンテナの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7setindicator
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>設定インジケーターの16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 白の背景を持つインジケーターを設定するには、次のように記述します。

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

個々の設定インジケーターのドットの外観は、CSSクラスセレクターを使用して制御します。

`.s7mixedmediaviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>設定インジケーターのドットの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>設定インジケーターのドットの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>左余白（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>上余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>右余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom </span> </p> </td> 
   <td colname="col2"> <p>下余白（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>境界線の半径（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>設定インジケーターのドットでは、属 `state` 性セレクターがサポートされます。このセレクターは、サムネールの状態ごとに異なるスキンを適用するのに使用できます。 特に、はサムネ `state="selected"` ールの現在のページに対応し、はデフォ `state="unselected"` ルトのドットの状態に対応します。

例 — 15 x 15ピクセルで、2ピクセルの水平マージン、5ピクセルの上マージン、1ピクセルの下マージン、12ピクセルの半径、#D5D3D3の初期設定の色および#939393アクティブカラーを設定するには、次のように記述します。

```
.s7mixedmediaviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7mixedmediaviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```

