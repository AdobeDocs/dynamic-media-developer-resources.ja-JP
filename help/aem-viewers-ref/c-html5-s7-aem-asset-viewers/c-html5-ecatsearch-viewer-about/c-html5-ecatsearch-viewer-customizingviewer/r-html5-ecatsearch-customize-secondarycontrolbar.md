---
description: セカンダリコントロールバーは、「最初」ボタンと「最後」ボタンと、CSSで使用可能にした場合のページインジケーターを含む長方形の領域です。
solution: Experience Manager
title: セカンダリコントロールバー
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,Business Practitioner
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 2%

---

# セカンダリコントロールバー{#secondary-control-bar}

セカンダリコントロールバーは、「最初」ボタンと「最後」ボタンと、CSSで使用可能にした場合のページインジケーターを含む長方形の領域です。

デフォルトでは、携帯電話にのみ表示され、ビューアの下部に表示されます。 ビューアの幅は常に全体となります。 CSSで、ビューアのコンテナに対するカラー、高さ、垂直方向の位置を変更できます。

セカンダリコントロールバーの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>ビューアの上端からの位置 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビューアの下端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>セカンダリコントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 高さが72ピクセルで、ビューアのコンテナの下部に配置するグレーのセカンダリコントロールバーを設定します。

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
