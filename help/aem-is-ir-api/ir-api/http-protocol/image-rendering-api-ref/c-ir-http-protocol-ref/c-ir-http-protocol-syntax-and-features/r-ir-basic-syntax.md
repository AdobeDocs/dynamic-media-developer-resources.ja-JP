---
description: この節では、Dynamic MediaイメージレンダリングHTTPプロトコルの基本的な構文を説明します。
solution: Experience Manager
title: イメージレンダリングHTTPプロトコルの基本構文
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---


# イメージレンダリングHTTPプロトコル基本構文{#image-rendering-http-protocol-basic-syntax}

この節では、Dynamic MediaイメージレンダリングHTTPプロトコルの基本的な構文を説明します。

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
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> 修飾子</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> ビネット  </span> </p> </td> 
   <td colname="col2"> <p>ビネット指定子（相対ファイルパスまたはビネットカタログエントリ） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾子 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp;  <span class="varname"> modifier</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾子 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $  <span class="varname"> macro</span> $ } | { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro  </span> </p> </td> 
   <td colname="col2"> <p>コマンドマクロの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> コメント  </span> </p> </td> 
   <td colname="col2"> <p>コメント文字列（サーバーでは無視されます）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName  </span> </p> </td> 
   <td colname="col2"> <p>コマンドまたは属性の名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>カスタム変数の名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> value  </span> </p> </td> 
   <td colname="col2"> <p>コマンドまたは変数の値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*、、 *`cmdName`*、 *`macro`*&#x200B;およびは大文字と小文字が区別されま *`var`* せん。サーバーは、大文字と小文字を区別し、他の文字列値もすべて保持します。

**サーバー識別子**

イメージレンダリングへのすべてのHTTP要求には、「`/ir/render`」ルートコンテキストが必要です。

**コメント**

コメントはリクエスト文字列のどこにでも埋め込むことができ、ピリオド(.)で識別します。 コマンド区切り文字(&amp;)の直後。 コメントは、次に（エンコードされていない）コマンドセパレータが出現すると終了します。 この機能は、タイムスタンプ、データベースIDなど、画像サービングで使用されない情報を要求に追加する場合に使用します。

**HTTPデコード**

画像レンダリングは、最初に、受信要求から&#x200B;*`object`*&#x200B;と&#x200B;*`modifiers`*&#x200B;を抽出します。 *`object`* は、個別にHTTPデコードされるパス要素に分割されます。*`modifiers`*&#x200B;文字列は&#x200B;*`command`*= *`value`*&#x200B;ペアに区切られ、*`value`*&#x200B;はコマンド固有の処理の前にHTTPデコードされます。
