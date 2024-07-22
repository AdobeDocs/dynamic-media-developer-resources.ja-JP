---
title: コントロールバー
description: コントロールバーは、再生/一時停止ボタンや音量コントロールなど、ビデオビューアで使用できるすべての UI コントロールの背後にある、を含む長方形領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2239307a-4a05-4392-b35c-a64ea6c938ad
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# コントロールバー{#control-bar}

コントロールバーは、再生/一時停止ボタンや音量コントロールなど、ビデオビューアで使用できるすべての UI コントロールの背後にある、を含む長方形領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは常に、使用可能なビューアの幅全体を取ります。 色、高さ、垂直方向の位置を、ビデオビューアコンテナに対して CSS で変更できます。

次の CSS クラスセレクターで、コントロールバーの外観を制御します。

```
.s7videoviewer .s7controlbar
```

## コントロールバーの CSS プロパティ {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>上部のボーダーから配置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p> 下罫線からパディングを含めて移動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーの背景色 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

ビデオビューアコンテナの上部に配置された、高さが 30 ピクセルのグレーのコントロールバーを持つビデオビューアをセットアップします。

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
