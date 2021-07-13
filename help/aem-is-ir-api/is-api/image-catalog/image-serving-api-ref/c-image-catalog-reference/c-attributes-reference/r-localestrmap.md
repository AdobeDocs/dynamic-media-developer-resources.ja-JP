---
description: 文字列変換マップ。 任意の数のinternalLocIdにマッピングできるlocIdを参照します。
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# LocaleStrMap{#localestrmap}

文字列変換マップ。 任意の数のinternalLocIdにマッピングできるlocIdを参照します。

`*``*&#42;['|' *`itemitem`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 品目 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale  </span>,  <span class="varname"> locId  </span>*[','  <span class="varname"> locId  </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>ロケール（大文字と小文字は区別されません）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId  </span> </p> </td> 
  <td class="stentry"> <p>内部ロケールID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap` は、任意の数 `locId` のにマッピングできるを指しま `internalLocId`す。

空の&#x200B;*`locale`*&#x200B;値は、空および不明な`locale=`文字列と一致します。 これにより、不明なロケールに対するデフォルトのルールを定義できます。

空の&#x200B;*`locId`*&#x200B;値が許可され、*`defaultString`*&#x200B;を選択します（*`defaultString`*&#x200B;にはロケール識別子はありません）。 *`locId`* の値は、指定した順序で検索されます。最初の一致が返されます。

文字列の翻訳を有効にすると、次の画像カタログフィールドのテキスト文字列に適用されます。

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>カタログフィールド</b> </td> 
   <td> <b>フィールド内の文字列要素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet  </span> </p> </td> 
   <td> <p>翻訳可能な文字列を含むサブ要素（区切り文字「,」「;」「:」やフィールドの開始/終了の組み合わせで区切られます）。 </p> <p>ローカライズ可能フィールドの先頭の<span class="codeph"> 0xrrggbb </span>カラー値は、ローカライゼーションから除外され、変更なしで渡されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Map  </span> </p> </td> 
   <td> <p><span class="codeph"> coords= </span>および<span class="codeph"> shape= </span>属性の値を除く、一重引用符または二重引用符で囲まれた属性値。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Targets  </span> </p> </td> 
   <td> <p><span class="filepath">ターゲットの値。*.label </span>と<span class="filepath">ターゲット。*.userdata </span>プロパティを追加します。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData  </span> </p> </td> 
   <td> <p>プロパティの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8505a8525f6948ada3979f68c4081044}

1つ以上の項目( |（各項目は、コンマ区切りの2つ以上の文字列値で構成されます）。

## 関連項目 {#section-0c0516e4f83d42d38247308cab9b6708}

ローカリゼーションのサポート， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog:userData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
