---
title: ビデオ時間
description: ビデオ時間は、現在再生中のビデオの現在の時間とデュレーションを示す数値表示です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0ef09f06-c2d5-4c84-8ff9-4e94e9e54d40
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# ビデオ時間{#video-time}

ビデオ時間は、現在再生中のビデオの現在の時間とデュレーションを示す数値表示です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビデオ時間のフォントファミリー、フォントサイズ、フォントカラーは、CSS が制御できるプロパティの 1 つです。 また、CSS を使用して、タグを含むコントロールバーに対して相対的にタグを配置することもできます。

ビデオ時間の外観は、次の CSS クラスセレクターで制御します。

```
.s7smartcropvideoviewer .s7videotime
```

## ビデオ時間の CSS プロパティ {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>上部のボーダーから配置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>パディングを含めて、右側のボーダーから配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> ビデオ時間コントロールの幅。 このプロパティは、Internet Explorer 8 以降が正常に機能するために必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

ビデオ時間をライトグレー（16 進 `#BBBBBB`）に設定します。12 ピクセルのサイズで、コントロールバーの上部から 15 ピクセル、コントロールバーの右端から 80 ピクセルの位置に配置します。

```
.s7smartcropvideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
