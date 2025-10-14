---
description: HTTP プロトコルの基本的な構文は次のとおりです。
solution: Experience Manager
title: 画像サービス HTTP プロトコルの基本構文
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# 画像サービス HTTP プロトコルの基本構文{#image-serving-http-protocol-basic-syntax}

HTTP プロトコルの基本的な構文は次のとおりです。

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> リクエスト </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> 修飾子 </span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> オブジェクト </span> </span> </p></td> 
  <td class="stentry"> <p>Source オブジェクト指定子（画像パスまたは画像カタログエントリ）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾子 </span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾子 </span>*[&amp;<span class="varname"> 修飾子 </span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾子 </span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">command|{$<span class="varname"> マクロ </span>$}|{.<span class="varname"> コメント </span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> コマンド </span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> マクロ </span> </span> </p> </td> 
  <td class="stentry"> <p>コマンド マクロの名前。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> comment</span> </span> </p></td> 
  <td class="stentry"> <p>コメント文字列（サーバーでは無視されます）。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>サポートされるコマンド名または属性名。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>カスタム変数の名前。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 値 </span> </span> </p></td> 
  <td class="stentry"> <p>コマンドまたは変数値。 </p></td> 
 </tr> 
</table>

*`server_address`*、*`cmdName`*、*`macro`*、*`var`* では、大文字と小文字が区別されません。 サーバーは、他のすべての文字列値の大文字と小文字を区別しません。

*`value`* はコマンド固有であり、コンマで区切られた 1 つ以上の値で構成できます。 詳しくは、個々のコマンドの説明を参照してください。

## サーバー識別子 {#section-926ae55ddba14b8d952147a5fd701e14}

画像サービングへのすべての HTTP リクエストに [!DNL /is/image] ルートコンテキストが必要です。

## HTTP デコード {#section-20922baccd804d2d986b44ce9a183a7d}

画像サービングでは、まず受信リクエストから *`object`* と *`modifiers`* を抽出します。 次に、*`object`* をパス要素に分割し、各パス要素を個別に HTTP デコードします。 *`modifiers`* の文字列は *`command`*= *`value`* ペアに分割され、*`value`* の後、コマンド固有の処理の前に HTTP デコードされます。

>[!NOTE]
>
>ドキュメントで特に指定がない限り、安全でない文字はすべて、HTTP 標準に従ってエンコードする必要があります。 詳しくは、HTTP の仕様を参照してください。

## コメント {#section-69ef0be0f17a418c87a0eba21c2ddb00}

コメントは、任意の場所のリクエスト文字列に埋め込むことができ、コマンド区切り記号（&amp;）の直後のピリオド（.）で識別されます。 コメントは、（エンコードされていない）コマンド区切り記号が次に現れることによって終了します。 この機能を使用すると、画像サービング以外の情報（タイムスタンプ、データベース ID など）をリクエストに追加できます。

## 関連項目 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[&#x200B; データタイプ &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa)、[HTTP/1.1 仕様 &#x200B;](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
