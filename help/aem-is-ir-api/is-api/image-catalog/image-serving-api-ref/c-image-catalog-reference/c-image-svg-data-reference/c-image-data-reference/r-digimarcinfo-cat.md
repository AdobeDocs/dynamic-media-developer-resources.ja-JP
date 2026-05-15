---
title: DigimarcInfo
description: Digimarc画像情報。 Digimarc埋め込みを有効にし、透かしの種類と関連する画像固有のデータを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 87f4d8f0-02b9-4511-9151-89c58116c78d
TQID: 'https://experienceleague.adobe.com/q50ZkCNO7xYJVVyfWgqu-BgxEd8HEZkI7uDX4jv8-ps'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 242
ht-degree: 9%

---

# DigimarcInfo{#digimarcinfo}

Digimarc画像情報。 Digimarc埋め込みを有効にし、透かしの種類と関連する画像固有のデータを指定します。

## プロパティ {#section-62af219e8bac422b8541841221c9ce4f}

コンマで区切られた4つの整数値。

`*`type`*, *`flags`*, *`val1`*, *`val2`*`

`*`type`*`は、Digimarc埋め込みを有効にし、透かしの種類を指定します。

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><b>透かしタイプ </b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>基本： </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>画像ID: </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>トランザクション ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>著作権年。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`flags`*`は、3つの値を持つビット フィールドです。 ビット 0をコピーで保護されたコンテンツを示し、ビット 1を制限されたコンテンツを示し、ビット 2をアダルトコンテンツを示すように設定します。

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> フラグ </span> </span> </p> </th> 
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
   <td> <p>コピー保護： </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>制限付き： </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>コピー保護され、制限されています。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>成熟したコンテンツ： </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>保護されたアダルトコンテンツをコピー。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>制限付きアダルトコンテンツ： </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>コピー保護され、制限された、成熟したコンテンツ： </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`val1`*`と`*`val2`*`の解釈は、`*`type`*`によって異なります。

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1 </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2 </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>未使用： </p> </td> 
   <td> <p>未使用： </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>未使用： </p> </td> 
   <td> <p>未使用： </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>画像ID: </p> </td> 
   <td> <p>未使用： </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>トランザクション ID。 </p> </td> 
   <td> <p>未使用： </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>最初の著作権年。 </p> </td> 
   <td> <p>2回目の著作権年。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 初期設定 {#section-4bb97e5f79074be89cc691e73449eb43}

フィールドが存在しない場合、またはフィールドが空の場合、属性：:DigimarcInfoから継承されます。

## 例 {#section-0f14727a0a2a408781c9df71fed7f42d}

「0,0,0,0」は、この画像のDigimarc透かしを無効にします。

「1,5,0,0」は、アダルトおよびコピーで保護されたコンテンツフラグが設定された基本的な透かしを指定します。

「2,0,4567,0」は、画像IDを持つ透かしを指定します。

「3,2,56483,0」は、トランザクション IDと制限付きコンテンツフラグが設定された透かしを指定します。

「4,0,1998,2001」は、著作権年を含む透かしを指定します。

## 関連項目 {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[属性：:DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667)、[属性：:DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
