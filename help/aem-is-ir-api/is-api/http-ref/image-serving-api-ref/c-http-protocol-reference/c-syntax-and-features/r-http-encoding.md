---
description: コマンド値は、値文字列に予約文字「=」、「&」、「%」が含まれないように、%xxエスケープシーケンスを使用してHTTPエンコードする必要があります。
seo-description: コマンド値は、値文字列に予約文字「=」、「&」、「%」が含まれないように、%xxエスケープシーケンスを使用してHTTPエンコードする必要があります。
seo-title: 画像サービングHTTPエンコーディング
solution: Experience Manager
title: 画像サービングHTTPエンコーディング
topic: Scene7 Image Serving - Image Rendering API
uuid: e7fb368b-060a-439e-95a1-16b94d4796dc
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 画像サービングHTTPエンコーディング{#image-serving-http-encoding}

コマンド値は、値文字列に予約文字「=」、「&amp;」、「%」が含まれないように、%xxエスケープシーケンスを使用してHTTPエンコードする必要があります。

それ以外の場合は、標準のHTTPエンコーディングルールが適用されます。 HTTP仕様では、安全でない文字と、およびなどの制御文字のエンコードが必要 `<return>` です `<tab>`。 文字のURLエンコーディングは、「%」記号に続いて、その文字のISO-Latinコードポイントの2桁の16進表現（大文字と小文字を区別しない）が続きます。 安全でない文字とコードポイントは次のとおりです。

<table id="table_D2C01CADB35E477D82D4C27586424625"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 安全でない文字 </th> 
   <th colname="col2" class="entry"> コードポイント（16進） </th> 
   <th colname="col3" class="entry"> コードポイント（12月） </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>空白文字 </p> </td> 
   <td colname="col2"> <p>20 </p> </td> 
   <td colname="col3"> <p>32 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&lt; </p> </td> 
   <td colname="col2"> <p>3C </p> </td> 
   <td colname="col3"> <p>60 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&gt; </p> </td> 
   <td colname="col2"> <p>3E </p> </td> 
   <td colname="col3"> <p>62 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>" </p> </td> 
   <td colname="col2"> <p>22 </p> </td> 
   <td colname="col3"> <p>34 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p># </p> </td> 
   <td colname="col2"> <p>23 </p> </td> 
   <td colname="col3"> <p>35 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>% </p> </td> 
   <td colname="col2"> <p>25 </p> </td> 
   <td colname="col3"> <p>37 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>{ </p> </td> 
   <td colname="col2"> <p>7B </p> </td> 
   <td colname="col3"> <p>123 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>} </p> </td> 
   <td colname="col2"> <p>7D </p> </td> 
   <td colname="col3"> <p>125 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>| </p> </td> 
   <td colname="col2"> <p>7C </p> </td> 
   <td colname="col3"> <p>124 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>\ </p> </td> 
   <td colname="col2"> <p>5C </p> </td> 
   <td colname="col3"> <p>92 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>^ </p> </td> 
   <td colname="col2"> <p>5E </p> </td> 
   <td colname="col3"> <p>94 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~ </p> </td> 
   <td colname="col2"> <p>7E </p> </td> 
   <td colname="col3"> <p>126 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[ </p> </td> 
   <td colname="col2"> <p>5B </p> </td> 
   <td colname="col3"> <p>91 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>] </p> </td> 
   <td colname="col2"> <p>5D </p> </td> 
   <td colname="col3"> <p>93 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>` </p> </td> 
   <td colname="col2"> <p>60 </p> </td> 
   <td colname="col3"> <p>96 </p> </td> 
  </tr> 
 </tbody> 
</table>

予約文字もエンコードする必要があります。

<table id="table_A6C808A05EA6420F8125186D3D5C9E33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 予約文字 </th> 
   <th colname="col2" class="entry"> コードポイント（16進） </th> 
   <th colname="col3" class="entry"> コードポイント（12月） </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>$ </p> </td> 
   <td colname="col2"> <p>24 </p> </td> 
   <td colname="col3"> <p>36 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp; </p> </td> 
   <td colname="col2"> <p>26 </p> </td> 
   <td colname="col3"> <p>38 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+ </p> </td> 
   <td colname="col2"> <p>2B </p> </td> 
   <td colname="col3"> <p>43 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>, </p> </td> 
   <td colname="col2"> <p>2C </p> </td> 
   <td colname="col3"> <p>44 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>/ </p> </td> 
   <td colname="col2"> <p>2F </p> </td> 
   <td colname="col3"> <p>47 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>。 </p> </td> 
   <td colname="col2"> <p>3A </p> </td> 
   <td colname="col3"> <p>58 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>; </p> </td> 
   <td colname="col2"> <p>3B </p> </td> 
   <td colname="col3"> <p>59 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>= </p> </td> 
   <td colname="col2"> <p>3D </p> </td> 
   <td colname="col3"> <p>61 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>? </p> </td> 
   <td colname="col2"> <p>3F </p> </td> 
   <td colname="col3"> <p>63 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>@ </p> </td> 
   <td colname="col2"> <p>40 </p> </td> 
   <td colname="col3"> <p>64 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-b85895e5b6a84b96b7fca987656dd34d}

`…&$text=rate&weight=85% 27#&…`

不明化を適用しない場合、上記の要求フラグメントは次のようにエンコードする必要があります。

`…&$text=rate%26weight%3D85%25%2027%23&…`

不明化を適用した場合、エンコーディングでは、「=」、「&amp;」および「%」の文字を削除するように制限できます。

`…&$text=rate%26weight%3D85%25 27#&…`

## 関連項目 {#section-295476ec34c74973962d07dfa9eb2180}

[不明化の要求](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)、 [HTTP/1.1仕様(RFC 2616)](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
