---
description: 'null'
seo-description: 'null'
seo-title: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
topic: Dynamic media
uuid: 3192d810-fb30-44ae-9939-98e890c76e5c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *`dividerWidthdividerColordividerOpacityborderOnOffborderColorfillColor`*, *``*, *``*, *``*, *``*, *``*`

をデスクトップシステムで、またはに設 `PageView.frametransition` 定した場合のコンポ `turn` ーネントの外 `auto` 観を制御します。

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> 見開きの左右のページを区切るページ区切りシャドウの幅（ピクセル単位）です。 めくっているページの横に表示される実行中のシャドウの幅も制御します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB形式のシャドウカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>シャドウの不透明度(0 ～ <span class="codeph"> 1</span> ) <span class="codeph"></span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> めくっているページの <span class="codeph"> 周囲の境界線のオン/オフを切り替えるフラグ(0</span> また <span class="codeph"> は1</span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB形式の境界線の色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> ページめくりアニメーション中に使用されるコンポーネント領域のべた塗りのカラー（RRGGBB形式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-54c634116cfe4f17813318e07539264c}

（オプション）

## 初期設定 {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## 例 {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
