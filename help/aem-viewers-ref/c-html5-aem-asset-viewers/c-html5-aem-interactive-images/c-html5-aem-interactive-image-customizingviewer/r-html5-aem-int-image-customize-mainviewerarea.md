---
description: メインビュー領域は、ズーム画像が表示される領域です。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。
seo-description: メインビュー領域は、ズーム画像が表示される領域です。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。
seo-title: メインビューア領域
solution: Experience Manager
title: メインビューア領域
topic: Dynamic media
uuid: 666328fe-1819-43a6-a2c2-ba63ac798700
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# メインビューア領域{#main-viewer-area}

メインビュー領域は、ズーム画像が表示される領域です。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactiveimage
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 白の背景( `#FFFFFF`)を持つビューアを設定し、サイズを1174 x 500ピクセルにします。

```
.s7interactiveimage { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```

