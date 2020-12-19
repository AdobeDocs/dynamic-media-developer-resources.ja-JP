---
description: 高度なテキストの書式設定には、次のコマンドを使用します。
seo-description: 高度なテキストの書式設定には、次のコマンドを使用します。
seo-title: 高度なテキストの書式設定
solution: Experience Manager
title: 高度なテキストの書式設定
topic: Scene7 Image Serving - Image Rendering API
uuid: 340166a5-5aef-4081-9114-a715cde68891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 1%

---


# 高度なテキストの書式設定{#advanced-text-formatting}

高度なテキストの書式設定には、次のコマンドを使用します。

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> コマンド </th> 
   <th class="entry"> 説明 </th> 
   <th class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>下付き文字（フォントサイズなし）を変更。 </p> </td> 
   <td> <p>位置はハーフポイント。初期設定は6です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>フォントサイズを変更しない上付き文字。 </p> </td> 
   <td> <p>位置はハーフポイント。初期設定は6です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>指定したフォントサイズで無効/有効にします。 </p> </td> 
   <td> <p>フォントサイズ（ハーフポイント）。この値を超えるとカーニングが適用されます。0の場合、カーニングが無効になります。初期設定は、すべてのフォントサイズを1/2ポイント以上にカーニングする場合に1です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical  </span> </td> 
   <td> <p>オプティカルカーニングを選択 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric  </span> </td> 
   <td> <p>指標のカーニングを選択します。 </p> </td> 
   <td> <p>初期設定. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd  <span class="varname"> N  </span> </span> </td> 
   <td> <p>文字間隔を変更する。 </p> </td> 
   <td> <p>正または負の四半期ポイント初期設定は0です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>文字間隔を変更する。 </p> </td> 
   <td> <p>正または負のtwip。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>水平方向の文字の拡大縮小。 </p> </td> 
   <td> <p>正または負の割合；初期設定は100です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>垂直方向の文字の拡大/縮小 </p> </td> 
   <td> <p>正または負の割合；初期設定は100;Scene7拡張。 </p> <p> <span class="codeph"> \charscaley </span> も、 <span class="codeph"> text=を適用した場合に行間隔を拡大・縮小 </span>します。<span class="codeph"> textPs=では、垂直方向の文字の拡大/縮小の量に関係なく、 </span> 常に行間が保持されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>左から右の文字フローを選択します。 </p> </td> 
   <td> <p>初期設定. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>右から左に書く文字のフローを選択します。 </p> </td> 
   <td> <p> <span class="codeph"> text= </span> のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>「サイズ調整」を有効にし、許可されるフォントサイズを最大に設定 </p> </td> 
   <td> <p>フォントサイズ（半分ポイント）<span class="codeph"> textPs= </span>のみ；Scene7拡張。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>コピーフィット線の最大数（ソフトリミット） </p> </td> 
   <td> <p>0（行制限なし）<span class="codeph"> textPs= </span>のみ；Scene7拡張。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>コピーフィットの最大行数（切り捨て） </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;Scene7拡張。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>文字の向き。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;欧文以外のフォントでは無視されます。は、 <span class="codeph"> \stextflow1が有効で </span> ない場合は無視されます。 </p> <p>0垂直（デフォルト） </p> <p>1を右回りに90度回転させました。 </p> </td> 
  </tr> 
 </tbody> 
</table>

