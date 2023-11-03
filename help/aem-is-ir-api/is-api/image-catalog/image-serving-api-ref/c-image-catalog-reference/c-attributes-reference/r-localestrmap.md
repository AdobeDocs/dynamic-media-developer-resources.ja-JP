---
description: 文字列翻訳マップ。 任意の数の internalLocId にマッピングできる locId を参照します。
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# LocaleStrMap{#localestrmap}

文字列翻訳マップ。 任意の数の internalLocId にマッピングできる locId を参照します。

`*`項目`*&#42;['|' *`項目`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 品目 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> ロケール </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>ロケール（大文字と小文字を区別しない）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>内部ロケール ID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap` は、 `locId` 任意の数の `internalLocId`.

空の *`locale`* 値が空と不明に一致する `locale=` 文字列。 これにより、不明なロケールに対するデフォルトのルールを定義できます。

空 *`locId`* 値を許可し、 *`defaultString`* ( *`defaultString`* はロケール識別子を持ちません )。 *`locId`* 値は指定した順序で検索されます。 最初の一致が返されます。

文字列翻訳を有効にすると、次の画像カタログフィールド内のテキスト文字列に適用されます。

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>カタログフィールド</b> </td> 
   <td> <b>フィールドの文字列要素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>翻訳可能な文字列を含むサブ要素（区切り文字「,」、「;」、「:」、フィールドの開始/終了の組み合わせで区切られます）。 </p> <p>A <span class="codeph"> 0xrrggbb </span> ローカライズ可能フィールドの先頭の色の値は、ローカライゼーションから除外され、変更されずに渡されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>引用符で囲まれた単一または二重引用符で囲まれた任意の属性値 ( <span class="codeph"> coords= </span> および <span class="codeph"> shape= </span> 属性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>任意の <span class="filepath"> ターゲット。*.label </span> および <span class="filepath"> ターゲット。*.userdata </span> プロパティ。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>任意のプロパティの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8505a8525f6948ada3979f68c4081044}

1 つ以上の項目（で区切る） |。各項目は 2 つ以上のコンマ区切りの文字列値で構成されます。

## 関連項目 {#section-0c0516e4f83d42d38247308cab9b6708}

ローカリゼーションサポート [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
