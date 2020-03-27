---
description: このドキュメントでは、Scene7画像レンダリングのHTTPプロトコルについて説明します。
seo-description: このドキュメントでは、Scene7画像レンダリングのHTTPプロトコルについて説明します。
seo-title: はじめに
solution: Experience Manager
title: はじめに
topic: Scene7 Image Serving - Image Rendering API
uuid: d709f1d2-e7cc-4e9f-b039-aa333e517cbb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# はじめに{#introduction}

このドキュメントでは、Scene7画像レンダリングのHTTPプロトコルについて説明します。

プロトコルの公開された側面のみが記述されます。 サーバは、Scene7クライアントソフトウェアで使用するために予約されている追加のコマンドをサポートする場合があります。

**対象読者**

このドキュメントは、WebサイトやカスタムアプリケーションでScene7画像レンダリングを利用したい経験豊富なプログラマやWebサイト開発者を対象としています。

読者は、Scene7 Image AuthoringとImage Rendering、一般的なHTTPプロトコル標準と表記、基本的な画像処理の用語に精通していることを前提としています。

**文書の規則**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
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
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>「attribute::」というプリフィックスが付いた名前は、画像カタログ属性を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item </span> </p> </td> 
  <td class="stentry"> <p>「catalog::」というプリフィックスが付いた名前は、マテリアルカタログデータフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>「icc::」というプリフィックスが付いた名前は、ICCカラープロファイルマップ内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item </span> </p> </td> 
  <td class="stentry"> <p>「macro::」というプリフィックスが付いた名前は、マクロ定義テーブル内のフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item </span> </p> </td> 
  <td class="stentry"> <p>「ruleset::」というプリフィックスが付いた名前は、URLの事前処理ルールセット内の要素を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item </span> </p> </td> 
  <td class="stentry"> <p>「default::」というプリフィックスが付いた名前は、初期設定の画像カタログの属性を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> ビネット：:Item </span> </td> 
  <td class="stentry"> <p>名前の先頭に「vignette::」という文字が付いている場合は、ビネットマップ内のフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は角括弧で囲みます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は、1回以上繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </p> </td> 
  <td class="stentry"> <p>縦棒グラフは、左側の単一の構文項目または右側の構文項目のどちらかが使用できることを示します。 項目を1つだけ選択する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> グループ </span> } </p> </td> 
  <td class="stentry"> <p>中括弧は、構文要素をグループ化するために使用します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> グループ </span> } </p> </td> 
  <td class="stentry"> <p>グループ内の構文要素は、1回以上繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>HTTPリクエストでは空白（スペースまたはタブ）は使用できません。 この文書では、明確にするために、構文要素間に空白文字が使用されることがあります。 </p> </td> 
 </tr> 
</table>

**一般用語**

** *`MSS`* **材料仕様セグメント：リクエスト内の2つの選択コマンド間のマテリアル属性のセット。

** *`vignette`* ** Scene7 Image Authoringで画像レンダリング用に準備された画像。
