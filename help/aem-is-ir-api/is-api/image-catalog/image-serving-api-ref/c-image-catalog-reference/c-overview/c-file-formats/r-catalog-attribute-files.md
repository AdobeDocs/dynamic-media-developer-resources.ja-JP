---
description: カタログ属性ファイルには任意の名前を付けることができますが、.ini ファイルのサフィックスを付ける必要があります。 これらは、任意のテキストエディターを使用して簡単に管理できます。
solution: Experience Manager
title: カタログ属性ファイル
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 1%

---

# カタログ属性ファイル{#catalog-attribute-files}

カタログ属性ファイルには任意の名前を付けることができますが、.ini ファイルのサフィックスを付ける必要があります。 これらは、任意のテキストエディターを使用して簡単に管理できます。

カタログ属性ファイルは、一連のテキストレコードで構成され、1 つのレコードで区切られます。 `<CR>` （ASCII コード） `0xD`)、単一の `<LF>` （ASCII コード） `0xA`)、または `<CR><LF>` ペア。 各レコードは、属性名と 1 つ以上のコンマ区切りの属性値で構成されます。

`*`名前`*= *`値`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 値</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> 値</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>属性名。 1 つ以上の文字、数字、-、_で構成されます。 大文字と小文字は区別されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>属性値。 次を含めることはできません <span class="codeph"> &lt;cr&gt;</span> または <span class="codeph"> &lt;lf&gt;</span> 改行文字の直前にある 1 つのバックスラッシュでエスケープしない限り、文字。 </p></td> 
 </tr> 
</table>

トークン間の空白はオプションです。

不明な属性名を持つレコードは、 [!DNL Platform Server].

属性名は、ASCII 文字、数字、「 — 」、「_」、「。」の組み合わせで構成することができます。

同じ属性ファイル内で同じ属性名が複数回存在する場合は、最後に発生した属性名が優先されます。

#を最初の文字として使用し、任意のレコードをコメントとしてマークします。この場合、パーサーは無視します。
