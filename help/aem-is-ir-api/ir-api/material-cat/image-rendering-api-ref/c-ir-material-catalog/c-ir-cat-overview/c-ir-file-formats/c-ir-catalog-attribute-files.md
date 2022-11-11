---
title: カタログ属性ファイル
description: カタログ属性ファイルには任意の名前を付けることができますが、.ini ファイルのサフィックスを付ける必要があります。 任意のテキストエディターを使用して、簡単に管理できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# カタログ属性ファイル{#catalog-attribute-files}

カタログ属性ファイルには任意の名前を指定できますが、 `.ini` ファイルサフィックス 任意のテキストエディターを使用して、簡単に管理できます。

カタログ属性ファイルは、一連のテキストレコードで構成され、1 つのレコードで区切られます `<CR>` （ASCII コード 0xD）, `<LF>` （ASCII コード 0xA）、または `<CR><LF>` ペア。 各レコードは、属性名と 1 つ以上のコンマ区切りの属性値で構成されます。

`*`名前`*= *`値`*&#42;[, *`値`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名前 </span> </span> </p> </td> 
  <td class="stentry"> <p>属性名；は、1 つ以上の文字、数字、「 — 」、「_」で構成できます。大文字と小文字が区別されません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 値 </span> </span> </p> </td> 
  <td class="stentry"> <p>属性値次を含める必要はありません <span class="codeph"> &lt;cr&gt; </span>または <span class="codeph"> &lt;lf&gt; </span> 改行文字の直前にある 1 つのバックスラッシュでエスケープしない限り、文字。 </p> </td> 
 </tr> 
</table>

* トークン間の空白はオプションです。
* 属性名が不明なレコードは、 [!DNL Platform Server].
* 属性名は、ASCII 文字、数字、「 — 」、「_」、「。」の任意の組み合わせで構成できます。
* 同じ属性ファイル内で同じ属性名が複数回存在する場合は、最後に発生した属性名が優先されます。
* 最初の文字として「#」を使用し、任意のレコードをパーサーによって無視されるコメントとしてマークします。
