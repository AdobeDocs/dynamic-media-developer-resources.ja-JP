---
description: この節では、Dynamic Media Image Rendering HTTPプロトコルの基本構文について説明します。
solution: Experience Manager
title: 画像レンダリングHTTPプロトコルの基本構文
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 3%

---

# 画像レンダリングHTTPプロトコルの基本構文{#image-rendering-http-protocol-basic-syntax}

この節では、Dynamic Media Image Rendering HTTPプロトコルの基本構文について説明します。

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
   <td colname="col2"> <p><span class="varname"> server_address</span> [ : <span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> ビネット  </span> </p> </td> 
   <td colname="col2"> <p>ビネット指定子（相対ファイルパスまたはビネットカタログエントリ） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾子 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span>  *[ &amp;  <span class="varname"> modifier</span>  ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修飾子 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span>  | { $  <span class="varname"> macro</span> $ } | { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> マクロ  </span> </p> </td> 
   <td colname="col2"> <p>コマンドマクロの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> コメント  </span> </p> </td> 
   <td colname="col2"> <p>コメント文字列（サーバーで無視）。 </p> </td> 
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

*`server`*、 *`cmdName`*、 *`macro`*&#x200B;およびは大文字 *`var`* と小文字を区別しません。サーバーは、他のすべての文字列値の大文字と小文字を区別します。

**サーバー識別子**

画像レンダリングへのすべてのHTTPリクエストには、「 `/ir/render` 」ルートコンテキストが必要です。

**コメント**

コメントは、リクエスト文字列の任意の場所に埋め込むことができ、ピリオド(.)で識別されます。 コマンド区切り文字(&amp;)の直後に表示されます。 コメントは、次に（エンコードされていない）コマンド区切り文字が出現するまで終了します。 この機能は、タイムスタンプ、データベースIDなど、画像サービングでは使用しない情報を要求に追加する場合に使用します。

**HTTPデコード**

画像レンダリングは、最初に受信リクエストから&#x200B;*`object`*&#x200B;と&#x200B;*`modifiers`*&#x200B;を抽出します。 *`object`* は、個別にHTTPデコードされたパス要素に分割されます。*`modifiers`*&#x200B;文字列は&#x200B;*`command`*=*`value`*&#x200B;のペアに分割され、*`value`*&#x200B;はコマンド固有の処理の前にHTTPデコードされます。
