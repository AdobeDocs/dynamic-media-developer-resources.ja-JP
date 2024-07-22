---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2669c8e2-c942-420f-8262-9d76d5c499a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *`dividerWidth`*, *`dividerColor`*, *`dividerOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`]

[!DNL `PageView.frametransition`] が [!DNL `turn`] に設定されている場合、またはデスクトップシステムで [!DNL `auto`] に設定されている場合のコンポーネントの外観を制御します。

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> dividerWidth<span class="codeph"><span class="varname"> 指定 </span></span> </p> </td> 
   <td colname="col2"> <p> スプレッド内で左右のページを区切るページディバイダーのシャドウの幅（ピクセル単位）。 また、ターニングページの横に表示される連続影の幅も制御します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>dividerOpacity<span class="codeph"><span class="varname"> 指定 </span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB 形式の影の色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>dividerOpacity<span class="codeph"><span class="varname"> 指定 </span></span> </p> </td> 
   <td colname="col2"> <p>0</span> ～ <span class="codeph"> 1</span> の範囲のシャドウ <span class="codeph"> 不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> 回転するページの周囲の境界線をオンまたはオフにするフラグ（<span class="codeph"> 0</span> または <span class="codeph"> 1</span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> 境界線のカラー（RRGGBB 形式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>fillColor<span class="codeph"><span class="varname"> 指定 </span></span> </p> </td> 
   <td colname="col2"> <p> ページターンアニメーション中に使用されるコンポーネント領域の塗りつぶしの色（RRGGBB 形式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-54c634116cfe4f17813318e07539264c}

オプション。

## 初期設定 {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## 例 {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
