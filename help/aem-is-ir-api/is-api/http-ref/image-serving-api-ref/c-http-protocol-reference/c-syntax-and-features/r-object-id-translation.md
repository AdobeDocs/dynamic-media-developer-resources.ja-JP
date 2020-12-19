---
description: 画像サービングには、外部オブジェクトIDをロケール固有のオブジェクト（カタログ）IDに変換するメカニズムが用意されています。 主なアプリケーションは、ロケール固有のコンテンツと、複数のロケールで共有されるコンテンツを提供するためのもので、クライアントアプリケーションはロケール固有のオブジェクトIDを知る必要はありません。
seo-description: 画像サービングには、外部オブジェクトIDをロケール固有のオブジェクト（カタログ）IDに変換するメカニズムが用意されています。 主なアプリケーションは、ロケール固有のコンテンツと、複数のロケールで共有されるコンテンツを提供するためのもので、クライアントアプリケーションはロケール固有のオブジェクトIDを知る必要はありません。
seo-title: オブジェクトIDの変換
solution: Experience Manager
title: オブジェクトIDの変換
topic: Scene7 Image Serving - Image Rendering API
uuid: 8b4c2f44-033a-428a-b505-af389865c70a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 9%

---


# オブジェクトIDの変換{#object-id-translation}

画像サービングには、外部オブジェクトIDをロケール固有のオブジェクト（カタログ）IDに変換するメカニズムが用意されています。 主なアプリケーションは、ロケール固有のコンテンツと、複数のロケールで共有されるコンテンツを提供するためのもので、クライアントアプリケーションはロケール固有のオブジェクトIDを知る必要はありません。

アプリケーションは、グローバルオブジェクトIDのみを使用して書き込むことができ、画像サービングは、ロケール固有の画像とその他のコンテンツを自動的に置き換えます（使用可能な場合）。

*`locale`*&#x200B;は、画像サービング要求で`locale=`コマンドと共に指定します。

>[!NOTE]
>
>オブジェクトIDの変換は、画像サービングのカタログベースの使用にのみ適用できます。 ファイル名は変換できません。

## 範囲 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

画像、SVG、静的コンテンツのカタログ内のエントリへの参照は、翻訳フォントに対してはすべて考慮され、ICCプロファイルの参照は変換されません。 [!DNL /is/image]と[!DNL /is/static requests]のパス内の&#x200B;*`object`*&#x200B;に加えて、次のコマンドおよびカタログ属性はID変換の対象となります。`src=`、`mask=`、`template=`、`defaultImage=`、`attribute::DefaultImage`、`attribute::Watermark`。

## ID変換マップ{#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` 汎用オブジェクトIDと `locale=` 値を入力として指定され、サーバーがローカライズされたコンテンツのIDを決定するために使用するルールを定義します。

`attribute::LocaleMap` は、入力 *ロケール* （で指定した値と一致）のリストで構成され、各ロケールには何も出力されない(locSuffixes `locale=` ` *``*`)かそれ以上の出力ロケールサフィックスが含まれます。

例えば、`attribute::LocaleMap`は次のようになります。

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

リクエスト`/is/image/myCat/myImg?locale=de_de`は、カタログエントリ`myCat/myImg_D`に関連付けられた画像を返します（このようなカタログエントリが存在する場合）。

詳細は`attribute::LocaleMap`の説明を参照してください。

## 変換処理{#section-1f64db17e9f644d88e09853670e14a16}

上記の例では、サーバーはまずID変換マップで&#x200B;*`locale`* &quot; `de_de`&quot;を探します。 次に、このエントリに関連付けられた&#x200B;*`locSuffixes`*&#x200B;を繰り返し処理します。この場合は&quot; `_D`&quot;と&quot;&quot; （空のサフィックス）です。 繰り返しごとに、サフィックスが画像IDに追加され、カタログ内に存在するかどうかがテストされた結果のIDが追加されます。 見つかった場合はそのカタログエントリが使用され、それ以外の場合は次のカタログエントリがテストされます。 この例では、次のエントリがチェックされます。`myCat/myImg_D`と`myCat/myImg`。 一致が見つからない場合、サーバーはエラーまたはデフォルトの画像を返します（設定されている場合）。

## 不明なロケール{#section-b2f3c83f2dc845d69b5908107b775537}

上記の例で、`attribute::LocaleMap`には空の&#x200B;*`locale`*&#x200B;が含まれています。この&lt;a1/>は、不明な`locale=`値（つまり、翻訳マップに明示的に指定されていない値）に使用される、デフォルトの変換ルールを定義します。 この変換マップがリクエスト`/is/image/myCat/myImg?locale=ja`に適用された場合、`myCat/myImg_E`に解決されます（存在する場合）。それ以外の場合は`myCat/myImg`に解決されます。

変換マップでデフォルトの変換ルールが指定されていない場合、`locale=`値が不明なすべてのリクエストに対してエラーが返されます。

## 例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多層検索**

ロケール（ヨーロッパ、中東、北米など）をグループ化して地域の基準に対応することが望ましい場合が多くあります。 これは、多層検索を使用して実現できます。

この例では、西欧で使用するコレクションと中東で使用するコレクションをサポートします。 どちらのコレクションも汎用の画像コレクションに基づいて作成し、いくつかの画像を追加または変更します。次に、両方のコレクションが特定のロケール用にさらに絞り込まれます（2つの中東のバリエーションが`m1`、`m2`、および`w1`、`w2`、`w3`、西欧の3つのロケールが共有されます）。 `w3``w1`不明なロケールは汎用のコレクションのみにマッピングされ、ロケール固有の画像にはアクセスされません。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

次の表に、考慮されるカタログエントリと、汎用入力ID `myImg`に対して考慮される順序を示します。

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>検索するカタログID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>その他 </p> </td> 
   <td> <p> <span class="codeph"> myImg  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**特定のIDの検索**

一部の画像の命名規則では、内部的に汎用の画像IDがサポートされない場合があります。 リクエストの汎用IDは、常にカタログ内の特定のIDにマップする必要があります。正確な特定のIDがわからない場合があります。

この例では、すべての言語の画像に`_1`、`_2`、または`_3`のサフィックスを付けることができます。 フランス語のロケールに固有の画像には`_22`または`_23`のサフィックスを付け、ドイツ語のロケールに固有の画像には`_470`または`_480`のサフィックスを付けることができます。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

次の表に、考慮されるカタログエントリと、汎用入力ID `myImg`に対して考慮される順序を示します。

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>検索する出力ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de  </span>、 <span class="codeph"> de_at  </span>、 <span class="codeph"> de_de  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>その他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 関連項目 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) ,  [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b),  [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb),  [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
