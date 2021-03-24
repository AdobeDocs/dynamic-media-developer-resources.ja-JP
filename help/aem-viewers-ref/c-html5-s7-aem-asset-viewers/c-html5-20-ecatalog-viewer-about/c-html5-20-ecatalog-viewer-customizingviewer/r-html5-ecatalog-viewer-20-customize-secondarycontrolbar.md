---
description: セカンダリコントロールバーは、最初と最後のページのボタンと、ページインジケーターがCSSで使用可能になった場合に表示される矩形の領域です。
solution: Experience Manager
title: セカンダリコントロールバー
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# セカンダリコントロールバー{#secondary-control-bar}

セカンダリコントロールバーは、最初と最後のページのボタンと、ページインジケーターがCSSで使用可能になった場合に表示される矩形の領域です。

デフォルトでは、携帯電話にのみ表示され、ビューアの下部にあります。 ビューアの幅は常にそのままです。 カラー、高さ、およびビューアのコンテナに対する垂直方向の位置は、CSSで変更できます。

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>セカンダリコントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 高さが72ピクセルで、ビューアコンテナの下部に配置するグレーのセカンダリコントロールバーを設定します。

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

