---
description: 詳細なテキスト書式設定には、次のコマンドを使用します。
solution: Experience Manager
title: 詳細テキスト書式設定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
TQID: 'https://experienceleague.adobe.com/ZTUWB5N6T-I3DnokCqX--dj9g-807-D9Fv8l20opVkg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 0%

---

# 詳細テキスト書式設定{#advanced-text-formatting}

詳細なテキスト書式設定には、次のコマンドを使用します。

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
   <td> <p>半点の位置。デフォルトは6です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>フォントサイズを変更しない上付き文字。 </p> </td> 
   <td> <p>半点の位置。デフォルトは6です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span> </span> </td> 
   <td> <p>指定したフォントサイズで無効/有効にします。 </p> </td> 
   <td> <p>カーニングを適用する上で、半点のフォントサイズ。カーニングを無効にする場合は0で、カーニングを無効にする場合は1です。デフォルトでは、1/2点を超えるすべてのフォントサイズをカーニングします。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>オプティカルカーニングを選択します。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>指標カーニングを選択します。 </p> </td> 
   <td> <p>デフォルト： </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>文字間隔を変更します。 </p> </td> 
   <td> <p>正または負のクォーターポイント。デフォルトは0です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>文字間隔を変更します。 </p> </td> 
   <td> <p>ポジティブまたはネガティブなツイップ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>横組み文字の拡大・縮小。 </p> </td> 
   <td> <p>正または負の割合。デフォルトは100です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>文字の垂直方向の拡大・縮小： </p> </td> 
   <td> <p>正または負のパーセント。デフォルトは100、Dynamic Media拡張機能です。 </p> <p> <span class="codeph"> \charscaley </span>は、<span class="codeph"> text= </span>を適用した場合にも行間を拡大・縮小します。 <span class="codeph"> textPs= </span>は、縦方向の文字の拡大・縮小の量に関係なく、常に行間を保持します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>左から右への文字フローを選択します。 </p> </td> 
   <td> <p>デフォルト： </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>右から左への文字フローを選択します。 </p> </td> 
   <td> <p> <span class="codeph"> テキスト= </span>のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span> </span> </td> 
   <td> <p>コピーフィッティングを有効にし、許可される最大のフォントサイズを設定します。 </p> </td> 
   <td> <p>フォントサイズ （ハーフポイント）、<span class="codeph"> textPs= </span>のみ、Dynamic Media拡張機能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>最大コピーフィット線（ソフト制限）。 </p> </td> 
   <td> <p>行の制限なしの場合は0です。<span class="codeph"> textPs= </span>のみ。Dynamic Media拡張機能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>最大コピー適合行（切り捨て）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>のみ。Dynamic Media拡張機能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>文字方向： </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>のみ。ローマ字以外のフォントでは無視されます。<span class="codeph"> \stextflow1 </span>が有効でない場合は無視されます。 </p> <p>0垂直方向（デフォルト）。 </p> <p>1時計回りに90度回転しました。 </p> </td> 
  </tr> 
 </tbody> 
</table>
