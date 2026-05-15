---
description: Image Servingは、外部オブジェクト IDをロケール固有のオブジェクト（カタログ） IDに変換するメカニズムを提供します。 主なアプリケーションは、クライアントアプリケーションがロケール固有のオブジェクト IDを知らなくても、ロケール固有のコンテンツと複数のロケール間で共有されるコンテンツを提供するためのものです。
solution: Experience Manager
title: オブジェクト IDの翻訳
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
TQID: 'https://experienceleague.adobe.com/jeFY6jJ5HJ4mPK6ng93G9PZ6ENSlk7Wtj8S-GTdMJbM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 715
ht-degree: 5%

---

# オブジェクト IDの翻訳{#object-id-translation}

Image Servingは、外部オブジェクト IDをロケール固有のオブジェクト（カタログ） IDに変換するメカニズムを提供します。 主なアプリケーションは、クライアントアプリケーションがロケール固有のオブジェクト IDを知らなくても、ロケール固有のコンテンツと複数のロケール間で共有されるコンテンツを提供するためのものです。

アプリケーションはグローバルオブジェクト IDのみを使用して書き込むことができ、画像サービングは、ロケール固有の画像やその他のコンテンツが利用可能な場合に自動的に置き換えられます。

*`locale`*&#x200B;は、`locale=` コマンドを使用して画像サービング要求で指定されます。

>[!NOTE]
>
>オブジェクト IDの翻訳は、画像サービングのカタログベースの使用にのみ適用されます。 ファイル名は翻訳できません。

## 範囲 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

画像、SVGおよび静的コンテンツカタログ内のエントリに対するすべての参照は、翻訳フォントに対して考慮され、ICC プロファイル参照は翻訳されません。 [!DNL /is/image]および[!DNL /is/static requests]のパスの&#x200B;*`object`*&#x200B;に加えて、これらのコマンドおよびカタログ属性は、ID翻訳の対象となります：`src=`、`mask=`、`template=`、`defaultImage=`、`attribute::DefaultImage`、および`attribute::Watermark`。

## ID翻訳マップ {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap`は、汎用オブジェクト IDと`locale=`値の入力として指定された、ローカライズされたコンテンツのIDを決定するためにサーバーが使用するルールを定義します。

`attribute::LocaleMap`は、入力&#x200B;*ロケール* （`locale=`で指定された値に一致）のリストで構成され、それぞれに出力ロケールのサフィックスが付いていません（`*`locSuffixes`*`）。

例えば、`attribute::LocaleMap`は次のようになります。

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

リクエスト `/is/image/myCat/myImg?locale=de_de`は、カタログエントリ `myCat/myImg_D`に関連付けられた画像を返します（そのようなカタログエントリが存在すると仮定します）。

詳しくは、`attribute::LocaleMap`の説明を参照してください。

## 翻訳プロセス {#section-1f64db17e9f644d88e09853670e14a16}

上記の例を考えると、サーバーは最初にID翻訳マップで&#x200B;*`locale`* 「`de_de`」を検索します。 次に、この場合は「`_D`」と「」（空のサフィックス）のエントリに関連付けられた&#x200B;*`locSuffixes`*&#x200B;を繰り返します。 各反復に対して、サフィックスが画像IDに追加され、結果のIDがカタログ内に存在するかどうかをテストされます。 見つかった場合は、そのカタログのエントリが使用され、それ以外の場合は次のエントリがテストされます。 この例では、次のエントリがチェックされます：`myCat/myImg_D`、および`myCat/myImg`。 一致するものが見つからない場合、サーバーはエラーまたはデフォルトの画像（設定されている場合）を返します。

## 不明なロケール {#section-b2f3c83f2dc845d69b5908107b775537}

上記の例では、`attribute::LocaleMap`には、不明な`locale=`値（つまり、翻訳マップに明示的にリストされていない値）に使用されるデフォルトの翻訳ルールを定義する空の&#x200B;*`locale`*&#x200B;が含まれています。 この翻訳マップがリクエスト `/is/image/myCat/myImg?locale=ja`に適用された場合、この翻訳マップは`myCat/myImg_E`、存在する場合、または存在しない場合は`myCat/myImg`に解決されます。

翻訳マップでデフォルトの翻訳ルールが指定されていない場合、不明な`locale=`値を持つすべてのリクエストに対してエラーが返されます。

## 例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多層検索**

地域の標準に対応するために、ロケール（ヨーロッパ、中東、北米など）をグループ化することがしばしば望ましいです。 これを実現するには、多層検索を使用します。

この例では、欧米と中東のコレクションをサポートします。 どちらのコレクションも汎用の画像コレクションに基づいて作成し、いくつかの画像を追加または変更します。 画像が`w1`と`w3`で共有される場合を除き、両方のコレクションは、特定のロケール（`m1`、`m2`、2つの中東のバリエーション、および`w1`、`w2`、および`w3`）に対してさらに絞り込まれます。 不明なロケールは汎用のコレクションのみにマッピングされ、ロケール固有の画像にはアクセスされません。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

次の表は、どのカタログ エントリが考慮され、それらが汎用入力ID `myImg`に対して考慮される順序を示しています。

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> ロケール </i> </b> </th> 
   <th class="entry"> <b>検索するカタログ ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1、w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W、myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2、myImg-W、myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1、myImg-M、myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2、myImg-M、myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>その他 </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**特定のIDを検索**

一部の画像命名規則では、内部で汎用画像IDをサポートしていない場合があります。 リクエストの汎用IDは、常にカタログ内の特定のIDにマッピングする必要があります。多くの場合、正確な特定のIDが分からない場合があります。

この例では、すべての言語の画像に`_1`、`_2`または`_3`のサフィックスが付いている場合があります。 フランス語ロケール固有の画像には`_22`または`_23`のサフィックスが付いている場合があり、ドイツ語ロケール固有の画像には`_470`または`_480`のサフィックスが付いている場合があります。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

次の表は、どのカタログ エントリが考慮され、それらが汎用入力ID `myImg`に対して考慮される順序を示しています。

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> ロケール </i> </b> </th> 
   <th class="entry"> <b>検索する出力ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> </span>の<span class="codeph"> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22、myImg_23、myImg_1、myImg_2、myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470、myImg_480、myImg_1、myImg_2、myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>その他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1、myImg_2、myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 関連項目 {#section-05893816c66a406d89f9bfd6ace8d47a}

[属性：:LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)、[属性：:DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b)、[locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)、[req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
