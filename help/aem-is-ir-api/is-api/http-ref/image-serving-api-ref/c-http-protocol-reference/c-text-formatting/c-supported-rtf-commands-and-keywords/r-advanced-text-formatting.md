---
description: 高度なテキストの書式設定を行うには、次のコマンドを使用します。
seo-description: 高度なテキストの書式設定を行うには、次のコマンドを使用します。
seo-title: 高度なテキストの書式設定
solution: Experience Manager
title: 高度なテキストの書式設定
topic: Scene7 Image Serving - Image Rendering API
uuid: 340166a5-5aef-4081-9114-a715cde68891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 高度なテキストの書式設定{#advanced-text-formatting}

高度なテキストの書式設定を行うには、次のコマンドを使用します。

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
   <td> <span class="codeph"> \dn <span class="varname"> N </span></span> </td> 
   <td> <p>下付き文字（フォントサイズなし）を変更。 </p> </td> 
   <td> <p>位置はハーフポイント。初期設定は6です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span></span> </td> 
   <td> <p>上付き文字（フォントサイズを変更しない） </p> </td> 
   <td> <p>位置はハーフポイント。初期設定は6です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span></span> </td> 
   <td> <p>指定したフォントサイズで無効/有効にします。 </p> </td> 
   <td> <p>フォントサイズ（ハーフポイント）。上にカーニングを適用します。0を指定するとカーニングが無効になります。初期設定は、1/2ポイントを超えるすべてのフォントサイズをカーニングする場合は1です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>オプティカルカーニングを選択します。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>指標のカーニングを選択します。 </p> </td> 
   <td> <p>初期設定. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span></span> </td> 
   <td> <p>文字間隔を変更します。 </p> </td> 
   <td> <p>正または負の四半期；初期設定は0です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span></span> </td> 
   <td> <p>文字間隔を変更します。 </p> </td> 
   <td> <p>正または負のtwip。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span></span> </td> 
   <td> <p>水平方向の文字の拡大/縮小 </p> </td> 
   <td> <p>正または負の割合。初期設定は100です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span></span> </td> 
   <td> <p>垂直方向の文字の拡大/縮小 </p> </td> 
   <td> <p>正または負の割合。初期設定は100;Scene7 Extension。 </p> <p> <span class="codeph"> \charscaleyは、 </span> text=を適用した場合も行間を拡大・縮小 <span class="codeph"> しま </span>す。 <span class="codeph"> textPs=では、縦 </span> 方向の文字の拡大/縮小の量に関係なく、行間が常に保持されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>左から右の文字フローを選択します。 </p> </td> 
   <td> <p>初期設定. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>右から左に書く文字フローを選択します。 </p> </td> 
   <td> <p> <span class="codeph"> text=の </span> み。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span></span> </td> 
   <td> <p>コピーフィットを有効にし、許容される最大フォントサイズを設定します。 </p> </td> 
   <td> <p>フォントサイズ（ハーフポイント）; <span class="codeph"> textPs= </span> のみ；Scene7 Extension。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span></span> </td> 
   <td> <p>コピーフィット線の最大数（ソフトリミット） </p> </td> 
   <td> <p>0（行制限なし） <span class="codeph"> textPs= </span> のみ；Scene7 Extension。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span></span> </td> 
   <td> <p>コピーフィットの最大行数（切り捨て） </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み；Scene7 Extension。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span></span> </td> 
   <td> <p>文字の向き。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み；欧文以外のフォントでは無視されます。\stextflow1が有 <span class="codeph"> 効でな </span> い場合は無視されます。 </p> <p>0垂直（デフォルト）。 </p> <p>1を右回りに90°回転しました。 </p> </td> 
  </tr> 
 </tbody> 
</table>

