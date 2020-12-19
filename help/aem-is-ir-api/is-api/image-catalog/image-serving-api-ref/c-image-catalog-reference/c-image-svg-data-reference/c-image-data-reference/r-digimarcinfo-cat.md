---
description: Digimarc画像情報 Digimarc埋め込みを有効にし、透かしの種類と関連する画像固有のデータを指定します。
seo-description: Digimarc画像情報 Digimarc埋め込みを有効にし、透かしの種類と関連する画像固有のデータを指定します。
seo-title: DigimarcInfo
solution: Experience Manager
title: DigimarcInfo
topic: Scene7 Image Serving - Image Rendering API
uuid: 8371880e-47df-4333-b8a6-91feaf16c409
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 12%

---


# DigimarcInfo{#digimarcinfo}

Digimarc画像情報 Digimarc埋め込みを有効にし、透かしの種類と関連する画像固有のデータを指定します。

## プロパティ {#section-62af219e8bac422b8541841221c9ce4f}

カンマで区切られた4つの整数値。

` *``*, *``*, *`typeflagsval1`*, *`val2`*`

` *`typeenables Digimarc埋め込みを有効にし、透かしの種類を次のように指定します。`*` 

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><b>透かしのタイプ</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>基本. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>画像 ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>トランザクションID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>著作権年 </p> </td> 
  </tr> 
 </tbody> 
</table>

` *``*` フラグは、3つの値を持つビットフィールドです。ビット0はコピー保護されたコンテンツを示し、ビット1は制限付きコンテンツを示し、ビット2は成人向けコンテンツを示します。

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> flags</span> </span> </p> </th> 
   <th class="entry"> <p><b>説明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>コピー保護。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>制限付き </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>コピー保護、制限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>成熟したコンテンツ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>保護された成人向けのコンテンツのコピー </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>制限付きアダルトコンテンツ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>コピー保護、制限付き、成熟したコンテンツ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

` *`val1`*`と` *`val2`*`の解釈は、` *`type`*`に依存します。

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1  </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2  </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>未使用。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>未使用。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>画像 ID. </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>トランザクションID。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>第1著作権年。 </p> </td> 
   <td> <p>第2著作権年。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 初期設定 {#section-4bb97e5f79074be89cc691e73449eb43}

フィールドが存在しない場合、または空の場合は、attribute::DigimarcInfoから継承します。

## 例 {#section-0f14727a0a2a408781c9df71fed7f42d}

「0,0,0,0」を指定すると、この画像のDigimarc透かしが無効になります。

「1,5,0,0」は、大人向けとコピー保護されたコンテンツフラグが設定された基本的な透かしを指定します。

「2,0,4567,0」は、画像IDを持つ透かしを指定します。

「3,2,56483,0」は、トランザクションIDと制限付きコンテンツフラグが設定された透かしを指定します。

「4,0,1998,2001」は著作権年を示す透かしを指定します。

## 関連項目 {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) ,  [attribute::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
