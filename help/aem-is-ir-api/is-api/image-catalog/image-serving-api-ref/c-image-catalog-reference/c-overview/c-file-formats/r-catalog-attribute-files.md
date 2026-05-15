---
description: カタログ属性ファイルには任意の名前を付けることができますが、.ini ファイルのサフィックスを付ける必要があります。 任意のテキストエディターを使用して、容易に管理できます。
solution: Experience Manager
title: カタログ属性ファイル
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
TQID: 'https://experienceleague.adobe.com/RCxeXg3wb10jo37biAs1puqmEo8bAL-i-oZBwGHuloA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 0%

---

# カタログ属性ファイル{#catalog-attribute-files}

カタログ属性ファイルには任意の名前を付けることができますが、.ini ファイルのサフィックスを付ける必要があります。 任意のテキストエディターを使用して、容易に管理できます。

カタログ属性ファイルは、単一の`<CR>` （ASCII コード `0xD`）、単一の`<LF>` （ASCII コード `0xA`）、または`<CR><LF>` ペアで区切られた一連のテキストレコードで構成されます。 各レコードは、属性名と1つ以上のコンマ区切りの属性値で構成されます。

`*`name`*= *`values`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">個の値</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname">個の値</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">名</span> </p> </td> 
  <td class="stentry"> <p>属性名： 1つ以上の文字、数字、-、および_で構成される場合があります。 大文字と小文字を区別しない。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>属性値： 改行文字の直前に1つのバックスラッシュでエスケープしない限り、<span class="codeph"> &lt;CR&gt;</span>または<span class="codeph"> &lt;LF&gt;</span>文字を含めることはできません。 </p></td> 
 </tr> 
</table>

トークン間の空白はオプションです。

属性名が不明なレコードは、[!DNL Platform Server]によって無視されます。

属性名は、ASCII文字、数字、および「 – 」、「_」、「。」の任意の組み合わせで構成できます。

同じ属性名が同じ属性ファイル内で複数回発生する場合は、最後に発生した属性名が優先されます。

#を最初の文字として使用して、任意のレコードをコメントとしてマークします。これはパーサーが無視します。
