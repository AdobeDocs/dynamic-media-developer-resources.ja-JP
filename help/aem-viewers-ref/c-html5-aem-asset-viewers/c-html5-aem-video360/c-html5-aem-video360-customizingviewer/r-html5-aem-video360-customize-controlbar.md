---
description: コントロールバーは、再生/一時停止ボタン、ボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その背後に配置する矩形の領域です。
seo-description: コントロールバーは、再生/一時停止ボタン、ボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その背後に配置する矩形の領域です。
seo-title: コントロールバー
solution: Experience Manager
title: コントロールバー
topic: Dynamic media
uuid: 328e34f1-9e60-4056-9a8a-e9292fb65605
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# コントロールバー{#control-bar}

コントロールバーは、再生/一時停止ボタン、ボリュームコントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その背後に配置する矩形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは、ビューアの幅いっぱいに表示されます。 カラー、高さおよびビデオビューアのコンテナに対する垂直方向の位置は、CSSで変更できます。

以下に示すCSSクラスセレクターで、コントロールバーの外観を制御します。

```
.s7video360viewer .s7controlbar
```

## コントロールバー{#css-properties-of-the-control-bar}のCSSプロパティ

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — 高さが30ピクセルで、ビデオビューアコンテナの上部に配置するグレーのコントロールバーを持つビデオビューアを設定するには、次のように記述します。

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

