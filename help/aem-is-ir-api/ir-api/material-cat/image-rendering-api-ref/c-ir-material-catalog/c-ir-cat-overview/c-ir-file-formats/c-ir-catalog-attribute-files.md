---
title: カタログ属性ファイル
description: カタログ属性ファイルには任意の名前を付けることができますが、.ini ファイルのサフィックスを付ける必要があります。 任意のテキストエディターを使用して、容易に管理できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
TQID: 'https://experienceleague.adobe.com/OwtzX3xKh5ByC3eUhz7dmFjGR5HRD9cbE6atUEL0Nic'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 0%

---

# カタログ属性ファイル{#catalog-attribute-files}

カタログ属性ファイルには任意の名前を付けることができますが、`.ini` ファイルのサフィックスを付ける必要があります。 任意のテキストエディターを使用して、容易に管理できます。

カタログ属性ファイルは、1つの`<CR>` （ASCII コード 0xD）、1つの`<LF>` （ASCII コード 0xA）、または`<CR><LF>` ペアで区切られた一連のテキストレコードで構成されます。 各レコードは、属性名と1つ以上のコンマ区切りの属性値で構成されます。

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">名</span> </span> </p> </td> 
  <td class="stentry"> <p>属性名。1つ以上の文字、数字、– （ハイフン）、_（アンダースコア）で構成できます。大文字と小文字は区別されません。</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">値</span> </span> </p> </td> 
  <td class="stentry"> <p>属性値。改行文字の直前に1つのバックスラッシュでエスケープしない限り、<span class="codeph"> &lt;CR&gt; </span>または<span class="codeph"> &lt;LF&gt; </span>文字を含めることはできません。 </p> </td> 
 </tr> 
</table>

* トークン間の空白はオプションです。
* [!DNL Platform Server]は、不明な属性名を持つレコードを無視します。
* 属性名は、ASCII文字、数字、および`-`、`_`、`.`文字の任意の組み合わせで構成できます。
* 同じ属性名が同じ属性ファイル内で複数回発生する場合は、最後に発生した属性名が優先されます。
* `#`を最初の文字として使用して、任意のレコードをパーサーが無視するコメントとしてマークします。
