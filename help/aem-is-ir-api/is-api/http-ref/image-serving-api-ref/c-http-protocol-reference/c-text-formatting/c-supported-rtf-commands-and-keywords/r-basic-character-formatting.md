---
description: 基本的な文字形式設定を行うには、次のコマンドを使用します。
seo-description: 基本的な文字形式設定を行うには、次のコマンドを使用します。
seo-title: 基本的な文字の形式設定
solution: Experience Manager
title: 基本的な文字の形式設定
topic: Scene7 Image Serving - Image Rendering API
uuid: cc8f276a-ebcc-479b-bd86-7ac0dc755f11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 8%

---


# 基本文字の書式設定{#basic-character-formatting}

基本的な文字形式設定を行うには、次のコマンドを使用します。

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
   <td> <p> <span class="codeph"> textPs= </span> のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f  <span class="varname"> N  </span> </span> </td> 
   <td> <p>フォント </p> </td> 
   <td> <p> <span class="codeph"> \fonttbl </span> インデックス </p> </td> 
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
   <td> <p>太字スタイル </p> </td> 
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
   <td> <p>フォントサイズを小さくします。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super  </span> </td> 
   <td> <p>上付き文字. </p> </td> 
   <td> <p>フォントサイズを小さくします。 </p> </td> 
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
     </ul> </p> <p>これらは、現時点では標準の<span class="codeph"> \ul </span>下線として実装されています。 その他のRTF下線コマンドはすべて無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnone  </span> </td> 
   <td> <p>下線をオフにする </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0  </span> </td> 
   <td> <p>下線をオフにする </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \キャップス </span> </td> 
   <td> <p>大文字 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps  </span> </td> 
   <td> <p>小文字（「スモールキャップス」） </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

