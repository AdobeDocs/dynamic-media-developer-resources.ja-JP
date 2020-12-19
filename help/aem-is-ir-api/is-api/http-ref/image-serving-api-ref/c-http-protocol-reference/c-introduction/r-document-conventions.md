---
description: このドキュメントでは、次の規則を使用します。
seo-description: このドキュメントでは、次の規則を使用します。
seo-title: ドキュメント規則
solution: Experience Manager
title: ドキュメント規則
topic: Scene7 Image Serving - Image Rendering API
uuid: c929774b-8560-4f8a-98fd-1b75d4419c4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---


# ドキュメント規則{#document-conventions}

このドキュメントでは、次の規則を使用します。

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>リテラル </p> </td> 
  <td class="stentry"> <p>構文セクションでは、斜体以外のテキストはリテラルです。これは、空白と記号[ ] { }には適用されません | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>説明セクションでは、一重引用符で囲まれた斜体以外のテキストはリテラルです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> パラメータ </span> </p> </td> 
  <td class="stentry"> <p>斜体は、実際の値で置き換えられる変数またはパラメーターを示します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> command=  </span> </p> </td> 
  <td class="stentry"> <p>末尾に「=」を付けた名前は、画像サービングのHTTPプロトコルコマンドを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">属性の前に付ける名前：</span>は、画像カタログ属性を参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">カタログの前に次の名前が付きます。</span>は、画像カタログデータフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> iccというプリフィックスが付いた名前：</span>は、ICCカラープロファイルマップ内のフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> font::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">フォントの前に次のような名前が付きます。</span>は、フォントマップ内のフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro:項目  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">マクロの前に次のような名前が付けられます。</span>は、マクロ定義テーブル内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">ルールセットの前に付く名前：</span>は、URLの事前処理ルールセット内の要素を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">というプリフィックスが付いた名前がデフォルトで次のようになります。</span>は、初期設定の画像カタログの属性を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [ <span class="varname"> オプション </span>]  </span> </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は角括弧で囲みます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[ <span class="varname"> オプション </span>]  </span> </p> </td> 
  <td class="stentry"> <p><span class="varname">オプションの</span>構文要素は、1回または複数回繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item1  </span>|  <span class="varname"> item2  </span> </span> </p> </td> 
  <td class="stentry"> <p>縦棒グラフは、左側に1つの構文項目、または右側に1つの項目を使用できることを示します。 項目を1つだけ選択する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> {  <span class="varname"> group  </span>}  </span> </p> </td> 
  <td class="stentry"> <p>中括弧は、構文要素をグループ化するために使用します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{  <span class="varname"> group  </span>}  </span> </p> </td> 
  <td class="stentry"> <p>グループ内の構文要素は、1回以上繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>HTTPリクエストでは、空白（スペースまたはタブ）は使用できません。 このドキュメントでは、構文要素間に空白文字が使用されることがあります。構文上の要素は明確化のためだけです。 </p> </td> 
 </tr> 
</table>

