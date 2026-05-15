---
title: 画像レンダリング HTTP プロトコルの基本構文
description: この節では、Dynamic Media Image Rendering HTTP プロトコルの基本的な構文について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
TQID: 'https://experienceleague.adobe.com/v-ucFAnnoq6ywaB97QSXodqnO4VWFvaK6I2HJ2-a4Fc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# 画像レンダリング HTTP プロトコルの基本構文{#image-rendering-http-protocol-basic-syntax}

この節では、Dynamic Media Image Rendering HTTP プロトコルの基本的な構文について説明します。

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>項目 </p> </th> 
   <th colname="col2" class="entry"> <p>定義 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> リクエスト </span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> 修飾子</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> サーバー</span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> ビネット </span> </p> </td> 
   <td colname="col2"> <p>周辺光量指定（相対ファイルパスまたは周辺光量補正カタログエントリ）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">個の修飾子</span> </p> </td> 
   <td colname="col2"> <p><span class="varname">修飾子</span> *[ &amp; <span class="varname">修飾子</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">修飾子</span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> コマンド </span> | { $ <span class="varname"> マクロ </span> $ } | { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> コマンド </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname">値</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> マクロ </span> </p> </td> 
   <td colname="col2"> <p>コマンド マクロの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> コメント </span> </p> </td> 
   <td colname="col2"> <p>コメント文字列（サーバーによって無視）。 </p> </td> 
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
   <td colname="col1"> <p><span class="varname">値</span> </p> </td> 
   <td colname="col2"> <p>コマンドまたは変数の値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*、*`cmdName`*、*`macro`*&#x200B;および&#x200B;*`var`*&#x200B;では、大文字と小文字が区別されません。 サーバーは、他のすべての文字列値の大文字と小文字を保持します。

**サーバー識別子**

画像レンダリングへのすべてのHTTP リクエストには、&#39; `/ir/render`&#39; ルートコンテキストが必要です。

**コメント**

コメントは、任意の場所のリクエスト文字列に埋め込むことができ、ピリオド（。）で識別されます。 コマンド区切り記号（&amp;）の直後に入力します。 コメントは、（エンコードされていない）コマンド区切り文字が次に発生することによって終了します。 この機能は、タイムスタンプやデータベース IDなど、画像サービング用ではない情報をリクエストに追加するために使用できます。

**HTTP デコード**

画像レンダリングでは、最初に受信リクエストから&#x200B;*`object`*&#x200B;と&#x200B;*`modifiers`*&#x200B;が抽出されます。 次に、*`object`*&#x200B;は、個別にHTTP デコードされるパス要素に分けられます。 *`modifiers`*&#x200B;文字列は&#x200B;*`command`*= *`value`*&#x200B;組に分けられ、*`value`*&#x200B;はコマンド固有の処理の前にHTTP デコードされます。
