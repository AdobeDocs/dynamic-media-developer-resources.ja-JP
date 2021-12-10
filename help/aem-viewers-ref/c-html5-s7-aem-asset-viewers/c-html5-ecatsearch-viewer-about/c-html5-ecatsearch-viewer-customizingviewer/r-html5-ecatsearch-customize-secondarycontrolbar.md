---
title: セカンダリコントロールバー
description: セカンダリコントロールバーは、「最初」ボタンと「最後」ボタンと、CSS で使用可能にした場合のページインジケーターを含む長方形の領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# セカンダリコントロールバー{#secondary-control-bar}

セカンダリコントロールバーは、「最初」ボタンと「最後」ボタンと、CSS で使用可能にした場合のページインジケーターを含む長方形の領域です。

デフォルトでは、ビューアの下部に携帯電話でのみ表示されます。 ビューアの幅全体を常に取得します。 CSS では、ビューアのコンテナを基準にして、色、高さおよび垂直方向の位置を変更できます。

セカンダリコントロールバーの外観は、以下の CSS クラスセレクターを使用して制御します。

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
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>ビューアの上部からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビューアの下部からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>セカンダリコントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 高さが 72 ピクセルで、ビューアのコンテナの下部に配置するグレーのセカンダリコントロールバーを設定します。

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
