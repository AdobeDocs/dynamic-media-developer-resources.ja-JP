---
description: メイン表示領域は、ズーム画像とスウォッチが表示される領域です。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。
seo-description: メイン表示領域は、ズーム画像とスウォッチが表示される領域です。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。
seo-title: メインビューア領域
solution: Experience Manager
title: メインビューア領域
uuid: 689116cb-bbb9-4e26-9c16-9229330c4034
feature: Dynamic Mediaクラシック，ビューア，SDK/API，ズーム
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# メインビューア領域{#main-viewer-area}

メイン表示領域は、ズーム画像とスウォッチが表示される領域です。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

埋め込みモードで（メインビューア領域に明示的なサイズを指定した場合）操作を行うと、1つの画像で作業しているスウォッチコンポーネントの高さ分、メイン領域の高さが自動的に低下するので、スウォッチは不要です。

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7zoomviewer
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
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

