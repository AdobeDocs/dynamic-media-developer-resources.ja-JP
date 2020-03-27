---
description: リクエストルール要素。 <ruleset>要素では1つ以上がオプションです。
seo-description: リクエストルール要素。 <ruleset>要素では1つ以上がオプションです。
seo-title: ルール
solution: Experience Manager
title: ルール
topic: Scene7 Image Serving - Image Rendering API
uuid: f7071681-e97e-4081-aeb1-093d2b23041c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ルール{#rule}

リクエストルール要素。 要素内の1つ以上はオプション `<ruleset>` です。

## Attributes {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"`（オプション）初期設定は「break」です。

` Name=" *`text`*"` Optional。 デバッグログおよびエラーメ `<rule>` ッセージの要素を識別するために使用します。

また、要素は `<rule>` 、任意の組み合わせで次の属性を定義できます。 指定した場合、ルールが正しく一致すると、このリクエストの対応するカタログ属性が上書きされます。

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
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> attribute::DefautPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> attribute::ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 有効期限 </span> </p> </td> 
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

有効期限属性は、デフォルトの属性値より優先されます。特定の値がリクエストに適用さ `catalog::Expiration` れる場合は無視されます。

## データ {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;式&gt; </span> </p> </td> 
  <td class="stentry"> <p>（オプション） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;置換&gt; </span> </p> </td> 
  <td class="stentry"> <p>（オプション） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;addressfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>（オプション） </p> </td> 
 </tr> 
</table>

## 説明 {#section-a27b91f9a03047c0bb7edc0967fb4216}

との両方を指 `<expression>` 定し、 `<substitution>` 取り込んだサブ文字列を使用しない場合、一致した最初のサブ文字列がに置き換えられま `<substitution>`す。

を指 `<expression>` 定しない場合、パスは一致し、 `<substitution>` パスの末尾に追加されます。

を指定し `<substitution>` ない場合、一致したサブ文字列が削除されます。

は、一 `<addressfilter>` 致が発生した場合、およびクエリルールが適用される前にのみ適用されます。
