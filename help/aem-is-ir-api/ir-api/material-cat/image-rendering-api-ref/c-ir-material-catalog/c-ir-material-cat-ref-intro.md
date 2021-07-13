---
description: このドキュメントでは、Dynamic Media Image Renderingのマテリアルカタログについて説明します。
solution: Experience Manager
title: はじめに
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 1cdb9c45-329d-44df-92c3-8cba5b2b1339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---

# はじめに{#introduction}

このドキュメントでは、Dynamic Media Image Renderingのマテリアルカタログについて説明します。

**対象読者**

このドキュメントは、WebサイトやカスタムアプリケーションでDynamic Media Image Renderingを活用したい経験豊富なプログラマーやWebサイト開発者を対象としています。

このドキュメントでは、Dynamic Media Image Authoring and Image Rendering、一般的なHTTPプロトコルの標準と規則、基本的な画像の用語について詳しい読者を想定しています。

**文書規則**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>リテラル </p> </td> 
  <td class="stentry"> <p>構文セクションでは、非斜体はリテラルです。これは、空白と記号[ ] { }には適用されません。 | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>説明セクションでは、一重引用符で囲まれた非斜体のテキストはリテラルです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> パラメータ </span> </p> </td> 
  <td class="stentry"> <p>斜体の部分には実際の値で置き換えられる変数またはパラメーターが表示されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item  </span> </p> </td> 
  <td class="stentry"> <p>「attribute::」というプレフィックスが付いた名前は、画像カタログ属性を表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> catalog::Item  </span> </td> 
  <td class="stentry"> <p>プレフィックス「catalog::」が付いた名前は、マテリアルカタログデータフィールドを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>プレフィックス「icc::」が付いた名前は、ICCカラープロファイルマップ内のフィールドを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro:::Item  </span> </p> </td> 
  <td class="stentry"> <p>「macro::」というプレフィックスが付いた名前は、マクロ定義テーブル内のフィールドを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item  </span> </p> </td> 
  <td class="stentry"> <p>プレフィックス「ruleset::」が付いた名前は、URL前処理ルールセット内の要素を表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item  </span> </p> </td> 
  <td class="stentry"> <p>プレフィックス「default:::」が付いた名前は、デフォルトの画像カタログの属性を表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> vignette::Item  </span> </p> </td> 
  <td class="stentry"> <p>「vignette::」というプレフィックスが付いた名前は、ビネットマップ内のフィールドを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname">オプション</span> ] </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は角括弧で囲みます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname">オプション</span> ] </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は、1回または複数回繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1  </span>|  <span class="varname"> item2  </span> </p> </td> 
  <td class="stentry"> <p>縦棒は、左側に単一の構文項目を指定するか、右側に項目を指定するかを示します。 項目を1つだけ選択する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> グループ </span> } </p> </td> 
  <td class="stentry"> <p>構文要素をグループ化するには波括弧を使用します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> グループ </span> } </p> </td> 
  <td class="stentry"> <p>グループ内の構文要素は、1回または複数回繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白。 </p> </td> 
  <td class="stentry"> <p>空白（スペースまたはタブ）は、HTTP要求では使用できません。 このドキュメントでは、構文要素間に空白を使用して明確にする場合のみがあります。 </p> </td> 
 </tr> 
</table>
