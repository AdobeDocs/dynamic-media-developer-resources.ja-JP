---
description: このドキュメントでは、次の規則を使用します。
solution: Experience Manager
title: 文書規則
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: e93de3fa-dde1-4d79-93aa-9ad800840cfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# 文書規則{#document-conventions}

このドキュメントでは、次の規則を使用します。

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>literal </p> </td> 
  <td class="stentry"> <p>構文セクションでは、非斜体テキストはリテラルです。 この規則は、空白と記号[ ] { }には適用されません | *. </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> command=  </span> </p> </td> 
  <td class="stentry"> <p>末尾に「=」を持つ名前は、画像サービングのHTTPプロトコルコマンドを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">属性のプレフィックスが付いた名前：</span>は、画像カタログ属性を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">カタログのプレフィックスが付いた名前：</span>は、画像カタログデータフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> iccというプレフィックスが付いた名前：</span>は、ICCカラープロファイルマップのフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> font::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">フォントの前に次の名前が付いています。</span>は、フォントマップ内のフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> マクロ：項目  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">マクロの前に次の名前が付きます。</span>は、マクロ定義テーブルのフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item  </span> </p> </td> 
  <td class="stentry"> <p>先頭に<span class="codeph"> ruleset:：が付いた名前</span>は、URL前処理ルールセット内の要素を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">というプレフィックスが付いた名前：</span>は、デフォルトの画像カタログの属性を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [オプ <span class="varname"> ション </span>]  </span> </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は角括弧で囲みます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[オ <span class="varname"> プショ </span>ン]  </span> </p> </td> 
  <td class="stentry"> <p><span class="varname">オプションの</span>構文要素は、1回または複数回繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item1  </span>|  <span class="varname"> item2  </span> </span> </p> </td> 
  <td class="stentry"> <p>縦棒は、左側に単一の構文項目を使用できること、または右側に項目を使用できることを示します。 項目を1つだけ選択する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> {  <span class="varname"> group  </span>}  </span> </p> </td> 
  <td class="stentry"> <p>構文要素をグループ化するには波括弧を使用します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{  <span class="varname"> group  </span>}  </span> </p> </td> 
  <td class="stentry"> <p>グループ内の構文要素は1回以上繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>空白（スペースまたはタブ）は、HTTP要求では使用できません。 このドキュメントでは、構文要素間に空白を使用して明確にする場合のみがあります。 </p> </td> 
 </tr> 
</table>
