---
title: はじめに
description: ここでは、Dynamic Media 画像レンダリングの HTTP プロトコルについて説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# はじめに{#introduction}

ここでは、Dynamic Media 画像レンダリングの HTTP プロトコルについて説明します。

公開されているプロトコルの側面のみが記載されています。 サーバーは、Dynamic Media クライアントソフトウェアで使用するために予約されている追加のコマンドをサポートする場合があります。

**対象オーディエンス**

このドキュメントは、Web サイトまたはカスタムアプリケーションに Dynamic Media 画像レンダリングを使用する、経験豊富なプログラマーおよび Web サイト開発者を対象としています。

Dynamic Media の画像オーサリングと画像レンダリング、一般的な HTTP プロトコルの標準と規則、基本的な画像用語について、読者が熟知していることを前提としています。

**ドキュメント規則**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>リテラル </p> </td> 
  <td class="stentry"> <p>構文セクションでは、斜体でないテキストはリテラルです。空白および記号 [ ] { } には適用されません | *. </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> 属性：:Item </span> </p> </td> 
  <td class="stentry"> <p>先頭に「attribute::」が付く名前は、画像カタログ属性を参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item </span> </p> </td> 
  <td class="stentry"> <p>先頭に「catalog::」が付いた名前は、材料カタログデータフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>先頭に「icc::」が付いた名前は、ICC カラープロファイルマップのフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item </span> </p> </td> 
  <td class="stentry"> <p>「macro::」というプレフィックスが付いた名前は、マクロ定義テーブルのフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ルールセット：:Item </span> </p> </td> 
  <td class="stentry"> <p>プレフィックス「ruleset::」が付いた名前は、URL 内の要素を前処理ルールセットとして参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item </span> </p> </td> 
  <td class="stentry"> <p>先頭に「default::」が付く名前は、デフォルトの画像カタログの属性を参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> vignette::Item </span> </td> 
  <td class="stentry"> <p>先頭に「vignette::」が付く名前は、ビネットマップ内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> オプション </span> ] </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は角括弧で囲みます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> オプション </span> ] </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は、まったく繰り返すことも、それ以上繰り返すこともできます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </p> </td> 
  <td class="stentry"> <p>縦棒は、左側に単一構文のアイテム、または右側に単一構文のアイテムが使用可能であることを示します。 選択する項目は 1 つだけです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> group </span> } </p> </td> 
  <td class="stentry"> <p>中括弧は、構文要素をグループ化するために使用されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> group </span> } </p> </td> 
  <td class="stentry"> <p>グループ内の構文要素は、1 回以上繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>HTTP リクエストでは、空白（スペースまたはタブ）は使用できません。 このドキュメントでは、分かりやすくするために、構文要素の間に空白を使用する場合があります。 </p> </td> 
 </tr> 
</table>

**一般用語**

**&#x200B; *`MSS`* &#x200B;** Material Specification Segment：要求内の 2 つの選択コマンド間の材料属性のセット。

**&#x200B; *`vignette`* &#x200B;** Dynamic Media 画像オーサリングで画像レンダリングと共に使用するために準備された画像。
