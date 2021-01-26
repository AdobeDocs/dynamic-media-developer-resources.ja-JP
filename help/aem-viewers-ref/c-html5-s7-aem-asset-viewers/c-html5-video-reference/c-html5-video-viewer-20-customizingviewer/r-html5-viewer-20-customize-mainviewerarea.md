---
description: メイン表示領域はビデオで占められます。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。
seo-description: メイン表示領域はビデオで占められます。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。
seo-title: メインビューア領域
solution: Experience Manager
title: メインビューア領域
topic: Dynamic Media
uuid: f395b22d-55b8-4422-9aa4-9dd4b7a24063
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---


# メインビューア領域{#main-viewer-area}

メイン表示領域はビデオで占められます。 サイズが指定されていない場合、通常は使用可能なデバイス画面に収まるように設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

以下に示すCSSクラスセレクターで、表示領域の外観を制御します。

```
.s7videoviewer 
```

## メインビューア領域{#css-properties-of-the-main-viewer-area}のCSSプロパティ

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ビューアの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ビューアの高さ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 16進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

白の背景(#FFFFFF)のビデオビューアを設定し、サイズを512 x 288ピクセルにするには：

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

