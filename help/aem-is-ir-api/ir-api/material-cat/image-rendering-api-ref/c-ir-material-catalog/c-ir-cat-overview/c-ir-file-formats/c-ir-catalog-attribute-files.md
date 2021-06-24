---
description: カタログ属性ファイルには任意の名前を付けることができますが、.iniファイルのサフィックスを付ける必要があります。 これらは、任意のテキストエディターを使用して簡単に管理できます。
solution: Experience Manager
title: カタログ属性ファイル
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# カタログ属性ファイル{#catalog-attribute-files}

カタログ属性ファイルには任意の名前を付けることができますが、.iniファイルのサフィックスを付ける必要があります。 これらは、任意のテキストエディターを使用して簡単に管理できます。

カタログ属性ファイルは、1つの`<CR>`（ASCIIコード0xD）、1つの`<LF>`（ASCIIコード0xA）、または`<CR><LF>`の組で区切られた一連のテキストレコードで構成されます。 各レコードは、属性名と1つ以上のコンマ区切りの属性値で構成されます。

`*``*= *``*&#42;[, *`namevaluevalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>属性名には、1つ以上の文字、数字、「 — 」および「_」を使用できます。大文字と小文字は区別されません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>属性値<span class="codeph"> &lt;CR&gt; </span>文字または<span class="codeph"> &lt;LF&gt; </span>文字を含めないでください。ただし、改行文字の直前に1つのバックスラッシュでエスケープする場合を除きます。 </p> </td> 
 </tr> 
</table>

* トークン間の空白はオプションです。
* 属性名が不明なレコードは、Platform Serverでは無視されます。
* 属性名は、ASCII文字、数字、「 — 」、「_」、「。」の任意の組み合わせで構成できます。
* 同じ属性ファイル内に同じ属性名が複数存在する場合は、最後に見つかった属性名が優先されます。
* 最初の文字として「#」を使用し、任意のレコードをパーサーによって無視されるコメントとしてマークします。
