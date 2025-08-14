---
description: 画像サービングは、外部オブジェクト ID をロケール固有のオブジェクト（カタログ） ID に変換するメカニズムを提供します。 主なアプリケーションは、クライアントアプリケーションがロケール固有のオブジェクト ID を知る必要なく、ロケール固有のコンテンツと、複数のロケール間で共有されるコンテンツを提供することです。
solution: Experience Manager
title: オブジェクト ID 変換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 2%

---

# オブジェクト ID 変換{#object-id-translation}

画像サービングは、外部オブジェクト ID をロケール固有のオブジェクト（カタログ） ID に変換するメカニズムを提供します。 主なアプリケーションは、クライアントアプリケーションがロケール固有のオブジェクト ID を知る必要なく、ロケール固有のコンテンツと、複数のロケール間で共有されるコンテンツを提供することです。

アプリケーションはグローバルオブジェクト ID のみを使用して記述でき、画像サービングは自動的にロケール固有の画像や他のコンテンツ（使用可能な場合）を置き換えます。

*`locale`* は、画像サービングリクエストで `locale=` コマンドを使用して指定します。

>[!NOTE]
>
>オブジェクト ID 変換は、画像サービングのカタログベースの使用にのみ適用されます。 ファイル名は翻訳できません。

## 範囲 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

画像、SVG、静的コンテンツカタログ内のエントリへのすべての参照は翻訳フォントに考慮され、ICC プロファイル参照は翻訳されません。 *`object`* と [!DNL /is/image] のパスの [!DNL /is/static requests] に加えて、これらのコマンドとカタログ属性は、ID 変換の対象となります（`src=`、`mask=`、`template=`、`defaultImage=`、`attribute::DefaultImage` および `attribute::Watermark`）。

## ID 翻訳マップ {#section-9e417b352c314dfe94e831fdd62cddc8}

汎用オブジェクト ID と `attribute::LocaleMap` 値の入力として指定される、ローカライズされたコンテンツの ID を決定するためにサーバーで使用されるルールを `locale=` で定義します。

`attribute::LocaleMap` は、入力 *ロケール* のリスト（`locale=` で指定された値に一致）で構成され、それぞれに出力ロケールのサフィックスが 1 つ以上ありません（`*`locSuffixes`*`）。

例えば、次のよ `attribute::LocaleMap` になります。

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

リクエスト `/is/image/myCat/myImg?locale=de_de` は、カタログエントリ `myCat/myImg_D` に関連付けられた画像を返します（そのようなカタログエントリが存在すると仮定）。

詳しくは、`attribute::LocaleMap` の説明を参照してください。

## 翻訳プロセス {#section-1f64db17e9f644d88e09853670e14a16}

上記の例では、サーバーは最初に ID 翻訳マップ内で *`locale`* 「`de_de`」を検索します。 次に、このエントリに関連付けられた *`locSuffixes`* （この場合は「`_D`」と「」（空のサフィックス））を反復します。 イテレーションごとに、画像 ID と結果の ID にサフィックスが追加され、カタログ内の存在がテストされます。 見つかった場合は、そのカタログエントリが使用され、見つからなかった場合は、次のカタログエントリがテストされます。 この例では、`myCat/myImg_D` および `myCat/myImg` のエントリがチェックされます。 一致するものが見つからない場合、サーバーはエラーまたはデフォルトの画像（設定されている場合）を返します。

## 不明なロケール {#section-b2f3c83f2dc845d69b5908107b775537}

上記の例では、`attribute::LocaleMap` にはデフォルトの翻訳ルールを定義する空の *`locale`* が含まれています。これは不明な `locale=` 値（つまり、翻訳マップに明示的にリストされていない値）に使用されます。 この翻訳マップがリクエスト `/is/image/myCat/myImg?locale=ja` に適用された場合は、存在する場合は `myCat/myImg_E` に解決され、存在しない場合は `myCat/myImg` に解決されます。

翻訳マップにデフォルトの翻訳ルールが指定されていない場合、`locale=` 値が不明なすべてのリクエストに対してエラーが返されます。

## 例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多層検索**

地域の基準に対応するために、ロケール（例：ヨーロッパ、中東、北米）をグループ化することが望ましい場合が多くあります。 これは、複数層のルックアップを使用して実現できます。

この例では、西および中東での使用に対応するコレクションをサポートします。 どちらのコレクションも汎用の画像コレクションに基づいて作成し、いくつかの画像を追加または変更します。その後、画像を `m1` と `m2` で共有する場合を除き、両方のコレクションが特定のロケール（中東の 2 つのバリアントには `w1`、`w2`、西洋の 3 つのロケールには `w3`、`w1` および `w3`）に対してさらに絞り込まれます。 不明なロケールは汎用コレクションにのみマッピングされ、ロケール固有の画像にはアクセスできません。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

次の表に、一般的な入力 ID `myImg` に対して考慮されるカタログエントリと、それらのエントリが考慮される順序を示します。

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b> 検索するカタログ ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> myImg-W2、myImg-W、myImg <span class="codeph"> の </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> myImg-M1、myImg-M、myImg <span class="codeph"> の </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> myImg-M2、myImg-M、myImg <span class="codeph"> の </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>その他すべて </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**特定の ID の検索**

一部の画像命名規則では、汎用画像 ID を内部でサポートしていない場合があります。 リクエストの汎用 ID は、常にカタログ内の特定の ID にマッピングする必要があります。正確な特定の ID が不明な場合もよくあります。

この例では、すべての言語の画像に `_1`、`_2` または `_3` のサフィックスを付けることができます。 フランス語のロケールに固有の画像には `_22` または `_23` サフィックスが付き、ドイツ語のロケールに固有の画像には `_470` または `_480` サフィックスが付きます。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

次の表に、一般的な入力 ID `myImg` に対して考慮されるカタログエントリと、それらのエントリが考慮される順序を示します。

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b> 検索する出力 ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph">_22、myImg_23、myImg_1、myImg_2、myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> myImg_470, myImg_480, myImg_1, myImg_2, myImg_3 <span class="codeph"> を </span> します </p> </td> 
  </tr> 
  <tr> 
   <td> <p>その他すべて </p> </td> 
   <td> <p> myImg_1、myImg_2、myImg_3<span class="codeph"> を </span> します </p> </td> 
  </tr> 
 </tbody> 
</table>

## 関連項目 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)、[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b)、[locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)、[req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
