---
title: ビデオ時間
description: ビデオ時間は、現在再生中のビデオの現在時間と時間を示す数値表示です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 78657fd2-e805-4047-be0a-592143025986
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---

# ビデオ時間{#video-time}

ビデオ時間は、現在再生中のビデオの現在時間と時間を示す数値表示です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビデオ時間のフォントファミリー、フォントサイズ、フォントカラーは、CSS で制御できるプロパティの 1 つです。 また、CSS を使用して、このコントロールバーを含むコントロールバーに対する相対位置を指定することもできます。

ビデオ時間の外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7video360viewer .s7videotime
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
   <td colname="col2"> <p> ビデオ時間制御の幅。 このプロパティは、Internet Explorer 8 以降が正しく機能するために必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — サイズが 12 ピクセルで、コントロールバーの上から 15 ピクセル、コントロールバーの上および右端から 80 ピクセルの位置に配置するライトグレー (16 進 `#BBBBBB`数 ) のビデオ時間を設定します。

```
.s7video360viewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
