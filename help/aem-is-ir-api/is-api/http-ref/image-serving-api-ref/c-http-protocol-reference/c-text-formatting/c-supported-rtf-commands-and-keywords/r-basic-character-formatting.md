---
description: 基本的な文字書式設定には、次のコマンドを使用します。
solution: Experience Manager
title: 基本的な文字書式
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: d3bd6d4d-d7bd-4c9b-bc9e-7edaaac6378e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 8%

---

# 基本的な文字書式{#basic-character-formatting}

基本的な文字書式設定には、次のコマンドを使用します。

<table id="table_65415B84652F4E7497299AD90AE7C191"> 
 <thead> 
  <tr> 
   <th class="entry"> コマンド </th> 
   <th class="entry"> 説明 </th> 
   <th class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \プレーン </span> </td> 
   <td> <p>文字書式をデフォルトにリセット </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f  <span class="varname"> N  </span> </span> </td> 
   <td> <p>フォント </p> </td> 
   <td> <p> <span class="codeph"> \fonttblインデ </span> ックス。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs  <span class="varname"> N  </span> </span> </td> 
   <td> <p>フォントサイズ </p> </td> 
   <td> <p>ハーフポイント初期設定は24です。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf  <span class="varname"> N  </span> </span> </td> 
   <td> <p>フォントカラー. </p> </td> 
   <td> <p>0を基準とするカラーテーブルのインデックス </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b </span> </td> 
   <td> <p>太字スタイル。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i </span> </td> 
   <td> <p>斜体スタイル。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub  </span> </td> 
   <td> <p>下付き文字. </p> </td> 
   <td> <p>フォントサイズを縮小します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super  </span> </td> 
   <td> <p>上付き文字. </p> </td> 
   <td> <p>フォントサイズを縮小します。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul  </span> </td> 
   <td> <p>下線 </p> </td> 
   <td> <p>画像サービングでは、次のRTF下線コマンドも認識されます。 </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \uld  </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uldash  </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd  </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashd  </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb  </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \ulth  </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \ulw  </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave  </span> </li> 
     </ul> </p> <p>これらは、現時点では標準の<span class="codeph"> \ul </span>下線として実装されます。 その他のRTF下線付きコマンドは無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnone  </span> </td> 
   <td> <p>下線を引く </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0  </span> </td> 
   <td> <p>下線を引く </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \キャップス </span> </td> 
   <td> <p>大文字 </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps  </span> </td> 
   <td> <p>小文字（「小文字」） </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み。 </p> </td> 
  </tr> 
 </tbody> 
</table>
