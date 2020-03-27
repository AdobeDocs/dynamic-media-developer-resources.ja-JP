---
description: 文字列変換マップ。 任意の数のinternalLocIdにマップできるlocIdを参照します。
seo-description: 文字列変換マップ。 任意の数のinternalLocIdにマップできるlocIdを参照します。
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# LocaleStrMap{#localestrmap}

文字列変換マップ。 任意の数のinternalLocIdにマップできるlocIdを参照します。

` *`項`*&#42;['|' *`目`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 品目 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale </span>、 <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>ロケール（大文字と小文字は区別されません）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>内部ロケールID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap` は、任意の数 `locId` のにマップできるを指します `internalLocId`。

空の値は、空 *`locale`* の文字列と不明な文字列に一致 `locale=` します。 これにより、不明なロケールのデフォルトのルールを定義できます。

空の *`locId`* 値を許可し、を選択しま *`defaultString`* す(ロ *`defaultString`* ケール識別子がない)。 *`locId`* の値は、指定された順序で検索されます。 最初の一致が返されます。

文字列変換を有効にすると、次の画像カタログフィールドのテキスト文字列に適用されます。

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>カタログフィールド</b> </td> 
   <td> <b>フィールド内の文字列要素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>変換可能な文字列を含むサブ要素（区切り文字「,」「;」「:」またはフィールドの開始/終了、あるいはその両方で区切られます）。 </p> <p>ローカライズ <span class="codeph"> 可能なフィー </span> ルドの最初にある0xrrggbbカラー値は、ローカリゼーションから除外され、変更なしで渡されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>coords=属性とshape=属性の値を除く、単一引用符または二重 <span class="codeph"> 引用符で囲ま </span> れた任 <span class="codeph"> 意の属 </span> 性値。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>任意のターゲットの <span class="filepath"> 値。*.labelと </span> target <span class="filepath"> 。*.userdataプロパ </span> ティ。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>任意のプロパティの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8505a8525f6948ada3979f68c4081044}

1つ以上の項目(|を参照してください。各項目は、コンマで区切られた複数の文字列値で構成されます。

## 関連項目 {#section-0c0516e4f83d42d38247308cab9b6708}

Localization Support [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), catalog:SetSet [,](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)catalog:MapSet, [](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)[](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)[catalog:MapTargets, Catalog:MapTargets, Catalog:MapTargets,Catalog:Localization,UserCatalog:Data](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
