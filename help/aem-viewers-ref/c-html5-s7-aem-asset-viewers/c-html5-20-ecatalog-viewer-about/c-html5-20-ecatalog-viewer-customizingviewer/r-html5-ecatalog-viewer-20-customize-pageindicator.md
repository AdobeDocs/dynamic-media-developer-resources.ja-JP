---
description: ページインジケーターには、現在のページインデックスと合計ページ数が表示されます。 デスクトップシステムおよびタブレットではメインコントロールバーに表示され、携帯電話ではセカンダリコントロールバーに追加されます。 ページインジケーターは、CSSでサイズ変更、スキン表示および配置できます。
seo-description: ページインジケーターには、現在のページインデックスと合計ページ数が表示されます。 デスクトップシステムおよびタブレットではメインコントロールバーに表示され、携帯電話ではセカンダリコントロールバーに追加されます。 ページインジケーターは、CSSでサイズ変更、スキン表示および配置できます。
seo-title: ページインジケーター
solution: Experience Manager
title: ページインジケーター
topic: Dynamic media
uuid: 5e33c149-fdc7-419a-b5ff-b9be3f342d9f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ページインジケーター{#page-indicator}

ページインジケーターには、現在のページインデックスと合計ページ数が表示されます。 デスクトップシステムおよびタブレットではメインコントロールバーに表示され、携帯電話ではセカンダリコントロールバーに追加されます。 ページインジケーターは、CSSでサイズ変更、スキン表示および配置できます。

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
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 56 x 28ピクセルで、水平方向に中央揃えし、メインコントロールバーの下から4ピクセルの位置に配置し、14ピクセルのHelveticaフォントを使用するページインジケーターを設定します。

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

