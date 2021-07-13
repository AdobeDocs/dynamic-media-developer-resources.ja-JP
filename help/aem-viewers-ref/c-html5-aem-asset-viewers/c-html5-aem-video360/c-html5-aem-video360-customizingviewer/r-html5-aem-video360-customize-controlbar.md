---
description: コントロールバーは、再生/一時停止ボタン、音量コントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その後ろに配置する矩形の領域です。
solution: Experience Manager
title: コントロールバー
feature: Dynamic Media Classic，ビューア，SDK/API,360 VRビデオ
role: Developer,User
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# コントロールバー{#control-bar}

コントロールバーは、再生/一時停止ボタン、音量コントロールなど、ビデオビューアで使用できるすべてのユーザインターフェイスコントロールを含み、その後ろに配置する矩形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

コントロールバーは、常に、ビューアの幅全体に合わせて表示されます。 CSSで、ビデオビューアのコンテナに対するカラー、高さ、垂直方向の位置を変更できます。

以下に示すCSSクラスセレクターで、コントロールバーの外観を制御します。

```
.s7video360viewer .s7controlbar
```

## コントロールバーのCSSプロパティ {#css-properties-of-the-control-bar}

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

**例**  — 高さが30ピクセルで、ビデオビューアのコンテナの上部に配置するグレーのコントロールバーを持つビデオビューアを設定するには、次のように記述します。

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
