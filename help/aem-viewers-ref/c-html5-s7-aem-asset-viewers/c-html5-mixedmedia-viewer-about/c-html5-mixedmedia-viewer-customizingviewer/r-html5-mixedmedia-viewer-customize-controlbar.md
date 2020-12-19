---
description: コントロールバーは、再生/一時停止ボタン、ボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その背後に配置する矩形の領域です。
seo-description: コントロールバーは、再生/一時停止ボタン、ボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その背後に配置する矩形の領域です。
seo-title: コントロールバー
solution: Experience Manager
title: コントロールバー
topic: Dynamic media
uuid: 7b7dccb3-6c64-4342-aac7-82c769561902
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---


# コントロールバー{#control-bar}

コントロールバーは、再生/一時停止ボタン、ボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その背後に配置する矩形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは、ビューアの幅いっぱいに表示されます。 カラー、高さおよびビデオビューアのコンテナに対する垂直方向の位置は、CSSで変更できます。

以下に示すCSSクラスセレクターで、コントロールバーの外観を制御します。

```
.s7mixedmediaviewer .s7controlbar
```

## コントロールバー{#css-properties-of-the-control-bar}のCSSプロパティ

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

高さが30ピクセルのグレーのコントロールバーのある混在メディアビューアを設定するには、次のように記述します。

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

