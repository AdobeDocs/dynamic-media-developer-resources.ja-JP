---
description: このドキュメントでは、Dynamic MediaイメージレンダリングのHTTPプロトコルについて説明します。
solution: Experience Manager
title: はじめに
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---


# はじめに{#introduction}

このドキュメントでは、Dynamic MediaイメージレンダリングのHTTPプロトコルについて説明します。

プロトコルの公開された側面のみが説明されます。 サーバは、Dynamic Media・クライアント・ソフトウェアが使用するために予約した追加のコマンドをサポートする場合があります。

**対象オーディエンス**

このドキュメントは、WebサイトやカスタムアプリケーションでDynamic Media画像レンダリングを利用したい経験豊富なプログラマーやWebサイト開発者向けです。

このガイドでは、読者が、Dynamic Media画像オーサリングと画像レンダリング、一般的なHTTPプロトコル標準および表記、基本的な画像処理用語に精通していることを前提としています。

**ドキュメント規則**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
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
  <td class="stentry"> <p> <span class="codeph"> attribute::Item  </span> </p> </td> 
  <td class="stentry"> <p>「attribute::」というプリフィックスの付いた名前は、画像カタログ属性を参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item  </span> </p> </td> 
  <td class="stentry"> <p>「catalog::」というプリフィックスが付いた名前は、マテリアルカタログデータフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>「icc:」というプリフィックスが付いた名前は、ICCカラープロファイルマップ内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item  </span> </p> </td> 
  <td class="stentry"> <p>「macro::」というプリフィックスが付いた名前は、マクロ定義テーブル内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item  </span> </p> </td> 
  <td class="stentry"> <p>「ruleset::」というプリフィックスが付いた名前は、URLの事前処理ルールセット内の要素を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item  </span> </p> </td> 
  <td class="stentry"> <p>「default::」というプリフィックスの付いた名前は、初期設定の画像カタログの属性を参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> vignette::Item  </span> </td> 
  <td class="stentry"> <p>「vignette::」というプリフィックスが付いた名前は、ビネットマップ内のフィールドを指します。 </p> </td> 
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
  <td class="stentry"> <p>縦棒グラフは、左側に1つの構文項目、または右側に1つの項目を使用できることを示します。 項目を1つだけ選択する必要があります。 </p> </td> 
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
  <td class="stentry"> <p>HTTPリクエストでは、空白（スペースまたはタブ）は使用できません。 このドキュメントでは、構文要素間に空白文字が使用されることがあります。構文上の要素は明確化のためだけです。 </p> </td> 
 </tr> 
</table>

**一般用語**

** *`MSS`* **材料仕様セグメント：リクエスト内の2つの選択コマンド間のマテリアル属性のセット。

** *`vignette`* **Dynamic Media画像オーサリングで画像レンダリング用に準備された画像。
