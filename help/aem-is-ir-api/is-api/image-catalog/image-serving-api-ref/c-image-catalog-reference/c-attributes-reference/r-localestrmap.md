---
description: 文字列翻訳マップ。 任意の数のinternalLocIdにマッピングできるlocIdを指します。
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
TQID: 'https://experienceleague.adobe.com/tEpdZ-AEabQKLIV1Zkwh9JG7-LHV4gABlmv9PLPqz08'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---

# LocaleStrMap{#localestrmap}

文字列翻訳マップ。 任意の数のinternalLocIdにマッピングできるlocIdを指します。

`*`項目`*&#42;['|' *`項目`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">項目</span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> ロケール </span>、<span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> ロケール </span> </p> </td> 
  <td class="stentry"> <p>ロケール （大文字と小文字は区別されません）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>内部ロケール ID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap`は、任意の数の`internalLocId`にマッピングできる`locId`を指します。

空の&#x200B;*`locale`*&#x200B;値は、空の`locale=`文字列と不明な文字列と一致します。 これにより、不明なロケールに対するデフォルトのルールを定義できます。

空の&#x200B;*`locId`*&#x200B;値を許可し、*`defaultString`*&#x200B;を選択します（*`defaultString`*&#x200B;にはロケール識別子がありません）。 *`locId`*&#x200B;個の値が指定された順序で検索されます。 最初の一致が返されます。

文字列翻訳を有効にすると、次の画像カタログフィールドのテキスト文字列に適用されます。

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b> カタログフィールド </b> </td> 
   <td> フィールド </b>の<b>文字列要素 </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> カタログ：:ImageSet </span> </p> </td> 
   <td> <p>翻訳可能な文字列を含むサブエレメント（区切り記号「,」「;」「:」および/またはフィールドの開始/終了の任意の組み合わせで区切られます）。 </p> <p>ローカライズ可能なフィールドの先頭にある<span class="codeph"> 0xrrggbb </span>のカラー値は、ローカライズから除外され、変更なしで渡されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> カタログ：：マップ </span> </p> </td> 
   <td> <p><span class="codeph"> coords= </span>および<span class="codeph"> shape= </span>属性の値を除く、任意の一重引用符または二重引用符で囲まれた属性値。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> カタログ：：ターゲット </span> </p> </td> 
   <td> <p>任意の<span class="filepath"> target.*.label </span>および<span class="filepath"> target.*.userdata </span> プロパティの値。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> カタログ：:UserData </span> </p> </td> 
   <td> <p>任意のプロパティの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8505a8525f6948ada3979f68c4081044}

1つ以上の項目を|で区切り、各項目が2つ以上のコンマ区切りの文字列値で構成されます。

## 関連項目 {#section-0c0516e4f83d42d38247308cab9b6708}

ローカライゼーションサポート、[locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)、[属性：:LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)、[ カタログ：:ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)、[ カタログ：:Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)、[ カタログ：:Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)、[ カタログ：UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
