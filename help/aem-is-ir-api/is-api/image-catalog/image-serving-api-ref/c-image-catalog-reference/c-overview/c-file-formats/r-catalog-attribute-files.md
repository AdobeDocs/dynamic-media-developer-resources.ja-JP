---
description: カタログ属性ファイルには任意の名前を付けることができますが、.iniファイルのサフィックスを付ける必要があります。 これらは、任意のテキストエディタを使用して簡単に管理できます。
seo-description: カタログ属性ファイルには任意の名前を付けることができますが、.iniファイルのサフィックスを付ける必要があります。 これらは、任意のテキストエディタを使用して簡単に管理できます。
seo-title: カタログ属性ファイル
solution: Experience Manager
title: カタログ属性ファイル
topic: Scene7 Image Serving - Image Rendering API
uuid: 63985780-f032-4542-8d84-b8b608ceea4b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# カタログ属性ファイル{#catalog-attribute-files}

カタログ属性ファイルには任意の名前を付けることができますが、.iniファイルのサフィックスを付ける必要があります。 これらは、任意のテキストエディタを使用して簡単に管理できます。

カタログ属性ファイルは、テキストレコードのセットで構成され、1つの`<CR>`（ASCIIコード`0xD`）、1つの`<LF>`（ASCIIコード`0xA`）、または`<CR><LF>`のペアで区切られます。 各レコードは、属性名と1つ以上のコンマ区切りの属性値で構成されます。

` *``*= *`名前値`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 値</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> values</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>属性名。 は、1文字以上、数字、 — および_で構成できます。 大文字と小文字は区別されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>属性値 改行文字の直前に1つのバックスラッシュでエスケープされていない限り、<span class="codeph"> &lt;CR&gt;</span>または<span class="codeph"> &lt;LF&gt;</span>文字を含めないでください。 </p></td> 
 </tr> 
</table>

トークン間の空白はオプションです。

属性名が不明なレコードは、プラットフォームサーバーで無視されます。

属性名は、ASCII文字、数字、「 — 」、「_」、「。」の組み合わせで構成できます。

同じ属性ファイル内で同じ属性名が複数回出現する場合は、最後に発生した属性名が使用されます。

#を最初の文字として使用し、任意のレコードをコメントとしてマークします。これはパーサーによって無視されます。
