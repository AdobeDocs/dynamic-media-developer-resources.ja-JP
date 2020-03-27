---
description: このドキュメントでは、次の規則を使用します。
seo-description: このドキュメントでは、次の規則を使用します。
seo-title: 文書の規則
solution: Experience Manager
title: 文書の規則
topic: Scene7 Image Serving - Image Rendering API
uuid: c929774b-8560-4f8a-98fd-1b75d4419c4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Document conventions{#document-conventions}

このドキュメントでは、次の規則を使用します。

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>リテラル </p> </td> 
  <td class="stentry"> <p>構文セクションでは、斜体以外のテキストはリテラルです。これは、空白と記号[ ] { }には適用されません| *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>説明的なセクションでは、一重引用符内の斜体以外のテキストはリテラルです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> パラメータ </span> </p> </td> 
  <td class="stentry"> <p>斜体は、実際の値で置き換えられる変数またはパラメータを示します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> command= </span> </p> </td> 
  <td class="stentry"> <p>末尾に「=」が付いた名前は、画像サービングHTTPプロトコルコマンドを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>属性の前に次のような名前 <span class="codeph"> が付きます。は、画 </span> 像カタログ属性を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item </span> </p> </td> 
  <td class="stentry"> <p>名前の先頭にcatalog：と <span class="codeph"> いう名前が付きます。は、画 </span> 像カタログデータフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>名前の先頭に <span class="codeph"> icc:は、ICC </span> カラープロファイルマップ内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> font::Item </span> </p> </td> 
  <td class="stentry"> <p>名前の先頭に <span class="codeph"> font:は、フ </span> ォントマップ内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> マクロ：項目 </span> </p> </td> 
  <td class="stentry"> <p>名前の先頭にマクロを付 <span class="codeph"> けます。は、マ </span> クロ定義テーブル内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item </span> </p> </td> 
  <td class="stentry"> <p>名前の先頭にルールセットが <span class="codeph"> 付きます：は、 </span> URLの事前処理ルールセット内の要素を参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item </span> </p> </td> 
  <td class="stentry"> <p>名前の先頭にデフォル <span class="codeph"> トを付けます。は、 </span> 初期設定の画像カタログの属性を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [オプ <span class="varname"> ション </span>] </span> </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は角括弧で囲みます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[オプ <span class="varname"> ション </span>] </span> </p> </td> 
  <td class="stentry"> <p>オプション <span class="varname"> の構 </span> 文要素は、何も繰り返さないことも、複数回繰り返すこともできます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item1 </span>| <span class="varname"> item2 </span></span> </p> </td> 
  <td class="stentry"> <p>縦棒グラフは、左側の単一の構文項目または右側の構文項目のどちらかが使用できることを示します。 項目を1つだけ選択する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> { <span class="varname"> group </span>} </span> </p> </td> 
  <td class="stentry"> <p>中括弧は、構文要素をグループ化するために使用します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{ <span class="varname"> group </span>} </span> </p> </td> 
  <td class="stentry"> <p>グループ内の構文要素は、1回以上繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>HTTPリクエストでは空白（スペースまたはタブ）は使用できません。 この文書では、明確にするために、構文要素間に空白文字が使用されることがあります。 </p> </td> 
 </tr> 
</table>

