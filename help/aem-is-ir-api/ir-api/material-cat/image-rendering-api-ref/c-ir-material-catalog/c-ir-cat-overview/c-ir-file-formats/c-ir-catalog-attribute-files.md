---
description: カタログ属性ファイルには任意の名前を付けることができますが、.iniファイルのサフィックスを付ける必要があります。 これらは、任意のテキストエディタを使用して簡単に管理できます。
solution: Experience Manager
title: カタログ属性ファイル
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# カタログ属性ファイル{#catalog-attribute-files}

カタログ属性ファイルには任意の名前を付けることができますが、.iniファイルのサフィックスを付ける必要があります。 これらは、任意のテキストエディタを使用して簡単に管理できます。

カタログ属性ファイルは、テキストレコードのセットで構成され、1つの`<CR>`（ASCIIコード0xD）、1つの`<LF>`（ASCIIコード0xA）、または`<CR><LF>`のペアで区切られます。 各レコードは、属性名と1つ以上のコンマ区切りの属性値で構成されます。

`*``*= *``*&#42;[, *`namevaluevalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Attribute name;は、1文字以上、数字、「 — 」および「_」で構成できます。大文字と小文字は区別されません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Attribute value;改行文字の直前に1つのバックスラッシュでエスケープされない限り、<span class="codeph"> &lt;CR&gt; </span>または<span class="codeph"> </span>文字を含めないでください。 </p> </td> 
 </tr> 
</table>

* トークン間の空白はオプションです。
* 属性名が不明なレコードは、プラットフォームサーバーで無視されます。
* 属性名は、ASCII文字、数字、「 — 」、「_」、「。」の組み合わせで構成できます。
* 同じ属性ファイル内で同じ属性名が複数回出現する場合は、最後に発生した属性名が使用されます。
* 「#」を最初の文字として使用し、すべてのレコードをパーサーによって無視されるコメントとしてマークします。

