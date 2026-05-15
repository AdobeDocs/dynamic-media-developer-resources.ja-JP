---
description: リクエストルール要素： <ruleset>要素の1つ以上はオプションです。
solution: Experience Manager
title: ルール
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f56012c-d01c-489c-9d18-91e256f72012
TQID: 'https://experienceleague.adobe.com/jNaX4-STdjDuKxcSFr5GhjpgB8fiGHrfegR1FxZOFhU'
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
ht-degree: 3%

---

# ルール{#rule}

リクエストルール要素： `<ruleset>`要素では、1つ以上がオプションです。

## 属性 {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` オプション。 デフォルトは「break」です。

` Name=" *`text`*"` オプション。 デバッグログとエラーメッセージで`<rule>`要素を識別するために使用します。

さらに、`<rule>`要素は、任意の組み合わせで次のいずれかの属性を定義できます。 指定され、ルールが正常に一致した場合、このリクエストに対応するカタログ属性が上書きされます。

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>&lt;rule&gt;属性 </p> </th> 
   <th colname="col2" class="entry"> <p>対応する画像カタログ属性 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local">属性：:DefautPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local">属性：:ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">有効期限</span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local">属性：：有効期限</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local">属性：:MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local">属性：:RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

詳しくは、対応する画像カタログ属性の説明を参照してください。

Expiration属性は、デフォルトの属性値のみを上書きします。特定の`catalog::Expiration`値がリクエストに適用される場合は無視されます。

## データ {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;式&gt; </span> </p> </td> 
  <td class="stentry"> <p>オプション。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;代替&gt; </span> </p> </td> 
  <td class="stentry"> <p>オプション。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;addressfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>オプション。 </p> </td> 
 </tr> 
</table>

## 説明 {#section-a27b91f9a03047c0bb7edc0967fb4216}

`<expression>`と`<substitution>`の両方が指定されていて、キャプチャされた部分文字列が使用されていない場合、最初に一致した部分文字列は`<substitution>`に置き換えられます。

`<expression>`が指定されていない場合、パスが一致し、`<substitution>`がパスの末尾に追加されます。

`<substitution>`が指定されていない場合、一致する部分文字列は削除されます。

`<addressfilter>`は、一致が発生し、クエリ ルールが適用される前にのみ適用されます。
