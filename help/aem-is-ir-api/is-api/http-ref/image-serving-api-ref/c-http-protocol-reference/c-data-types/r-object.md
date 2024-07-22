---
description: Source オブジェクト指定子。 画像、SVG、および ICC プロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます
solution: Experience Manager
title: オブジェクト
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# オブジェクト{#object}

Source オブジェクト指定子。 画像、SVG、および ICC プロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます

`*`object`*[/]{[ *`rootId`*/] *`objId`*}| *`path`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>画像カタログの名前（<span class="codeph"> attribute::RootId </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span> </span> </p> </td> 
  <td class="stentry"> <p>指定した、メインまたはデフォルトの画像カタログ内の画像、SVG、テンプレートまたは ICC プロファイルレコードの ID </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> path </span> </span> </p> </td> 
  <td class="stentry"> <p>画像、マスク、または ICC プロファイルファイルの相対パスと名前 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> オブジェクト </span> </span> </p> </td> 
  <td class="stentry"> <p>は、メイン URL パス、または <span class="codeph"> src= </span>、<span class="codeph"> mask= </span>、icc= </span> コマンドのいずれかで使用 <span class="codeph"> きます。 </p> </td> 
 </tr> 
</table>

*`rootId`* は画像カタログを識別します。 （詳しくは、[ 画像カタログ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) を参照してください。） URL パスで *`rootId`* が指定されている場合、そのカタログはこのリクエストの *メインカタログ* になります。 それ以外の場合は、デフォルトのカタログがメインカタログとして使用されます。 同じリクエストで複数の異なる画像カタログを使用できます。

サーバは最初に、`src=`、`mask=`、`icc=` のコマンドで *`rootId`* が省略されていると仮定し、メイン カタログ内のカタログ エントリを検索しようとします。 実際には、サーバーは *`object`* 文字列全体を *`objId.`* のように使用しようとします

カタログエントリが見つかった場合はそのエントリが使用されます。見つからなかった場合は、次にサーバーによって画像カタログの *`rootId`* の照合が試行されます。 カタログが識別された場合は、*`objId`* が検索されます。 およびエントリが見つかった場合は、使用されます。

それ以外の場合は、*`object`* は明示的なファイルパスと見なされます。 この場合、メインのカタログで `attribute::FullMatch` が設定されていると、このオブジェクトではカタログが無視され、代わりにデフォルトのカタログが使用されます。 `attribute::FullMatch` が設定されていない場合は、メインカタログを使用してさらに処理を行います。

*`rootId`* と *`objId`* はどちらも大文字と小文字が区別されます。 *`path`* は、UNIX でのみ大文字と小文字を区別します。

先頭の `/` を指定すると、メインのカタログではなく既定のカタログが検索されます。 これは主に、明示的なパスがメイン カタログの `attribute::RootPath` ではなく `default::RootPath` を必要とする場合に役立ちますが、既定のカタログ内のエントリへのアクセスを取得する場合にも使用できます。このアクセスを無効にすると、メイン カタログ内のエントリによって優先されます。

*Server 構成ガイド* の *コンテンツの管理* を参照して、*`path`* を物理ファイルパスに変換する方法を確認してください。

>[!NOTE]
>
>*`object.`* では、コンマ「,」は使用できません

## サポートされる画像ファイル形式 {#section-12c85aead78e4f759856ca9ff10637d7}

サポートされているファイル形式の完全なリストについては、IC （Image Converter）ユーティリティの説明を参照してください。

複数の解像度の画像データを必要とするアプリケーションは、Dynamic Media Pyramid Format （PTIF）のマルチTIFFフォーマットを使用する場合に最も高いパフォーマンスを発揮します。 IC ユーティリティは、サポートされている任意の画像形式から PTIF 画像を作成するために使用されます。

## 例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**2 つの異なる画像カタログの画像および ICC プロファイルへのアクセス**

&#39; [!DNL myImage]&#39;として識別される画像カタログ内の画像&#39; [!DNL myCatalog]&#39;を取得し、&#39; [!DNL sRGB]&#39;という名前の画像カタログにある ICC プロファイル [!DNL myProfiles]&#39;を添付してください：

` http:// *` サーバー `*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

レイヤー化による単一の画像カタログの使用

**3 つのレイヤーで構成される単純な複合画像を作成します。すべてのレイヤーは「[!DNL myCatalog]」から取得されます。**

` http:// *` サーバー `*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**カタログを使用して属性を指定しながら、画像ファイルに直接アクセスする**

`myImageCatalog` で設定されたデフォルトの jpg 属性を使用して、[!DNL my/image/path/myImage.tif] にアクセスします。

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 関連項目 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC ユーティリティ ](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
