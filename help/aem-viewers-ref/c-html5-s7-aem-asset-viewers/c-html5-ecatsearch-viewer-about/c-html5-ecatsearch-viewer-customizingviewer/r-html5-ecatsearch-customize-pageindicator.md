---
title: ページインジケーター
description: ページインジケーターには、現在のページインデックスと合計ページ数が表示されます。 デスクトップシステムとタブレットのメインコントロールバーに表示され、携帯電話ではセカンダリコントロールバーに追加されます。 ページインジケーターは、CSSでサイズ、スキン、配置できます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
TQID: 'https://experienceleague.adobe.com/QikQn00CFMxmnTEXKZcTifhXC-SBmW-IC9VbKlZ7TGY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 0%

---

# ページインジケーター{#page-indicator}

ページインジケーターには、現在のページインデックスと合計ページ数が表示されます。 デスクトップシステムとタブレットのメインコントロールバーに表示され、携帯電話ではセカンダリコントロールバーに追加されます。 ページインジケーターは、CSSでサイズ、スキン、配置できます。

アピアランス ページのインジケーターは、次のCSS クラスセレクターで制御されます。

`.s7ecatalogsearchviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレット）またはセカンダリコントロールバー（携帯電話）の上部境界線（パディングを含む）からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレット）またはセカンダリコントロールバー（携帯電話）の右端から、パディングを含む位置を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">さんが</span>を残しました </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレット）またはセカンダリコントロールバー（携帯電話）の左端（パディングを含む）からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムおよびタブレット）またはセカンダリコントロールバー（携帯電話）の下部境界（パディングを含む）からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ページインジケータの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ページインジケータの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>フォントカラー： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 56 x 28 ピクセルのページインジケーターを設定し、メインコントロールバーの下部から4 ピクセルを水平方向に中央に配置し、14 ピクセルのHelvetica® フォントを使用します。

```
.s7ecatalogsearchviewer  .s7pageindicator { 
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
