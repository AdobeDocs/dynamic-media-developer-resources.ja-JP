---
description: ビデオ時間は、現在時間と現在再生中のビデオの長さを数値で表示します。
seo-description: ビデオ時間は、現在時間と現在再生中のビデオの長さを数値で表示します。
seo-title: ビデオ時間
solution: Experience Manager
title: ビデオ時間
topic: Dynamic media
uuid: a15b069a-18c8-428f-ac6f-ab5aeda65f4d
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 2%

---


# ビデオ時間{#video-time}

ビデオ時間は、現在時間と現在再生中のビデオの長さを数値で表示します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビデオ時間のフォントファミリー、フォントサイズおよびフォントカラーのプロパティは、CSSで制御できます。 また、このコントロールを含むコントロールバーに対する位置も、CSSで設定できます。

ビデオ時間の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7videoviewer .s7videotime
```

## ビデオ時間{#css-properties-of-video-time}のCSSプロパティ

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
   <td colname="col2"> <p> ビデオ時間コントロールの幅。 このプロパティは、Internet Explorer 8以降が正しく機能するために必要です。 </p> </td> 
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

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

ライトグレー（16進数`#BBBBBB`）で、サイズが12ピクセルで、コントロールバーの上から15ピクセル、コントロールバーの右端から80ピクセルの位置に配置するビデオ時間を設定します。

```
.s7videoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```

