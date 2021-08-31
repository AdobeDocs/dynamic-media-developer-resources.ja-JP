---
description: HTTPプロトコルの基本構文は次のとおりです。
solution: Experience Manager
title: 画像サービングHTTPプロトコルの基本構文
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---

# 画像サービングHTTPプロトコルの基本構文{#image-serving-http-protocol-basic-syntax}

HTTPプロトコルの基本構文を次に示します。

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
  <td class="stentry"> <p>ソースオブジェクト指定子（画像パスまたは画像カタログエントリ）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifiers</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span> *[&amp;<span class="varname"> modifier</span>]</span> </p> </td> 
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
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> マクロ</span> </span> </p> </td> 
  <td class="stentry"> <p>コマンドマクロの名前。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> コメント</span> </span> </p></td> 
  <td class="stentry"> <p>コメント文字列（サーバーで無視）。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>サポートされているコマンド名または属性名の1つ。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>カスタム変数の名前。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span> </span> </p></td> 
  <td class="stentry"> <p>コマンドまたは変数の値。 </p></td> 
 </tr> 
</table>

*`server_address`*、 *`cmdName`*、 *`macro`*&#x200B;およびは大文字 *`var`* と小文字を区別しません。サーバーは、他のすべての文字列値の大文字と小文字を区別します。

*`value`* はコマンド固有で、コンマで区切った1つ以上の値で構成できます。詳しくは、個々のコマンドの説明を参照してください。

## サーバー識別子 {#section-926ae55ddba14b8d952147a5fd701e14}

画像サービングへのすべてのHTTP要求には、[!DNL /is/image]ルートコンテキストが必要です。

## HTTPデコード {#section-20922baccd804d2d986b44ce9a183a7d}

画像サービングは、まず、受信要求から&#x200B;*`object`*&#x200B;と&#x200B;*`modifiers`*&#x200B;を抽出します。 *`object`* は、個別にHTTPデコードされたパス要素に分割されます。*`modifiers`*&#x200B;文字列は&#x200B;*`command`*=*`value`*&#x200B;のペアに分割され、*`value`*&#x200B;はコマンド固有の処理の前にHTTPデコードされます。

>[!NOTE]
>
>ドキュメントに特に記載がない限り、安全でない文字はすべてHTTP標準に従ってエンコードする必要があります。 詳しくは、 HTTP仕様を参照してください。

## コメント {#section-69ef0be0f17a418c87a0eba21c2ddb00}

コメントは、リクエスト文字列の任意の場所に埋め込むことができ、ピリオド(.) コマンドseparator(&amp;)の直後。 コメントは、次に（エンコードされていない）コマンド区切り文字が出現するまで終了します。 この機能を使用して、タイムスタンプやデータベースIDなど、画像サービングでは使用しない情報を要求に追加できます。

## 関連項目 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[データタイプ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa)、 [HTTP/1.1仕様](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
