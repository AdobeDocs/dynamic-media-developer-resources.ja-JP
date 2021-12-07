---
title: ビデオ時間
description: ビデオ時間は、現在再生中のビデオの現在の時間と時間を示す数値表示です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---

# ビデオ時間{#video-time}

ビデオ時間は、現在再生中のビデオの現在の時間と時間を示す数値表示です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビデオの時間フォントファミリー、フォントサイズ、フォントカラーは、CSS で制御できるプロパティの 1 つです。 また、CSS を使用して、そのコントロールバーを基準とした位置に配置することもできます。

ビデオ時間の外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7videotime
```

## ビデオ時間の CSS プロパティ {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む上の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む右の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> ビデオ時間制御の幅。 このプロパティは、Internet Explorer 8 以降が正常に機能するために必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントサイズです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

ビデオ時間をライトグレー（16 進数）に設定します。 `#BBBBBB`) のサイズを 12 ピクセルに設定し、コントロールバーの上部から 15 ピクセル、コントロールバーの右端から 80 ピクセルの位置に配置します。

```
.s7smartcropvideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
