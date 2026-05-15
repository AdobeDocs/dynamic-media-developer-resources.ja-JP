---
description: このドキュメントでは、次の規則を使用します。
solution: Experience Manager
title: ドキュメント規則
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e93de3fa-dde1-4d79-93aa-9ad800840cfc
TQID: 'https://experienceleague.adobe.com/NuClwLkfN7-tuVMYcn610qL7-bQOQbVz940uTPAxk-g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 283
ht-degree: 0%

---

# ドキュメント規則{#document-conventions}

このドキュメントでは、次の規則を使用します。

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>リテラル </p> </td> 
  <td class="stentry"> <p>構文セクションでは、イタリック以外のテキストはリテラルです。 このルールは、空白および記号[ ] { } | *には適用されません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'リテラル' </p> </td> 
  <td class="stentry"> <p>記述的なセクションでは、単引用符の非イタリックのテキストはリテラルです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> パラメーター</span> </p> </td> 
  <td class="stentry"> <p>斜体は、実際の値で置き換える変数またはパラメーターを示します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> コマンド= </span> </p> </td> 
  <td class="stentry"> <p>末尾に「=」が付いた名前は、Image Serving HTTP Protocol コマンドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">属性：：項目</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">属性のプレフィックスが付いた名前：</span>は、画像カタログ属性を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> カタログ：：項目</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> カタログのプレフィックスが付いた名前：</span>は、画像カタログデータフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc:：項目</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> icc:: </span>というプレフィックスが付いた名前は、ICC カラープロファイルマップのフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> フォント：：項目</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> フォントのプレフィックスが付いた名前：</span>は、フォントマップ内のフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> マクロ：: アイテム </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> マクロのプレフィックスが付いた名前：</span>は、マクロ定義テーブルのフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ルールセット：：項目</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> ルールセットのプレフィックスが付いた名前：</span>は、URL前処理ルールセット内の要素を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">の既定値：：項目</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> default: </span>というプレフィックスが付いた名前は、デフォルトの画像カタログの属性を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [ <span class="varname"> オプション </span>] </span> </p> </td> 
  <td class="stentry"> <p>オプションの構文エレメントは、角括弧で囲まれます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[<span class="varname"> オプション </span>] </span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> オプションの</span>構文エレメントは、何も繰り返すことはできません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </span> </p> </td> 
  <td class="stentry"> <p>縦棒グラフは、左側の単一の構文アイテムまたは右側のアイテムのいずれかを使用できることを示します。 1つの項目を選択してください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> { <span class="varname"> グループ </span>} </span> </p> </td> 
  <td class="stentry"> <p>中括弧は、構文エレメントをグループ化するために使用されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{ <span class="varname"> グループ </span>} </span> </p> </td> 
  <td class="stentry"> <p>グループ内の構文要素は、1回以上繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>HTTP リクエストでは、空白（スペースまたはタブ）は使用できません。 このドキュメントでは、構文要素の間に空白が表示されることがあります。 </p> </td> 
 </tr> 
</table>
