---
description: 画像サービングは、外部オブジェクトIDをロケール固有のオブジェクト（カタログ）IDに変換するメカニズムを提供します。 主なアプリケーションは、ロケール固有のオブジェクトIDをクライアントアプリケーションが知る必要なく、ロケール固有のコンテンツとコンテンツを複数のロケールで共有するためのものです。
solution: Experience Manager
title: オブジェクトIDの変換
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 9%

---

# オブジェクトIDの変換{#object-id-translation}

画像サービングは、外部オブジェクトIDをロケール固有のオブジェクト（カタログ）IDに変換するメカニズムを提供します。 主なアプリケーションは、ロケール固有のオブジェクトIDをクライアントアプリケーションが知る必要なく、ロケール固有のコンテンツとコンテンツを複数のロケールで共有するためのものです。

アプリケーションはグローバルなオブジェクトIDのみを使用して書き込むことができ、画像サービングはロケール固有の画像やその他のコンテンツを自動的に置き換えます（使用可能な場合）。

*`locale`*&#x200B;は、画像サービング要求で`locale=`コマンドで指定します。

>[!NOTE]
>
>オブジェクトID変換は、カタログベースの画像サービングでのみ使用できます。 ファイル名は翻訳できません。

## 範囲 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

翻訳フォントとICCプロファイルの参照に関して、画像、SVG、静的コンテンツカタログ内のエントリへの参照はすべて、翻訳対象と見なされません。 [!DNL /is/image]と[!DNL /is/static requests]のパスの&#x200B;*`object`*&#x200B;に加えて、次のコマンドおよびカタログ属性はID変換の対象となります。`src=`、`mask=`、`template=`、`defaultImage=`、`attribute::DefaultImage`、および`attribute::Watermark`です。

## ID変換マップ {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` は、汎用オブジェクトIDと値を入力として指定され、ローカライズされたコンテンツのIDを決定するためにサーバーで使用されるルールを定 `locale=` 義します。

`attribute::LocaleMap` は、入力ロケールのリス *ト* （で指定された値と一致）で構成され、それぞれに出力ロケールのサフィックス(  `locale=`locSuffixes `*``*` )が1つも含まれません。

例えば、`attribute::LocaleMap`は次のようになります。

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

リクエスト`/is/image/myCat/myImg?locale=de_de`は、カタログエントリ`myCat/myImg_D`に関連付けられた画像を返します（このようなカタログエントリが存在する場合）。

詳しくは、`attribute::LocaleMap`の説明を参照してください。

## 翻訳プロセス {#section-1f64db17e9f644d88e09853670e14a16}

上記の例の場合、サーバーはまずID変換マップで&#x200B;*`locale`* &quot; `de_de`&quot;を探します。 次に、このエントリに関連付けられた&#x200B;*`locSuffixes`*&#x200B;を繰り返し処理します。この場合、&quot; `_D`&quot;と&quot;&quot; （空のサフィックス）。 繰り返しごとに、サフィックスが画像IDに追加され、カタログ内での存在がテストされる結果のIDが追加されます。 見つかった場合は、そのカタログエントリが使用され、それ以外の場合は次のエントリがテストされます。 この例では、次のエントリがチェックされます。`myCat/myImg_D`、および`myCat/myImg`。 一致する画像が見つからない場合、サーバーはエラーまたはデフォルトの画像を返します（設定されている場合）。

## 不明なロケール {#section-b2f3c83f2dc845d69b5908107b775537}

上記の例では、`attribute::LocaleMap`に空の&#x200B;*`locale`*&#x200B;が含まれます。これは、不明な`locale=`値（つまり、翻訳マップに明示的にリストされていない値）に使用される、デフォルトの翻訳ルールを定義します。 この翻訳マップがリクエスト`/is/image/myCat/myImg?locale=ja`に適用された場合、`myCat/myImg_E`（存在する場合）または`myCat/myImg`に解決されます。

翻訳マップでデフォルトの翻訳ルールが指定されていない場合、`locale=`値が不明なすべてのリクエストに対してエラーが返されます。

## 例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多層検索**

地域標準に対処するために、ロケール（ヨーロッパ、中東、北米など）をグループ化することが望ましい場合が多いです。 これは、複数層のルックアップを使用して実現できます。

この例では、西部および中東で使用するコレクションをサポートします。 どちらのコレクションも汎用の画像コレクションに基づいて作成し、いくつかの画像を追加または変更します。次に、2つの中東のバリエーションの場合は`m1`、`m2`、3つの西側ロケールの場合は`w1`、`w2`、`w3`といった特定のロケール用に、画像が`w1`と`w3`で共有される点を除き、両方のコレクションがさらに絞り込まれます。 不明なロケールは汎用のコレクションのみにマッピングされ、ロケール固有の画像にはアクセスされません。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

次の表に、どのカタログエントリを考慮するか、および汎用入力ID `myImg`に対してどのカタログエントリを考慮するかの順序を示します。

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

一部の画像の命名規則では、汎用の画像IDが内部でサポートされない場合があります。 要求の汎用IDは、常にカタログ内の特定のIDにマッピングする必要があります。多くの場合、正確な特定のIDが不明な場合があります。

この例では、すべての言語の画像に`_1`、`_2`、`_3`のサフィックスを付けることができます。 フランス語のロケールに固有の画像には`_22`または`_23`のサフィックスを付け、ドイツ語のロケールに固有の画像には`_470`または`_480`のサフィックスを付けることができます。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

次の表に、どのカタログエントリを考慮するか、および汎用入力ID `myImg`に対してカタログエントリを考慮する順序を示します。

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
   <td> <p> <span class="codeph"> de  </span>、  <span class="codeph"> de_at  </span>、  <span class="codeph"> de_de  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>その他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 関連項目 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) 、 [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b)、 [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)、 [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
