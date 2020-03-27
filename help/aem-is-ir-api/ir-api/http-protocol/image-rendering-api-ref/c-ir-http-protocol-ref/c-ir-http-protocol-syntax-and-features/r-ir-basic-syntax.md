---
description: この節では、Scene7画像レンダリングHTTPプロトコルの基本的な構文について説明します。
seo-description: この節では、Scene7画像レンダリングHTTPプロトコルの基本的な構文について説明します。
seo-title: イメージレンダリングHTTPプロトコルの基本構文
solution: Experience Manager
title: イメージレンダリングHTTPプロトコルの基本構文
topic: Scene7 Image Serving - Image Rendering API
uuid: e01314f0-6aaa-41ca-8c05-d5db3148a071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# イメージレンダリングHTTPプロトコルの基本構文{#image-rendering-http-protocol-basic-syntax}

この節では、Scene7画像レンダリングHTTPプロトコルの基本的な構文について説明します。

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
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/vignette<span class="varname"></span> ] [ ?<span class="varname"> 修飾子</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> ビネット </span> </p> </td> 
   <td colname="col2"> <p>ビネット指定子（相対ファイルパスまたはビネットカタログエントリ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾子 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp; <span class="varname"> modifier</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾子 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $ <span class="varname"> macro</span> $ }| { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> マクロ </span> </p> </td> 
   <td colname="col2"> <p>コマンドマクロの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> コメント </span> </p> </td> 
   <td colname="col2"> <p>コメント文字列（サーバーでは無視）。 </p> </td> 
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
   <td colname="col1"> <p><span class="varname"> value </span> </p> </td> 
   <td colname="col2"> <p>コマンドまたは変数の値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*、、およ *`cmdName`*&#x200B;びは大 *`macro`*&#x200B;文字と小 *`var`* 文字が区別されません。 サーバーは、他のすべての文字列値の大文字と小文字の区別を保持します。

**サーバー識別子**

イメージレンダ `/ir/render`リングに対するすべてのHTTP要求には、「」ルートコンテキストが必要です。

**コメント**

コメントは、任意の場所でリクエスト文字列に埋め込むことができ、ピリオド(.)で識別されます。コマンド区切り文字(&amp;)の直後。 コメントは、次に（エンコードされていない）コマンド区切り文字が出現するたびに終了します。 この機能は、タイムスタンプ、データベースIDなど、画像サービングで使用されない情報を要求に追加する場合に使用します。

**HTTPデコード**

画像レンダリングは、最初 *`object`* に要求を *`modifiers`* 抽出し、その要求から抽出します。 *`object`* が個別にHTTPデコードされるパス要素に分割されます。 文字列 *`modifiers`* は、 *`command`*=のペアに分けら *`value`* れ、コマ *`value`* ンド固有の処理の前にHTTPデコードされます。
