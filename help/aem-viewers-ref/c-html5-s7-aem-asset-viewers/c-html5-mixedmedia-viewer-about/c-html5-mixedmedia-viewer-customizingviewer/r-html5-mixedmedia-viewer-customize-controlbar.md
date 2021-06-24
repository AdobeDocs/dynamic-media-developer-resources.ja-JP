---
description: コントロールバーは、再生/一時停止ボタン、音量コントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その後ろに配置する矩形の領域です。
solution: Experience Manager
title: コントロールバー
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# コントロールバー{#control-bar}

コントロールバーは、再生/一時停止ボタン、音量コントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その後ろに配置する矩形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは、常に、ビューアの幅全体に合わせて表示されます。 CSSで、ビデオビューアのコンテナに対するカラー、高さ、垂直方向の位置を変更できます。

以下に示すCSSクラスセレクターで、コントロールバーの外観を制御します。

```
.s7mixedmediaviewer .s7controlbar
```

## コントロールバーのCSSプロパティ {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

高さが30ピクセルのグレーのコントロールバーを持つ混在メディアビューアを設定するには

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
