---
description: コントロールバーは、再生/一時停止ボタン、ボリュームコントロールなど、スマート切り抜きビデオビューアで使用できるすべての UI コントロールを含み、その背後に配置される長方形の領域です。
solution: Experience Manager
title: コントロールバー
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2239307a-4a05-4392-b35c-a64ea6c938ad
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 2%

---

# コントロールバー{#control-bar}

コントロールバーは、再生/一時停止ボタン、ボリュームコントロールなど、スマート切り抜きビデオビューアで使用できるすべての UI コントロールを含み、その背後に配置される長方形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは、常に、使用可能なビューアの幅全体を占めます。 スマート切り抜きビデオビューアコンテナに対して、CSS を使用して、色、高さおよび垂直方向の位置を変更できます。

以下に示す CSS クラスセレクターで、コントロールバーの外観を制御します。

```
.s7smartcropvideoviewer .s7controlbar
```

## コントロールバーの CSS プロパティ {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む上の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む下の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

高さが 30 ピクセルで、スマート切り抜きビデオビューアコンテナの上に配置されるグレーのコントロールバーを持つスマート切り抜きビデオビューアを設定するには、次の手順に従います。

```
.s7smartcropvideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
