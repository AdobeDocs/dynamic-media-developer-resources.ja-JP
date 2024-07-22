---
title: コントロールバー
description: コントロール バーは、ビデオ ビューアーで使用可能なすべてのユーザーインターフェイス コントロール （再生/一時停止ボタンや音量コントロールなど）の背後にある、を含む四角形の領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# コントロールバー{#control-bar}

コントロール バーは、ビデオ ビューアーで使用可能なすべてのユーザーインターフェイス コントロール （再生/一時停止ボタンや音量コントロールなど）の背後にある、を含む四角形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは常に、使用可能なビューアの幅全体を取ります。 色、高さ、垂直方向の位置を、ビデオビューアコンテナに対して CSS で変更できます。

次の CSS クラスセレクターで、コントロールバーの外観を制御します。

```
.s7video360viewer .s7controlbar
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

**例** – 高さが 30 ピクセルで、ビデオビューアコンテナの上部に配置されたグレーのコントロールバーを持つビデオビューアを設定します。

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
