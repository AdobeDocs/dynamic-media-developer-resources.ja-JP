---
description: メインビュー領域は、スマート切り抜きビデオで占められます。 通常、サイズが指定されていない場合は、使用可能なデバイス画面に収まるようにが設定されます。
solution: Experience Manager
title: メインビューア領域
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 7d1379c1-7746-4f61-92df-e8ac4ab7d506
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---

# メインビューア領域{#main-viewer-area}

メインビュー領域はビデオで占められます。 通常、サイズが指定されていない場合は、使用可能なデバイス画面に収まるようにが設定されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

以下に示す CSS クラスセレクターで、表示領域の外観を制御します。

```
.s7smartcropvideoviewer 
```

## メインビューア領域の CSS プロパティ {#css-properties-of-the-main-viewer-area}

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 16 進数形式の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

白の背景 (#FFFFFF) を持つスマート切り抜きビデオビューアを設定し、サイズを 512 x 288 ピクセルにするには：

```
.s7smartcropvideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
