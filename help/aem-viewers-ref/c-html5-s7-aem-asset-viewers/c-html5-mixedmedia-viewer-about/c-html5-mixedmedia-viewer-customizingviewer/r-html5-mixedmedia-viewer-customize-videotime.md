---
description: ビデオ時間は、現在再生中のビデオの現在時間と長さを示す数値表示です。
seo-description: ビデオ時間は、現在再生中のビデオの現在時間と長さを示す数値表示です。
seo-title: ビデオ時間
solution: Experience Manager
title: ビデオ時間
topic: Dynamic media
uuid: f93e495b-44a1-493c-9bc6-5c088478ddce
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video time{#video-time}

ビデオ時間は、現在再生中のビデオの現在時間と長さを示す数値表示です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビデオ時間のフォントファミリ、フォントサイズ、フォントカラーは、CSSで制御できるプロパティの1つです。 また、CSSを使用して、これを含むコントロールバーを基準にして配置することもできます。

ビデオ時間の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7videotime
```

## ビデオ時間のCSSプロパティ {#css-properties-of-video-time}

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
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>時間表示テキストに使用するフォントファミリーです。 </p> </td> 
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

ビデオ時間をライトグレー(16進数 `#BBBBBB`)に設定し、サイズを12ピクセルにして、コントロールバーの上端から15ピクセル、コントロールバーの右端から80ピクセルの位置に配置します。

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```

