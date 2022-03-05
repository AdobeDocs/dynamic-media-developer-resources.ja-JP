---
title: 画像レンダリング HTTP プロトコルの基本構文
description: この節では、Dynamic Media Image Rendering HTTP プロトコルの基本構文について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 4%

---

# 画像レンダリング HTTP プロトコルの基本構文{#image-rendering-http-protocol-basic-syntax}

この節では、Dynamic Media Image Rendering HTTP プロトコルの基本構文について説明します。

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>項目 </p> </th> 
   <th colname="col2" class="entry"> <p>定義 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> リクエスト</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> ビネット</span> ] [ ?<span class="varname"> 修飾子</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> ポート</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> ビネット </span> </p> </td> 
   <td colname="col2"> <p>ビネット指定子（相対ファイルパスまたはビネットカタログエントリ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾子 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 修飾子</span> *[ &amp; <span class="varname"> 修飾子</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾子 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $ <span class="varname"> マクロ</span> $ } | { .<span class="varname"> コメント</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> 値</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> マクロ </span> </p> </td> 
   <td colname="col2"> <p>コマンドマクロの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> コメント </span> </p> </td> 
   <td colname="col2"> <p>コメント文字列（サーバーで無視）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>コマンドまたは属性の名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>カスタム変数の名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 値 </span> </p> </td> 
   <td colname="col2"> <p>コマンドまたは変数の値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`*、および *`var`* は大文字と小文字を区別しません。 サーバーは他のすべての文字列値の大文字と小文字を区別します。

**サーバー識別子**

&#39; `/ir/render`「 」ルートコンテキストは、画像レンダリングへのすべての HTTP リクエストに必要です。

**コメント**

コメントは、リクエスト文字列の任意の場所に埋め込むことができ、ピリオド (.) で識別されます。 コマンド区切り文字 (&amp;) の直後に表示されます。 コメントは、（エンコードされていない）コマンド区切り文字が次に出現すると終了します。 この機能を使用して、タイムスタンプやデータベース ID など、画像サービングでは使用しない情報を要求に追加できます。

**HTTP デコード**

画像レンダリングの最初の抽出 *`object`* および *`modifiers`* を呼び出します。 この *`object`* 次に、が個別に HTTP デコードされたパス要素に分割されます。 この *`modifiers`* 文字列が *`command`*= *`value`* ペアと *`value`* は、コマンド固有の処理の前に HTTP デコードされます。
