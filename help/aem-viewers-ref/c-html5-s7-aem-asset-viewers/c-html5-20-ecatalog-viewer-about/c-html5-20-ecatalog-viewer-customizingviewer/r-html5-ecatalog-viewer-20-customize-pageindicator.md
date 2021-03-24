---
description: ページインジケーターには、現在のページのインデックスと合計ページ数が表示されます。 このボタンは、デスクトップシステムおよびタブレットではメインコントロールバーに表示され、携帯電話ではセカンダリコントロールバーに追加されます。 ページインジケーターは、CSSを使用して、サイズ設定、スキン表示および配置できます。
solution: Experience Manager
title: ページインジケーター
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 3%

---


# ページインジケータ{#page-indicator}

ページインジケーターには、現在のページのインデックスと合計ページ数が表示されます。 このボタンは、デスクトップシステムおよびタブレットではメインコントロールバーに表示され、携帯電話ではセカンダリコントロールバーに追加されます。 ページインジケーターは、CSSを使用して、サイズ設定、スキン表示および配置できます。

ページインジケーターの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の上の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の右の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の左の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の下の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ページインジケーターの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ページインジケーターの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>フォントカラー. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>フォント名 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 56 x 28ピクセルで、水平方向に中央揃えしてメインコントロールバーの下から4ピクセルの位置に配置し、14ピクセルのHelveticaフォントを使用するページインジケーターを設定します。

```
.s7ecatalogviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```

