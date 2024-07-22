---
title: 画像レンダリングの HTTP プロトコル基本構文
description: ここでは、Dynamic Media画像レンダリング HTTP プロトコルの基本構文について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# 画像レンダリングの HTTP プロトコル基本構文{#image-rendering-http-protocol-basic-syntax}

ここでは、Dynamic Media画像レンダリング HTTP プロトコルの基本構文について説明します。

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>項目 </p> </th> 
   <th colname="col2" class="entry"> <p>定義 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 要求 </span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> 修飾子 </span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> ヴィネット </span> </p> </td> 
   <td colname="col2"> <p>ビネット指定子（相対ファイルパスまたはビネットカタログエントリ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾子 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 修飾子 </span> *[ &amp; <span class="varname"> 修飾子 </span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾子 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> コマンド </span> | { $ <span class="varname"> マクロ </span> $ } | {。<span class="varname"> コメント </span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> 値 </span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> マクロ </span> </p> </td> 
   <td colname="col2"> <p>コマンド マクロの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comment </span> </p> </td> 
   <td colname="col2"> <p>コメント文字列（サーバーでは無視されます）。 </p> </td> 
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
   <td colname="col2"> <p>コマンドまたは変数値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*、*`cmdName`*、*`macro`*、*`var`* では、大文字と小文字が区別されません。 サーバーは、他のすべての文字列値の大文字と小文字を区別しません。

**サーバー識別子**

画像レンダリングへのすべての HTTP リクエストにルートコンテキスト「`/ir/render`」が必要です。

**コメント**

コメントは、任意の場所のリクエスト文字列に埋め込むことができ、ピリオド（.）で識別されます。 コマンド区切り記号（&amp;）の直後 コメントは、（エンコードされていない）コマンド区切り記号が次に現れることによって終了します。 この機能は、画像サービング以外の情報（タイムスタンプ、データベース ID など）をリクエストに追加するために使用できます。

**HTTP デコード**

画像レンダリングでは、まず受信リクエストから *`object`* と *`modifiers`* を抽出します。 次に、*`object`* はパス要素に分割され、各パス要素は個別に HTTP デコードされます。 *`modifiers`* の文字列は *`command`*= *`value`* ペアに分割され、*`value`* の後、コマンド固有の処理の前に HTTP デコードされます。
