---
title: DigimarcInfo
description: Digimarc 画像情報。 Digimarc 埋め込みを有効にし、透かしの種類と関連する画像固有のデータを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 87f4d8f0-02b9-4511-9151-89c58116c78d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 13%

---

# DigimarcInfo{#digimarcinfo}

Digimarc 画像情報。 Digimarc 埋め込みを有効にし、透かしの種類と関連する画像固有のデータを指定します。

## プロパティ {#section-62af219e8bac422b8541841221c9ce4f}

カンマで区切られた 4 つの整数値。

`*`type`*, *`フラグ`*, *`val1`*, *`val2`*`

`*`type`*` Digimarc 埋め込みを有効にし、透かしの種類を指定します。

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
   <td> <p>トランザクション ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>著作権年。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`フラグ`*` は、3 つの値を持つビットフィールドです。 ビット 0 はコピー保護されたコンテンツを示し、ビット 1 は制限されたコンテンツを示し、ビット 2 は成人向けコンテンツを示します。

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> フラグ</span> </span> </p> </th> 
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
   <td> <p>コピーで保護。 </p> </td> 
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
   <td> <p>コンテンツが完成しました。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>保護された成人向けコンテンツをコピーします。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>制限付き、成人向けコンテンツ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>コピーで保護、制限、成熟したコンテンツ </p> </td> 
  </tr> 
 </tbody> 
</table>

解釈 `*`val1`*` および `*`val2`*` ～に依存する `*`type`*`:

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
   <td> <p>未使用。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>未使用。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>画像 ID. </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>トランザクション ID。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>最初の著作権年。 </p> </td> 
   <td> <p>第 2 著作権年。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 初期設定 {#section-4bb97e5f79074be89cc691e73449eb43}

フィールドが存在しない場合、または空の場合は、attribute::DigimarcInfo から継承されます。

## 例 {#section-0f14727a0a2a408781c9df71fed7f42d}

「0,0,0,0」を指定すると、この画像の Digimarc 透かしが無効になります。

「1,5,0,0」は、成人向けの基本透かしとコピー保護されたコンテンツフラグが設定された基本透かしを指定します。

「2,0,4567,0」は画像 ID を持つ透かしを指定します。

「3,2,56483,0」は、トランザクション ID と制限付きコンテンツフラグが設定された透かしを指定します。

「4,0,1998,2001」は著作権年を示す透かしを指定します。

## 関連項目 {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) , [attribute::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
