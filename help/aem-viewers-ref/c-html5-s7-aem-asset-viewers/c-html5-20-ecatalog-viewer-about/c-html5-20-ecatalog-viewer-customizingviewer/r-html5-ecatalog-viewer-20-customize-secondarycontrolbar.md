---
title: セカンダリコントロールバー
description: セカンダリコントロールバーは、最初と最後のページボタンと、CSSで使用可能なページインジケーターを含む長方形の領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 2354c3a0-2df7-4a18-aac1-fac158a9b659
TQID: 'https://experienceleague.adobe.com/aT-NQikSvfT9khT6idoN9HcN6oDJBzJv6zoo0G8wg1g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 0%

---

# セカンダリコントロールバー{#secondary-control-bar}

セカンダリコントロールバーは、最初と最後のページボタンと、CSSで使用可能なページインジケーターを含む長方形の領域です。

デフォルトでは、携帯電話でのみ表示され、ビューアの下部に配置されます。 常に利用可能なビューア幅全体を使用します。 ビューアコンテナに対して、CSSで色、高さ、垂直位置を変更できます。

セカンダリコントロールバーの外観は、次のCSS クラスセレクターで制御されます。

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p>ビューアの上部からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p>ビューアの下部からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>セカンダリコントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 高さ72 ピクセルで、ビューアコンテナの下部に配置されたグレーのセカンダリコントロールバーを設定します。

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
