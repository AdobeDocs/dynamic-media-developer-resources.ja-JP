---
description: 次のコマンドを使用して、高度なテキスト書式を設定します。
solution: Experience Manager
title: 高度なテキスト書式設定
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 1%

---

# 高度なテキスト書式設定{#advanced-text-formatting}

次のコマンドを使用して、高度なテキスト書式を設定します。

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
   <td> <p>フォントサイズのない下付き文字を変更。 </p> </td> 
   <td> <p>半分ポイントでの位置初期設定は6です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>フォントサイズを変更しない上付き文字 </p> </td> 
   <td> <p>半分ポイントでの位置初期設定は6です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>指定したフォントサイズでの無効化/有効化 </p> </td> 
   <td> <p>カーニングを適用するフォントサイズ（半分ポイント単位）0の場合、カーニングを無効にします。初期設定は、1/2ポイントを超えるすべてのフォントサイズにカーニングを適用する場合は1です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical  </span> </td> 
   <td> <p>オプティカルカーニングを選択します。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み。 </p> </td> 
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
   <td> <p>水平方向の文字の拡大/縮小 </p> </td> 
   <td> <p>正または負の割合初期設定は100です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>縦方向の文字の拡大/縮小 </p> </td> 
   <td> <p>正または負の割合デフォルトは100です。Dynamic Media拡張機能。 </p> <p> <span class="codeph"> \charscaleyは、  </span> text=を適用した場合 <span class="codeph"> に、行間を拡大/縮小しま </span>す。<span class="codeph"> textPs=で </span> は、縦方向の文字の拡大/縮小の量に関係なく、常に行間が保持されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltch  </span> </td> 
   <td> <p>左から右の文字フローを選択します。 </p> </td> 
   <td> <p>初期設定. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>右から左の文字フローを選択します。 </p> </td> 
   <td> <p> <span class="codeph"> text=の </span> み。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>コピーフィッティングを有効にし、許容される最大フォントサイズを設定します。 </p> </td> 
   <td> <p>フォントサイズ（半分ポイント）<span class="codeph"> textPs= </span>のみ；Dynamic Media拡張機能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>コピーフィット線の最大値（ソフトリミット） </p> </td> 
   <td> <p>0（ライン制限なし）<span class="codeph"> textPs= </span>のみ；Dynamic Media拡張機能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>最大コピーフィット線（切り捨て） </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ；Dynamic Media拡張機能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>文字の向き。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ；ローマ以外のフォントでは無視されます。\stextflow1が有 <span class="codeph"> 効でな </span> い場合は無視されます。 </p> <p>0垂直（デフォルト） </p> <p>1時計回りに90度回転 </p> </td> 
  </tr> 
 </tbody> 
</table>
