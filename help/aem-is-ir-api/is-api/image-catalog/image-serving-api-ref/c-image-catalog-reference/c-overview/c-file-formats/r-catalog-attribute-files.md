---
description: カタログ属性ファイルには任意の名前を付けることができますが、.ini ファイルの拡張子を付ける必要があります。 任意のテキストエディターを使用して簡単に維持できます。
solution: Experience Manager
title: カタログ属性ファイル
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# カタログ属性ファイル{#catalog-attribute-files}

カタログ属性ファイルには任意の名前を付けることができますが、.ini ファイルの拡張子を付ける必要があります。 任意のテキストエディターを使用して簡単に維持できます。

カタログ属性ファイルは、1 つの `<CR>` （ASCII コード `0xD`）、1 つの `<LF>` （ASCII コード `0xA`）、または `<CR><LF>` のペアで区切られた一連のテキスト レコードで構成されます。 各レコードは、属性名と、1 つ以上のコンマ区切り属性値で構成されます。

`*`name`*= *`values`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 値 </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> values</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 名 </span> </p> </td> 
  <td class="stentry"> <p>属性名。 1 つ以上の文字、数字、– および_で構成される場合があります。 大文字と小文字は区別されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>属性値。 改行文字の直前 <span class="codeph">1 つのバックスラッシュでエスケープしない限り、&lt;CR&gt;</span> 文字または <span class="codeph">&lt;LF&gt;</span> 文字を含めないでください。 </p></td> 
 </tr> 
</table>

トークン間の空白は任意です。

不明な属性名を持つレコードは、[!DNL Platform Server] で無視されます。

属性名は、ASCII 文字、数字、「–」、「_」、「。」の任意の組み合わせで構成できます。

同じ属性ファイル内で同じ属性名が複数回出現する場合は、最後に出現した属性名が優先されます。

&#x200B;#を最初の文字として使用して、パーサーが無視するレコードをコメントとしてマークします。
