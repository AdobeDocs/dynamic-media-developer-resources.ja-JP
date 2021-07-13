---
description: ページインジケーターは、現在のページインデックスと合計ページ数を表示します。 デスクトップシステムおよびタブレットのメインコントロールバーに表示され、携帯電話の場合はセカンダリコントロールバーに追加されます。 ページインジケーターは、CSSを使用してサイズ設定、スキン、配置できます。
solution: Experience Manager
title: ページインジケーター
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,User
exl-id: c63af583-274c-4052-8186-604119a368af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 3%

---

# ページインジケーター{#page-indicator}

ページインジケーターは、現在のページインデックスと合計ページ数を表示します。 デスクトップシステムおよびタブレットのメインコントロールバーに表示され、携帯電話の場合はセカンダリコントロールバーに追加されます。 ページインジケーターは、CSSを使用してサイズ設定、スキン、配置できます。

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
