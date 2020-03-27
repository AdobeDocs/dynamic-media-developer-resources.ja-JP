---
description: カタログ属性ファイルには任意の名前を付けることができますが、.iniファイルのサフィックスを付ける必要があります。 どのテキストエディターでも、簡単に管理できます。
seo-description: カタログ属性ファイルには任意の名前を付けることができますが、.iniファイルのサフィックスを付ける必要があります。 どのテキストエディターでも、簡単に管理できます。
seo-title: カタログ属性ファイル
solution: Experience Manager
title: カタログ属性ファイル
topic: Scene7 Image Serving - Image Rendering API
uuid: ea2bddad-2c4a-43c1-9b62-6e724fcfb8a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# カタログ属性ファイル{#catalog-attribute-files}

カタログ属性ファイルには任意の名前を付けることができますが、.iniファイルのサフィックスを付ける必要があります。 どのテキストエディターでも、簡単に管理できます。

カタログ属性ファイルは、1つのテキストレコード（ASCIIコード0xD）、1つの `<CR>` （ASCIIコード0xA）または `<LF>` 1組のテキストレコードで構成され `<CR><LF>` ます。 各レコードは、属性名と1つ以上のカンマ区切りの属性値で構成されます。

` *`namevaluevalue`*= *``*&#42;[, *`値`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名 </span> 前 </span> </p> </td> 
  <td class="stentry"> <p>属性名；は、1文字以上、数字、「 — 」および「_」で構成できます。大文字と小文字は区別されません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 価 </span> 値 </span> </p> </td> 
  <td class="stentry"> <p>属性値；は、改行文字の直前に <span class="codeph"> ある1つのバックスラッシュでエ </span>スケープされない限り、&lt;CR&gt; <span class="codeph"></span> または&lt;LF&gt;文字を含めないでください。 </p> </td> 
 </tr> 
</table>

* トークン間の空白はオプションです。
* 属性名が不明なレコードは、プラットフォームサーバーでは無視されます。
* 属性名は、ASCII文字、数字、「 — 」、「_」、「。」の任意の組み合わせで構成できます。
* 同じ属性ファイル内に同じ属性名が複数存在する場合は、最後に存在した属性名が使用されます。
* 「#」を最初の文字として使用し、パーサが無視するコメントとしてレコードをマークします。

