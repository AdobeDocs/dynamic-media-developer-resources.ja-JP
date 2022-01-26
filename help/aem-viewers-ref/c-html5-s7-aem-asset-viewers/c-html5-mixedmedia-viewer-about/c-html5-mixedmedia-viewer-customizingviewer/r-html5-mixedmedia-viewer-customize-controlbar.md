---
title: コントロールバー
description: コントロールバーは、再生/一時停止ボタン、ボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その背後に配置される長方形の領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 1%

---

# コントロールバー{#control-bar}

コントロールバーは、再生/一時停止ボタン、ボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その背後に配置される長方形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは、常に、使用可能なビューアの幅全体を占めます。 ビデオビューアのコンテナを基準に、CSS で色、高さおよび垂直方向の位置を変更できます。

以下に示す CSS クラスセレクターで、コントロールバーの外観を制御します。

```
.s7mixedmediaviewer .s7controlbar
```

## コントロールバーの CSS プロパティ {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
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

高さが 30 ピクセルのグレーのコントロールバーを持つ混在メディアビューアを設定するには

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
