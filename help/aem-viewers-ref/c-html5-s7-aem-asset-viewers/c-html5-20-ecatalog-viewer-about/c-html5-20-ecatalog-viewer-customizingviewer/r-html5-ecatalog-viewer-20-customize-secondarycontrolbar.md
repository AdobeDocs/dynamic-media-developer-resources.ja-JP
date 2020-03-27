---
description: セカンダリコントロールバーは、CSSで「先頭ページ」ボタンと「最後のページ」ボタンを使用できる場合は、ページインジケーターを含む矩形の領域です。
seo-description: セカンダリコントロールバーは、CSSで「先頭ページ」ボタンと「最後のページ」ボタンを使用できる場合は、ページインジケーターを含む矩形の領域です。
seo-title: セカンダリコントロールバー
solution: Experience Manager
title: セカンダリコントロールバー
topic: Dynamic media
uuid: 9a91da6b-0d9b-4b4c-9659-86a64e624947
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# セカンダリコントロールバー{#secondary-control-bar}

セカンダリコントロールバーは、CSSで「先頭ページ」ボタンと「最後のページ」ボタンを使用できる場合は、ページインジケーターを含む矩形の領域です。

初期設定では、携帯電話にのみ表示され、ビューアの下部に表示されます。 ビューアの幅は、常に使用可能な幅全体に収まります。 ビューアのコンテナを基準にして、CSSで色、高さおよび垂直方向の位置を変更できます。

セカンダリコントロールバーの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

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
   <td colname="col2"> <p>ビューアの上端からの位置。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>セカンダリコントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 高さが72ピクセルで、ビューアのコンテナの下部に配置するグレーのセカンダリコントロールバーを設定します。

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

