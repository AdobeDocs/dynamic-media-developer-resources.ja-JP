---
description: 文字列変換マップ。 任意の数のinternalLocIdにマップできるlocIdを参照します。
seo-description: 文字列変換マップ。 任意の数のinternalLocIdにマップできるlocIdを参照します。
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# LocaleStrMap{#localestrmap}

文字列変換マップ。 任意の数のinternalLocIdにマップできるlocIdを参照します。

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

`LocaleStrMap` は、任意の数 `locId` にマップできる `internalLocId`。

空の&#x200B;*`locale`*&#x200B;値は、空および不明な`locale=`文字列と一致します。 これにより、不明なロケールに対するデフォルトのルールを定義できます。

空の&#x200B;*`locId`*&#x200B;値を許可し、*`defaultString`*&#x200B;を選択します（*`defaultString`*&#x200B;にはロケール識別子がありません）。 *`locId`* の値は、指定された順序で検索されます。最初の一致が返されます。

文字列変換は、有効な場合、次の画像カタログフィールド内のテキスト文字列に適用されます。

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>カタログフィールド</b> </td> 
   <td> <b>フィールド内の文字列要素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet  </span> </p> </td> 
   <td> <p>変換可能な文字列を含むサブ要素(区切り文字「,」、「;」、「:」、フィールドの開始/終了」、またはその両方の組み合わせで区切られます)。 </p> <p>ローカライズ可能なフィールドの先頭の<span class="codeph"> 0xrrggbb </span>カラー値は、ローカライゼーションから除外され、変更せずに渡されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Map  </span> </p> </td> 
   <td> <p><span class="codeph"> coords= </span>および<span class="codeph"> shape= </span>属性の値を除く、単一または重複で引用符で囲まれた任意の属性値。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ターゲット  </span> </p> </td> 
   <td> <p><span class="filepath">ターゲットの値。*.label </span>と<span class="filepath">ターゲット。*.userdata </span>プロパティ。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData  </span> </p> </td> 
   <td> <p>任意のプロパティの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8505a8525f6948ada3979f68c4081044}

1つ以上の項目、区切り |を指定します。各項目は、コンマ区切りの2つ以上の文字列値で構成されます。

## 関連項目 {#section-0c0516e4f83d42d38247308cab9b6708}

ローカライゼーションのサポート， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::ターゲット](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [カタログ：userData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
