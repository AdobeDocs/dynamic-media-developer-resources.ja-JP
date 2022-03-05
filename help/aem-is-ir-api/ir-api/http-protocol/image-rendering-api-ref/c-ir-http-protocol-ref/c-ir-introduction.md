---
title: はじめに
description: このドキュメントでは、Dynamic Media Image Rendering の HTTP プロトコルについて説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---

# はじめに{#introduction}

このドキュメントでは、Dynamic Media Image Rendering の HTTP プロトコルについて説明します。

プロトコルの公開されている側面のみが記述されます。 サーバーは、Dynamic Mediaクライアントソフトウェアで使用するために予約されている追加のコマンドをサポートする場合があります。

**対象オーディエンス**

このドキュメントは、Web サイトやカスタムアプリケーションでDynamic Media Image Rendering を使用する経験豊富なプログラマーや Web サイト開発者を対象としています。

この読者は、Dynamic Media Image Authoring and Image Rendering、一般的な HTTP プロトコルの標準と規則、基本的な画像の用語に精通していることを前提としています。

**文書の規則**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>literal </p> </td> 
  <td class="stentry"> <p>構文セクションでは、非斜体テキストはリテラルです。空白と記号 [ ] { } には適用されません | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>説明セクションでは、一重引用符で囲まれた非斜体テキストはリテラルです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> パラメータ </span> </p> </td> 
  <td class="stentry"> <p>斜体の部分には、実際の値で置き換えられる変数またはパラメーターが表示されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>「attribute::」というプレフィックスが付いた名前は、画像カタログ属性を表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item </span> </p> </td> 
  <td class="stentry"> <p>「catalog::」というプレフィックスが付いた名前は、マテリアルカタログデータフィールドを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>プレフィックス「icc::」が付いた名前は、ICC カラープロファイルマップ内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro:::Item </span> </p> </td> 
  <td class="stentry"> <p>「macro:::」というプレフィックスが付いた名前は、マクロ定義テーブル内のフィールドを参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item </span> </p> </td> 
  <td class="stentry"> <p>「ruleset::」というプレフィックスが付いた名前は、URL の前処理ルールセット内の要素を参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default:::Item </span> </p> </td> 
  <td class="stentry"> <p>プレフィックス「default::」が付いた名前は、デフォルトの画像カタログの属性を参照します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> vignette::Item </span> </td> 
  <td class="stentry"> <p>「vignette::」というプレフィックスが付いた名前は、ビネットマップ内のフィールドを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> オプション </span> ] </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は角括弧で囲みます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> オプション </span> ] </p> </td> 
  <td class="stentry"> <p>オプションの構文要素は、1 回も繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </p> </td> 
  <td class="stentry"> <p>縦棒は、左側の単一の構文項目または右側の項目のどちらかが使用できることを示します。 項目を 1 つだけ選択する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> グループ </span> } </p> </td> 
  <td class="stentry"> <p>中括弧は、構文要素をグループ化するために使用します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> グループ </span> } </p> </td> 
  <td class="stentry"> <p>グループ内の構文要素は、1 回以上繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>空白（スペースまたはタブ）は、HTTP リクエストでは使用できません。 このドキュメントでは、構文要素間に空白を使用して明確にするだけです。 </p> </td> 
 </tr> 
</table>

**一般用語**

** *`MSS`* **材料仕様セグメント：リクエスト内の 2 つの選択コマンド間のマテリアル属性のセット。

** *`vignette`* ** Dynamic Media Image Authoring で画像レンダリングで使用するために準備された画像。
