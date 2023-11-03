---
description: 画像サービングは、外部オブジェクト ID をロケール固有のオブジェクト（カタログ）ID に変換するメカニズムを提供します。 主なアプリケーションは、ロケール固有のオブジェクト ID を知る必要のない、ロケール固有のコンテンツとコンテンツを複数のロケールで共有するためのものです。
solution: Experience Manager
title: オブジェクト ID の変換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 9%

---

# オブジェクト ID の変換{#object-id-translation}

画像サービングは、外部オブジェクト ID をロケール固有のオブジェクト（カタログ）ID に変換するメカニズムを提供します。 主なアプリケーションは、ロケール固有のオブジェクト ID を知る必要のない、ロケール固有のコンテンツとコンテンツを複数のロケールで共有するためのものです。

アプリケーションは、グローバルオブジェクト ID のみを使用して記述でき、画像サービングは、使用可能な場合は、ロケール固有の画像とその他のコンテンツを自動的に置き換えます。

The *`locale`* が画像サービング要求で指定され、 `locale=` コマンドを使用します。

>[!NOTE]
>
>オブジェクト ID の変換は、画像サービングのカタログベースでの使用にのみ適用できます。 ファイル名は翻訳できません。

## 範囲 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

画像、SVG、および静的コンテンツカタログ内のエントリへの参照は、翻訳フォントと ICC プロファイルの参照に対しては、すべて翻訳されません。 また、 *`object`* ～の道のりで [!DNL /is/image] および [!DNL /is/static requests]の場合、これらのコマンドとカタログ属性は ID 変換の対象になります。 `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage`、および `attribute::Watermark`.

## ID 変換マップ {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` 汎用オブジェクト ID と `locale=` の値です。

`attribute::LocaleMap` 入力のリストで構成されます *ロケール* ( `locale=`) の代わりに、1 つ以上の出力ロケールのサフィックス ( `*`locSuffixes`*`) をクリックします。

例： `attribute::LocaleMap` 次のようになります。

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

リクエスト `/is/image/myCat/myImg?locale=de_de` は、カタログエントリに関連付けられた画像を返します。 `myCat/myImg_D` （このようなカタログエントリが存在する場合）。

詳しくは、 `attribute::LocaleMap` 」を参照してください。

## 翻訳プロセス {#section-1f64db17e9f644d88e09853670e14a16}

上記の例では、サーバーはまず *`locale`* &quot; `de_de`」と入力します。 次に、 *`locSuffixes`* このエントリに関連付けられています。この場合は&quot; `_D`&quot;と&quot;&quot;（空のサフィックス） 繰り返しごとに、サフィックスが画像 ID に追加され、カタログ内での存在がテストされた結果の ID が追加されます。 見つかった場合は、そのカタログエントリが使用され、それ以外の場合は、次のカタログエントリがテストされます。 この例では、次のエントリがチェックされます。 `myCat/myImg_D`、および `myCat/myImg`. 一致する画像が見つからない場合、サーバーはエラーまたはデフォルトの画像（設定されている場合）を返します。

## 不明なロケール {#section-b2f3c83f2dc845d69b5908107b775537}

上記の例では、 `attribute::LocaleMap` 空を含む *`locale`* デフォルトの翻訳ルールを定義し、不明な場合に使用します。 `locale=` の値（つまり、翻訳マップに明示的にリストされていない値）に基づいて行われます。 この翻訳マップがリクエストに適用された場合 `/is/image/myCat/myImg?locale=ja`の場合、 `myCat/myImg_E`存在する場合は、存在する場合は、それ以外の場合は `myCat/myImg`.

翻訳マップでデフォルトの翻訳ルールが指定されていない場合は、不明なすべてのリクエストに対してエラーが返されます `locale=` 値。

## 例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**複数層の参照**

地域の標準に対応するために、ロケール（ヨーロッパ、中東、北米など）をグループ化することが望ましい場合も多いです。 これは、複数層のルックアップを使用して実現できます。

この例では、西部および中東部で使用するコレクションをサポートします。 どちらのコレクションも汎用の画像コレクションに基づいて作成し、いくつかの画像を追加または変更します。次に、両方のコレクションが特定のロケール用にさらに絞り込まれます ( `m1`, `m2` 中東の 2 つの亜種に対して `w1`, `w2`、および `w3` （3 つの西側のロケールの場合）、ただし、画像が `w1` および `w3`. 不明なロケールは汎用のコレクションのみにマッピングされ、ロケール固有の画像にはアクセスされません。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

次の表に、どのカタログエントリを考慮するか、および汎用入力 ID に対してエントリを考慮する順序を示します `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>検索するカタログ ID</b> </th> 
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
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**特定の ID の検索**

一部の画像の命名規則では、内部的に汎用の画像 ID をサポートしていない場合があります。 要求の汎用 ID は、常にカタログ内の特定の ID にマッピングする必要があります。多くの場合、正確な特定の ID が不明な場合があります。

この例では、すべての言語の画像に `_1`, `_2`または `_3` サフィックス フランス語のロケールに固有の画像には、 `_22` または `_23` サフィックスと、ドイツ語のロケールに固有の画像には、 `_470` または `_480` サフィックス

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

次の表に、どのカタログエントリを考慮するか、および汎用入力 ID に対してエントリを考慮する順序を示します `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>検索する出力 ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>その他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 関連項目 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
