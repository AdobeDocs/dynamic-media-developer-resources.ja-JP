---
title: カタログ属性ファイル
description: カタログ属性ファイルには任意の名前を付けることができますが、.ini ファイルの拡張子を付ける必要があります。 任意のテキストエディターを使用して簡単に維持できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# カタログ属性ファイル{#catalog-attribute-files}

カタログ属性ファイルには任意の名前を付けることができますが、ファイルの接尾辞は `.ini` にする必要があります。 任意のテキストエディターを使用して簡単に維持できます。

カタログ属性ファイルは、1 つの `<CR>` （ASCII コード 0xD）、1 つの `<LF>` （ASCII コード 0xA）、または `<CR><LF>` のペアで区切られた一連のテキスト レコードで構成されます。 各レコードは、属性名と、1 つ以上のコンマ区切り属性値で構成されます。

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> の名前 </span> </span> </p> </td> 
  <td class="stentry"> <p>属性名。1 つ以上の文字、数字、– （ハイフン）、_（アンダースコア）で構成でき、大文字と小文字は区別されません。</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 値 </span> </span> </p> </td> 
  <td class="stentry"> <p>属性値。改行文字の直前 <span class="codeph"> 単一のバックスラッシュでエスケープされない限り、&lt;CR&gt;</span> または <span class="codeph">&lt;LF&gt;</span> 文字を含めることはできません。 </p> </td> 
 </tr> 
</table>

* トークン間の空白は任意です。
* [!DNL Platform Server] は、不明な属性名を持つレコードを無視します。
* 属性名は、ASCII 文字、数字、`-`、`_`、`.` 文字の任意の組み合わせで構成できます。
* 同じ属性ファイル内で同じ属性名が複数回出現する場合は、最後に出現した属性名が優先されます。
* `#` を最初の文字として使用して、パーサーが無視するコメントとしてレコードをマークします。
