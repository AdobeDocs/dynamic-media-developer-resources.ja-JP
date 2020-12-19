---
description: ソースオブジェクト指定子 画像、SVG、ICCプロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます
seo-description: ソースオブジェクト指定子 画像、SVG、ICCプロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます
seo-title: オブジェクト
solution: Experience Manager
title: オブジェクト
topic: Scene7 Image Serving - Image Rendering API
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 1%

---


# オブジェクト{#object}

ソースオブジェクト指定子 画像、SVG、ICCプロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます

` *`objectrootIdobjIdpath`*[/]{[ *``*/] *``*}| *``*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId  </span> </span> </p> </td> 
  <td class="stentry"> <p>画像カタログの名前（<span class="codeph">属性：:RootId </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定、メインまたは初期設定の画像カタログ内の画像、SVG、プロファイルまたはICC画像レコードのid </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> path  </span> </span> </p> </td> 
  <td class="stentry"> <p>相対的な画像、マスク、またはICCプロファイルのファイルパスと名前 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object  </span> </span> </p> </td> 
  <td class="stentry"> <p>は、メインURLパス、または<span class="codeph"> src= </span>、<span class="codeph"> mask= </span>、<span class="codeph"> icc= </span>コマンドで使用されます </p> </td> 
 </tr> 
</table>

*`rootId`* は、画像カタログを識別します。（詳しくは、[画像カタログ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)を参照）。 URLパスで&#x200B;*`rootId`*&#x200B;を指定した場合、そのカタログはこのリクエストの&#x200B;*メインカタログ*&#x200B;になります。 それ以外の場合は、初期設定のカタログがメインカタログとして使用されます。 同じリクエストで、複数の異なる画像カタログを使用できます。

サーバは、最初、`src=`、`mask=`、`icc=`の各コマンドで&#x200B;*`rootId`*&#x200B;が省略されていると想定し、メインカタログ内のカタログエントリの検索を試みます。 事実上、サーバーは&#x200B;*`object`*&#x200B;文字列全体を&#x200B;*`objId.`*&#x200B;として使用しようとします

カタログエントリが見つかった場合は、そのエントリが使用されます。それ以外の場合は、次に、サーバは画像カタログの&#x200B;*`rootId`*&#x200B;の照合を試みます。 カタログが特定された場合は、*`objId`*&#x200B;を検索します。 とが見つかった場合は、その値が使用されます。

それ以外の場合は、*`object`*&#x200B;は明示的なファイルパスと見なされます。 この場合、メインカタログに`attribute::FullMatch`が設定されていると、このオブジェクトではカタログが無視され、代わりにデフォルトのカタログが使用されます。 `attribute::FullMatch`が設定されていない場合は、メインカタログを使用して以降の処理を行います。

*`rootId`*&#x200B;と&#x200B;*`objId`*&#x200B;の両方で、大文字と小文字が区別されます。 *`path`* は、UNIXでのみ大文字と小文字が区別されます。

先頭に「/」を指定した場合は、メインカタログではなくデフォルトのカタログが検索されます。 これは、明示的なパスに`default::RootPath`が必要な場合に主に役立ちます。メインカタログの`attribute::RootPath`ではなく、&lt;a0/>が必要な場合にも便利ですが、これ以外の場合は、メインカタログのエントリによって上書きされます。

*`path`*&#x200B;を物理ファイルパスに変換する方法の詳細については、『*サーバ設定ガイド*』の「*コンテンツの管理*」を参照してください。

>[!NOTE]
>
>*`object.`*&#x200B;では、コンマ&#39;,&#39;文字は使用できません

## サポートされる画像ファイル形式{#section-12c85aead78e4f759856ca9ff10637d7}

サポートされるファイル形式の完全なリストについては、IC(Image Converter)ユーティリティの説明を参照してください。

複数の異なる解像度の画像データを必要とするアプリケーションは、Scene7ピラミッドTIFF(PTIF)マルチ解像度形式を使用する場合に最適です。 ICユーティリティは、サポートされている任意の画像形式からPTIF画像を作成する場合に使用します。

## 例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**2つの異なる画像カタログ内の画像とICCプロファイルへのアクセス**

「[!DNL myCatalog]」として識別される画像カタログ内の画像「[!DNL myImage]」を取得し、「[!DNL myProfiles]」という画像カタログ内のICCプロファイル「[!DNL sRGB]」をアタッチします。

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

レイヤーを使用した単一の画像カタログの使用

**3つのレイヤーで構成され、すべて&#39; [!DNL myCatalog]&#39;から取得した単純な合成イメージを作成します。**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**カタログを使用して属性を指定したまま、画像ファイルに直接アクセス**

[!DNL my/image/path/myImage.tif]にアクセスします。`myImageCatalog`で設定されている初期設定のjpg属性を使用します。

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 関連項目 {#section-b6eccefad63f441d922699c4aba58fc9}

[ICユーティリティ](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)、 [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、 [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、 [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
