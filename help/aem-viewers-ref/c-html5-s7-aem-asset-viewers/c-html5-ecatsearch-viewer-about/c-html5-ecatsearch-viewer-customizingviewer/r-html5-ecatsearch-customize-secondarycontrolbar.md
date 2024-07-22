---
title: セカンダリコントロールバー
description: セカンダリコントロールバーは、CSS で使用できる場合、最初と最後のページボタンとページインジケーターを含む長方形の領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# セカンダリコントロールバー{#secondary-control-bar}

セカンダリコントロールバーは、CSS で使用できる場合、最初と最後のページボタンとページインジケーターを含む長方形の領域です。

デフォルトでは、ビューアの下部に携帯電話でのみ表示されます。 常に、使用可能なビューアの幅の全体が使用されます。 ビューアのコンテナを基準にして、CSS でカラー、高さ、垂直方向の位置を変更できます。

セカンダリコントロールバーの外観は、次の CSS クラスセレクターで制御します。

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>ビューアの上部からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビューアの下部からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>メイン コントロール バーの高さです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>セカンダリ コントロール バーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 高さが 72 ピクセルで、ビューアコンテナの下部に配置されているグレーのセカンダリコントロールバーを設定する

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
