---
description: 次のコマンドを使用して、高度なテキストフォーマットを設定します。
solution: Experience Manager
title: 詳細なテキストフォーマット
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 詳細なテキストフォーマット{#advanced-text-formatting}

次のコマンドを使用して、高度なテキストフォーマットを設定します。

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
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>フォントサイズを変更しない下付き文字。 </p> </td> 
   <td> <p>ハーフポイント単位の位置。デフォルトは 6 です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>フォントサイズを変更しない上付き文字。 </p> </td> 
   <td> <p>ハーフポイント単位の位置。デフォルトは 6 です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span> </span> </td> 
   <td> <p>指定したフォントサイズで無効/有効にします。 </p> </td> 
   <td> <p>半角のフォントサイズ。その上にカーニングを適用します。カーニングを無効にするには 0 を指定します。1/2 ポイントを超えるすべてのフォントサイズのカーニングでは、デフォルトは 1 です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>「オプティカルカーニング」を選択します。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>指標のカーニングを選択します。 </p> </td> 
   <td> <p>デフォルト。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>文字間隔を修正します。 </p> </td> 
   <td> <p>正または負の四半期ポイント。デフォルトは 0 です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>文字間隔を修正します。 </p> </td> 
   <td> <p>正または負のツイップ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>文字の水平方向の拡大/縮小。 </p> </td> 
   <td> <p>正または負の割合。デフォルトは 100。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>縦書き文字の拡大/縮小。 </p> </td> 
   <td> <p>正または負の割合。デフォルトは 100。Dynamic Media 拡張機能。 </p> <p> <span class="codeph"> \charscaley </span> は、<span class="codeph"> text= </span> を適用した場合に行間隔も拡大/縮小します。 textPs= <span class="codeph"></span>、縦書きの文字の拡大/縮小の量に関係なく、行間隔を常に保持します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>左から右への文字フローを選択します。 </p> </td> 
   <td> <p>デフォルト。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>右から左への文字フローを選択します。 </p> </td> 
   <td> <p> <span class="codeph"> text= </span> のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span> </span> </td> 
   <td> <p>コピー調整を有効にし、許容される最大フォントサイズを設定します。 </p> </td> 
   <td> <p>ハーフポイント単位のフォントサイズ。<span class="codeph"> textPs= </span> のみ。Dynamic Media 拡張機能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>最大コピーフィット線（ソフト制限）。 </p> </td> 
   <td> <p>行の制限なし：0、<span class="codeph"> textPs= </span> のみ、Dynamic Media 拡張機能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>最大コピーフィット線（切り捨て）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ。Dynamic Media 拡張機能です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>文字の方向。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ。欧文以外のフォントでは無視されます。\stextflow1 <span class="codeph"> が有効でない場合 </span> 無視されます。 </p> <p>垂直方向に 0 を指定します（既定値）。 </p> <p>1 を時計回りに 90 度回転します。 </p> </td> 
  </tr> 
 </tbody> 
</table>
