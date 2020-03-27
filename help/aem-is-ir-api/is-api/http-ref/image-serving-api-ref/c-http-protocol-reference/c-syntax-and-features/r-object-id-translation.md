---
description: 画像サービングには、外部オブジェクトIDをロケール固有のオブジェクト（カタログ） IDに変換するメカニズムが用意されています。 主なアプリケーションは、ロケール固有のコンテンツと複数のロケールで共有されるコンテンツを提供するためのもので、クライアントアプリケーションはロケール固有のオブジェクトIDを知る必要はありません。
seo-description: 画像サービングには、外部オブジェクトIDをロケール固有のオブジェクト（カタログ） IDに変換するメカニズムが用意されています。 主なアプリケーションは、ロケール固有のコンテンツと複数のロケールで共有されるコンテンツを提供するためのもので、クライアントアプリケーションはロケール固有のオブジェクトIDを知る必要はありません。
seo-title: オブジェクトIDの変換
solution: Experience Manager
title: オブジェクトIDの変換
topic: Scene7 Image Serving - Image Rendering API
uuid: 8b4c2f44-033a-428a-b505-af389865c70a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# オブジェクトIDの変換{#object-id-translation}

画像サービングには、外部オブジェクトIDをロケール固有のオブジェクト（カタログ） IDに変換するメカニズムが用意されています。 主なアプリケーションは、ロケール固有のコンテンツと複数のロケールで共有されるコンテンツを提供するためのもので、クライアントアプリケーションはロケール固有のオブジェクトIDを知る必要はありません。

アプリケーションは、グローバルオブジェクトIDのみを使用して書き込むことができ、画像サービングは、ロケール固有の画像と、使用可能な他のコンテンツを自動的に置き換えます。

は、コ *`locale`* マンドを使用して画像サービング要求で指定 `locale=` します。

>[!NOTE]
>
>オブジェクトIDの変換は、画像サービングのカタログベースの使用にのみ適用されます。 ファイル名は変換できません。

## 範囲 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

画像、SVG、静的コンテンツのカタログ内のエントリへの参照は、すべて変換フォントに対する参照と見なされ、ICCプロファイルの参照は変換されません。 とのパスの内 *`object`* のに加え、次のコ [!DNL /is/image] マンド [!DNL /is/static requests]とカタログ属性はID変換の対象となります。 `src=`、、、、 `mask=`、、 `template=`および `defaultImage=`です `attribute::DefaultImage``attribute::Watermark`。

## ID変換マップ {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` 汎用オブジェクトIDと値の入力として与えられる、ローカライズされたコンテンツのIDを決定するためにサーバーが使用するルールを定義 `locale=` します。

`attribute::LocaleMap` は、入力ロケールのリスト ** (で指定した値と一致する `locale=`)で構成され、各ロケールには出力ロケールサフィックス( ` *`locSuffixes`*`)が1つも含まれていない。

例えば、次のよ `attribute::LocaleMap` うになります。

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

リクエストは、 `/is/image/myCat/myImg?locale=de_de` カタログエントリに関連付けられた画像を返しま `myCat/myImg_D` す（カタログエントリが存在する場合）。

詳しくは、の説明を参照し `attribute::LocaleMap` てください。

## 翻訳プロセス {#section-1f64db17e9f644d88e09853670e14a16}

上記の例では、サーバーはまずID変換マッ *`locale`* プで「 `de_de`」を探します。 次に、このエントリに関連 *`locSuffixes`* 付けられている項目(この場合は&quot; `_D`&quot;と&quot; &quot; （空のサフィックス）)を繰り返し処理します。 繰り返しごとに、サフィックスが画像IDに追加され、カタログ内に存在するかどうかがテストされた結果のIDが追加されます。 見つかった場合は、そのカタログエントリが使用され、それ以外の場合は次のエントリがテストされます。 この例では、次のエントリがチェックされます。、 `myCat/myImg_D`および `myCat/myImg`。 一致が見つからない場合、サーバーはエラーまたはデフォルトの画像（設定されている場合）を返します。

## 不明なロケール {#section-b2f3c83f2dc845d69b5908107b775537}

上の例では、は、不明な値( `attribute::LocaleMap` つまり、翻訳マ *`locale`* ップに明示的にリストされていない値)に使用される、デフォルトの変換ルールを定義する空の変 `locale=` 換を含んでいます。 この翻訳マップがリクエストに適用された場合、 `/is/image/myCat/myImg?locale=ja`存在する場合は、存在する `myCat/myImg_E`場合は、その他の場合に解決されま `myCat/myImg`す。

変換マップでデフォルトの変換ルールが指定されていない場合、不明な値を持つすべてのリクエストに対してエラーが返さ `locale=` れます。

## 例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多層検索**

地域標準に対応するために、ロケール（ヨーロッパ、中東、北米など）をグループ化することが望ましい場合が多いです。 これは、複数層の参照を使用して達成できます。

この例では、西欧での使用と中東での使用に対してコレクションをサポートします。 どちらのコレクションも汎用の画像コレクションに基づいて作成し、いくつかの画像を追加または変更します。Both collections are then further refined for specific locales ( `m1`, `m2` for two middle-eastern variants, and `w1`, `w2`, and `w3` for three Western locales), except that images are shared for `w1` and `w3`. 不明なロケールは汎用のコレクションのみにマッピングされ、ロケール固有の画像にはアクセスされません。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

次の表に、考慮されるカタログエントリと、汎用入力IDとして考慮される順序を示します `myImg`。

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
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**特定のIDの検索**

一部の画像の命名規則では、内部的な汎用画像IDをサポートしていない場合があります。 リクエストの汎用IDは、常にカタログ内の特定のIDにマップする必要があります。多くの場合、正確な特定のIDが不明な場合があります。

この例では、すべての言語の画像に、、、またはのサフィッ `_1`クスを付 `_2`けることがで `_3` きます。 フランス語のロケールに固有の画像には、サフィッ `_22` クスまたはサ `_23` フィックスを付け、ドイツ語のロケールに固有の画像には、サフィックスを付けるこ `_470` とが `_480` できます。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

次の表に、考慮されるカタログエントリと、汎用入力IDとして考慮される順序を示します `myImg`。

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
   <td> <p> <span class="codeph"> de </span>、 <span class="codeph"> de_at </span>、 <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>その他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 関連項目 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)[,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b)attribute::DefaultLocale [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)locale= [, req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
