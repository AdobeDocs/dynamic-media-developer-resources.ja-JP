---
description: HTTPプロトコルの基本構文は次のとおりです。
seo-description: HTTPプロトコルの基本構文は次のとおりです。
seo-title: 画像サービングHTTPプロトコルの基本構文
solution: Experience Manager
title: 画像サービングHTTPプロトコルの基本構文
topic: Scene7 Image Serving - Image Rendering API
uuid: 3269c2f2-df0f-4b62-ae9c-a267acae8071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---


# 画像サービングHTTPプロトコル基本構文{#image-serving-http-protocol-basic-syntax}

HTTPプロトコルの基本構文は次のとおりです。

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> リクエスト</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> modifiers</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server  </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span> </span> </p></td> 
  <td class="stentry"> <p>ソースオブジェクト指定子（画像パスまたは画像カタログエントリ） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifiers</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span>*[&amp;<span class="varname"> modifier</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">command|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> command</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
  <td class="stentry"> <p>コマンドマクロの名前。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> コメント</span> </span> </p></td> 
  <td class="stentry"> <p>コメント文字列（サーバーでは無視されます）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>サポートされているコマンド名または属性名の1つ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>カスタム変数の名前。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span> </span> </p></td> 
  <td class="stentry"> <p>コマンドまたは変数の値。 </p></td> 
 </tr> 
</table>

*`server_address`*、、 *`cmdName`*、 *`macro`*&#x200B;およびは大文字と小文字が区別されま *`var`* せん。サーバーは、大文字と小文字を区別し、他の文字列値もすべて保持します。

*`value`* はコマンド固有で、1つ以上の値をコンマで区切って構成できます。詳しくは、個々のコマンドの説明を参照してください。

## サーバー識別子{#section-926ae55ddba14b8d952147a5fd701e14}

[!DNL /is/image]ルートコンテキストは、画像サービングへのすべてのHTTP要求に必要です。

## HTTPデコード{#section-20922baccd804d2d986b44ce9a183a7d}

画像サービングは、最初に、受信要求から&#x200B;*`object`*&#x200B;と&#x200B;*`modifiers`*&#x200B;を抽出します。 *`object`* は、個別にHTTPデコードされるパス要素に分割されます。*`modifiers`*&#x200B;文字列は&#x200B;*`command`*= *`value`*&#x200B;ペアに区切られ、*`value`*&#x200B;はコマンド固有の処理の前にHTTPデコードされます。

>[!NOTE]
>
>ドキュメントに特に記載がない限り、安全でないすべての文字は、HTTP標準に従ってエンコードする必要があります。 詳しくは、HTTPの仕様を参照してください。

## コメント {#section-69ef0be0f17a418c87a0eba21c2ddb00}

コメントはリクエスト文字列のどこにでも埋め込むことができ、ピリオド(.)で識別します。 コマンドseparator(&amp;)の直後にあります。 コメントは、（エンコードされていない）コマンドの区切り文字が次に出現するたびに終了します。 この機能は、タイムスタンプ、データベースIDなど、画像サービングで使用されない情報を要求に追加する場合に使用します。

## 関連項目 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[データ型](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa)、 [HTTP/1.1仕様](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
