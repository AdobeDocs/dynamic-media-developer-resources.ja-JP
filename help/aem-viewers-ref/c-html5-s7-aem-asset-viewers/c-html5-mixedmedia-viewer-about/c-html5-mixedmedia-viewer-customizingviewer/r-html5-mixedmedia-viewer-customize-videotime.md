---
description: ビデオ時間は、現在再生中のビデオの現在時間と時間を示す数値表示です。
solution: Experience Manager
title: ビデオ時間
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,User
exl-id: 5efae314-5f37-4afc-9b9e-3108a8529e50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

---

# ビデオ時間{#video-time}

ビデオ時間は、現在再生中のビデオの現在時間と時間を示す数値表示です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビデオ時間のフォントファミリ、フォントサイズ、フォントカラーは、CSSで制御できるプロパティの1つです。 また、CSSを使用して、このコントロールバーを含むコントロールバーに対する相対位置を指定することもできます。

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
   <td colname="col2"> <p> ビデオ時間制御の幅。 このプロパティは、Internet Explorer 8以降が正しく機能するために必要です。 </p> </td> 
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

ライトグレー（16進数`#BBBBBB`）でサイズが12ピクセルで、コントロールバーの上から15ピクセル、コントロールバーの右端から80ピクセルの位置に配置するビデオ時間を設定します。

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
