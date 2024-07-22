---
title: ページインジケーター
description: ページインジケーターは、現在のページインデックスと合計ページ数を表示します。 デスクトップシステムやタブレットのメインコントロールバーに表示され、携帯電話ではセカンダリコントロールバーに追加されます。 ページインジケーターは、CSS を使用してサイズ変更、スキニング、配置を行うことができます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# ページインジケーター{#page-indicator}

ページインジケーターは、現在のページインデックスと合計ページ数を表示します。 デスクトップシステムやタブレットのメインコントロールバーに表示され、携帯電話ではセカンダリコントロールバーに追加されます。 ページインジケーターは、CSS を使用してサイズ変更、スキニング、配置を行うことができます。

外観ページインジケーターは、次の CSS クラスセレクターで制御します。

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
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムやタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の上部ボーダーからパディングを含めて配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムやタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の右端から配置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムやタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の左側のボーダーから、パディングを含めて配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバー（デスクトップシステムやタブレットの場合）またはセカンダリコントロールバー（携帯電話の場合）の下部の境界線からの位置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ページインジケーターの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ページインジケーターの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>フォントカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 56 x 28 ピクセルのページインジケーターをメインコントロールバーの下部から水平方向に中央に 4 ピクセル配置して設定し、14 ピクセルの Helvetica® フォントを使用する場合

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
