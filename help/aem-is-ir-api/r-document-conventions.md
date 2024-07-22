---
description: このドキュメントでは、次の規則を使用します。
solution: Experience Manager
title: ドキュメントの規則
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cc334766-544b-4d77-aa0e-4e509525cbaa
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# ドキュメントの規則{#document-conventions}

このドキュメントでは、次の規則を使用します。

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>リテラル </p> </td> 
  <td class="stentry"> <p>構文セクションでは、斜体でないテキストはリテラルです。これは、空白および記号 [ ] { } には適用されません | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'リテラル' </p> </td> 
  <td class="stentry"> <p>説明セクションでは、一重引用符で囲まれた斜体でないテキストはリテラルです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> パラメーター </span> </p> </td> 
  <td class="stentry"> <p>斜体は、実際の値に置き換える変数またはパラメーターを示します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> command= </span> </p> </td> 
  <td class="stentry"> <p>末尾に「=」を付けた名前は、画像サービス HTTP プロトコルコマンドを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 属性：:Item </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 属性：</span> というプレフィックスが付いた名前は、画像カタログ属性を参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog: </span> というプレフィックスが付いた名前は、画像カタログデータフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>先頭に「icc: </span>」 <span class="codeph"> 付いた名前は、ICC カラープロファイルマップ内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> font::Item </span> </p> </td> 
  <td class="stentry"> <p>フォントがプレフィックス <span class="codeph"> れた名前：</span> はフォントマップ内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> マクロ：：項目 </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> マクロが付いた名前：</span> はマクロ定義テーブルのフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ルールセット：:Item </span> </p> </td> 
  <td class="stentry"> <p>名前の先頭に <span class="codeph"> ルールセット：</span> というプレフィックスが付いた場合、URL 内の要素を参照して、ルールセットを前処理します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item </span> </p> </td> 
  <td class="stentry"> <p>デフォルト：<span class="codeph"> というプレフィックスが付いた名前 </span>、デフォルトの画像カタログの属性を参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [ <span class="varname"> optional </span>] </span> </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は角括弧で囲みます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[ <span class="varname"> オプション </span>] </span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> のオプションの </span> 構文要素は、まったく繰り返すことも、それ以上繰り返すこともできます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </span> </p> </td> 
  <td class="stentry"> <p>縦棒は、左側に単一構文のアイテム、または右側に単一構文のアイテムが使用可能であることを示します。 選択する項目は 1 つだけです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> { <span class="varname"> group </span>} </span> </p> </td> 
  <td class="stentry"> <p>中括弧は、構文要素をグループ化するために使用されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{ <span class="varname"> group </span>} </span> </p> </td> 
  <td class="stentry"> <p>グループ内の構文要素は、1 回以上繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>HTTP リクエストでは、空白（スペースまたはタブ）は使用できません。 このドキュメントでは、分かりやすくするために、構文要素の間に空白を使用する場合があります。 </p> </td> 
 </tr> 
</table>
