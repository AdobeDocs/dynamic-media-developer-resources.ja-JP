---
title: PageView.pageturnstyle
description: PageView.pageturnstyle
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 00706c64-c051-4b62-8194-61d0a1c565e9
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *`dividerWidth`*, *`dividerColor`*, *`dividerOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`

コンポーネントの外観をコントロールします。 `PageView.frametransition` が `turn` または `auto` （デスクトップシステムの場合）

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> 見開きの左右のページを区切るページ区切りのシャドウの幅（ピクセル単位）。 また、めくるページの横に表示される実行中のシャドウの幅も制御します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> シャドウの色（RRGGBB 形式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>シャドウの不透明度 <span class="codeph"> 0</span> から <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> フラグ ( <span class="codeph"> 0</span> または <span class="codeph"> 1</span>) をクリックします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> 境界線のカラー（RRGGBB 形式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> ページめくりアニメーション中に使用されるコンポーネント領域の塗りのベタ塗りのカラー（RRGGBB 形式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-54c634116cfe4f17813318e07539264c}

（オプション）

## 初期設定 {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## 例 {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
