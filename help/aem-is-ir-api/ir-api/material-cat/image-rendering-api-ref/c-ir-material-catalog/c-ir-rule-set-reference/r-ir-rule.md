---
description: リクエストルール要素。 <ruleset> 要素には、オプションの要素が 1 つ以上あります。
solution: Experience Manager
title: ルール
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f56012c-d01c-489c-9d18-91e256f72012
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# ルール{#rule}

リクエストルール要素。 `<ruleset>` 要素には、1 つ以上のパラメーターがオプションです。

## 属性 {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` オプション。 デフォルトは「break」です。

` Name=" *`text`*"` オプション。 デバッグログとエラーメッセージの `<rule>` 要素を識別するために使用します。

さらに、`<rule>` 要素は、任意の組み合わせで次の属性のいずれかを定義できます。 指定した場合、ルールが正常に一致すると、このリクエストに対応するカタログ属性が上書きされます。

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>&lt;rule&gt; 属性 </p> </th> 
   <th colname="col2" class="entry"> <p>対応する画像カタログ属性 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> attribute::DefaultPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> 属性：:ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Expiration </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> attribute::Expiration </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> attribute::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> attribute::RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

詳しくは、対応する画像カタログ属性の説明を参照してください。

Expiration 属性は、デフォルトの属性値のみを上書きします。特定の `catalog::Expiration` 値がリクエストに適用される場合、この属性は無視されます。

## データ {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt; 式 &gt; </span> </p> </td> 
  <td class="stentry"> <p>オプション。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt; 交代 &gt; </span> </p> </td> 
  <td class="stentry"> <p>オプション。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;addressfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>オプション。 </p> </td> 
 </tr> 
</table>

## 説明 {#section-a27b91f9a03047c0bb7edc0967fb4216}

`<expression>` と `<substitution>` の両方を指定し、取得した部分文字列を使用しない場合は、最初に一致した部分文字列が `<substitution>` に置き換えられます。

`<expression>` を指定しない場合、任意のパスが一致し、`<substitution>` がパスの末尾に追加されます。

`<substitution>` を指定しない場合、一致した部分文字列は削除されます。

`<addressfilter>` は、一致が発生した場合、およびクエリルールが適用される前にのみ適用されます。
