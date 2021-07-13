---
description: ソースオブジェクト指定子。 画像、SVG、ICCプロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます
solution: Experience Manager
title: オブジェクト
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 1%

---

# オブジェクト{#object}

ソースオブジェクト指定子。 画像、SVG、ICCプロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます

`*``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId  </span> </span> </p> </td> 
  <td class="stentry"> <p>画像カタログの名前( <span class="codeph"> attribute::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定した、メインまたはデフォルトの画像カタログ内の画像、SVG、テンプレートまたはICCプロファイルレコードのid </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> パス  </span> </span> </p> </td> 
  <td class="stentry"> <p>相対的な画像、マスク、またはICCプロファイルのファイルパスと名前 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object  </span> </span> </p> </td> 
  <td class="stentry"> <p>は、メインURLパス、または<span class="codeph"> src= </span>、<span class="codeph"> mask= </span>、<span class="codeph"> icc= </span>のいずれかのコマンドで使用されます。 </p> </td> 
 </tr> 
</table>

*`rootId`* は、画像カタログを識別します。（詳しくは、[画像カタログ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)を参照してください）。 URLパスで&#x200B;*`rootId`*&#x200B;を指定した場合、そのカタログがこのリクエストの&#x200B;*メインカタログ*&#x200B;になります。 それ以外の場合は、デフォルトのカタログがメインカタログとして使用されます。 同じリクエストで複数の異なる画像カタログを使用できます。

サーバーは、最初、`src=`、`mask=`、`icc=`の各コマンドで&#x200B;*`rootId`*&#x200B;が省略されたと想定し、メインカタログ内のカタログエントリの検索を試みます。 サーバーは、*`object`*&#x200B;文字列全体を&#x200B;*`objId.`*&#x200B;として使用しようとします

カタログエントリが見つかった場合は、そのエントリが使用されます。それ以外の場合は、サーバーは次に画像カタログの&#x200B;*`rootId`*&#x200B;の照合を試みます。 カタログが特定された場合は、*`objId`*&#x200B;を検索します。 とが見つかった場合は、それが使用されます。

それ以外の場合、*`object`*&#x200B;は明示的なファイルパスと見なされます。 この場合、`attribute::FullMatch`がメインカタログに設定されていると、このオブジェクトに対してカタログは無視され、代わりにデフォルトのカタログが使用されます。 `attribute::FullMatch`が設定されていない場合は、メインカタログを使用してさらに処理します。

*`rootId`*&#x200B;と&#x200B;*`objId`*&#x200B;の両方で大文字と小文字が区別されます。 *`path`* は、UNIXでのみ大文字と小文字が区別されます。

先頭に「/」を指定した場合、メインカタログではなくデフォルトのカタログが検索されます。 これは、明示的なパスにメインカタログの`attribute::RootPath`ではなく`default::RootPath`が必要な場合に主に役立ちますが、デフォルトカタログ内のエントリにアクセスするためにも使用できます。これは、メインカタログ内のエントリで上書きされます。

*`path`*&#x200B;を物理ファイルパスに変換する方法について詳しくは、『*サーバ設定ガイド*』の&#x200B;*コンテンツの管理*&#x200B;を参照してください。

>[!NOTE]
>
>*`object.`*&#x200B;では、コンマ&#39;,&#39;文字は使用できません

## サポートされる画像ファイル形式 {#section-12c85aead78e4f759856ca9ff10637d7}

サポートされているファイル形式の完全なリストについては、IC(Image Converter)ユーティリティの説明を参照してください。

複数の異なる解像度の画像データを必要とするアプリケーションは、Dynamic Media Pyramid TIFF(PTIF)マルチ解像度形式を使用する場合に最適です。 ICユーティリティは、サポートされている任意のイメージ形式からPTIFイメージを作成するために使用します。

## 例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**2つの異なる画像カタログ内の画像とICCプロファイルへのアクセス**

「 [!DNL myCatalog] 」と識別される画像カタログの画像「 [!DNL myImage] 」を取得し、画像カタログ「 [!DNL myProfiles] 」にあるICCプロファイル「 [!DNL sRGB] 」を添付します。

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

レイヤーを使用した単一の画像カタログの使用

**3つのレイヤーで構成され、すべて「 」から取得される単純な複合イメージを作 [!DNL myCatalog]成します。**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**カタログを使用して属性を提供しながら、画像ファイルに直接アクセス**

`myImageCatalog`で設定したデフォルトのjpg属性を使用して、[!DNL my/image/path/myImage.tif]にアクセスします。

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 関連項目 {#section-b6eccefad63f441d922699c4aba58fc9}

[ICユーティリティ](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)、 [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、 [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、 [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
