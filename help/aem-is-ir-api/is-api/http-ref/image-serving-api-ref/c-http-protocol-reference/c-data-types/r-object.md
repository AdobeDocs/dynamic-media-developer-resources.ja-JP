---
description: ソースオブジェクト指定子。 画像、SVG、ICCプロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます
seo-description: ソースオブジェクト指定子。 画像、SVG、ICCプロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます
seo-title: オブジェクト
solution: Experience Manager
title: オブジェクト
topic: Scene7 Image Serving - Image Rendering API
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# オブジェクト{#object}

ソースオブジェクト指定子。 画像、SVG、ICCプロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます

` *`objectrootIdobjIdpath`*[/]{[ *``*/] *``*}| *``*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span></span> </p> </td> 
  <td class="stentry"> <p>画像カタログの名 <span class="codeph"> 前(attribute::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> objtId <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>指定した、メインまたは初期設定の画像カタログ内の画像、SVG、テンプレートまたはICCプロファイルレコードのID </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 経 </span> 路 </span> </p> </td> 
  <td class="stentry"> <p>相対的な画像、マスク、またはICCプロファイルのファイルパスと名前 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 対象 </span> 物 </span> </p> </td> 
  <td class="stentry"> <p>は、メインURLパス、または <span class="codeph"> src=、mask=、また </span>は <span class="codeph"> icc=コ </span>マン <span class="codeph"> ドで使用で </span> きます。 </p> </td> 
 </tr> 
</table>

*`rootId`* 画像カタログを識別します。 (See [Image Catalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) for details.) URLパス *`rootId`* でを指定した場合、そのカタログがこのリクエストのメ *インカタログ* になります。 それ以外の場合は、初期設定のカタログがメインカタログとして使用されます。 同じ要求で複数の異なる画像カタログを使用できます。

サーバは、最初は、、およびコ *`rootId`* マンドではが省略され `src=`ていると想定し、メイン `mask=``icc=` カタログ内のカタログエントリの検索を試みます。 事実上、サーバは文字列全体を *`object`**`objId.`*

カタログエントリが見つかった場合は、そのエントリが使用されます。それ以外の場合、サーバは次に画像カタログの *`rootId`* 一致を試みます。 カタログが識別された場合は、そのカタログが検索されま *`objId`*&#x200B;す。 とが見つかった場合は、それが使用されます。

それ以外の場合 *`object`* 、は明示的なファイルパスと見なされます。 この場合、がメインカタ `attribute::FullMatch` ログに設定されている場合、このオブジェクトのカタログは無視され、代わりにデフォルトのカタログが使用されます。 を設定 `attribute::FullMatch` しない場合、メインカタログを使用してさらに処理が行われます。

とは両方 *`rootId`* で大文字 *`objId`* と小文字が区別されます。 *`path`* は、UNIXでのみ大文字と小文字が区別されます。

先頭に「/」を指定すると、メインカタログではなくデフォルトのカタログが検索されます。 これは、メインカタログではなく明示的なパスが必要な場合に主に役立ちますが、デフォルトのカタログ内のエントリにアクセスするためにも使用できます。これは、メインカタログ内のエントリによって上書きされます。 `default::RootPath``attribute::RootPath`

物理ファイル *パスへの変換方法の詳細については、『サーバ設定**』の「コンテンツ**`path`* の管理」を参照してください。

>[!NOTE]
>
>コンマ&#39;,&#39;文字は *`object.`*

## サポートされる画像ファイル形式 {#section-12c85aead78e4f759856ca9ff10637d7}

サポートされるファイル形式の完全なリストについては、IC(Image Converter)ユーティリティの説明を参照してください。

複数の異なる解像度の画像データを必要とするアプリケーションは、Scene7 Pyramid TIFF(PTIF)の複数解像度形式を使用する場合に最適です。 ICユーティリティは、サポートされている任意の画像形式からPTIF画像を作成するために使用します。

## 例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**2つの異なる画像カタログ内の画像とICCプロファイルへのアクセス**

「」として識別さ [!DNL myImage]れた画像カタログの画像「」を取得し、「 [!DNL myCatalog]」という画像カタログ内のICC [!DNL sRGB]プロファイル「」を添付し [!DNL myProfiles]ます。

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

単一の画像カタログとレイヤーの使用

**3つのレイヤーで構成され、すべて&#39;[!DNL myCatalog]&#39;から取得されたシンプルな合成画像を作成します。**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**カタログを使用して属性を提供しながら、画像ファイルに直接アクセス**

次の場所 [!DNL my/image/path/myImage.tif]で設定された初期設定のjpg属性を使用して、Accessにアクセスしま `myImageCatalog`す。

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 関連項目 {#section-b6eccefad63f441d922699c4aba58fc9}

[ICユーテ](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)ィリティ [, src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
