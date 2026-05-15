---
description: Source オブジェクト指定子。 Image、SVG、およびICC プロファイルオブジェクトは、画像カタログのエントリまたは相対ファイルパスとして指定できます
solution: Experience Manager
title: オブジェクト
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
TQID: 'https://experienceleague.adobe.com/UL5jAeFV4IyldSWQDddhTNVUzS3Gt-qN2PyXky6cHrM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 490
ht-degree: 1%

---

# オブジェクト{#object}

Source オブジェクト指定子。 Image、SVG、およびICC プロファイルオブジェクトは、画像カタログのエントリまたは相対ファイルパスとして指定できます

`*` オブジェクト `*[/]{[ *`rootId`*/] *`objId`*}| *` パス `*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>画像カタログの名前（<span class="codeph">属性：:RootId </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span> </span> </p> </td> 
  <td class="stentry"> <p>指定した画像カタログ、メインまたはデフォルトの画像カタログ内の画像、SVG、テンプレート、またはICC プロファイルレコードのID </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> パス </span> </span> </p> </td> 
  <td class="stentry"> <p>相対イメージ、マスク、またはICC プロファイルファイルのパスと名前 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> オブジェクト </span> </span> </p> </td> 
  <td class="stentry"> <p>は、メイン URL パス、または<span class="codeph"> src= </span>、<span class="codeph"> mask= </span>、<span class="codeph"> icc= </span> コマンドのいずれかで発生する可能性があります </p> </td> 
 </tr> 
</table>

*`rootId`*&#x200B;は画像カタログを識別します。 （詳しくは、[画像カタログ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)を参照してください）。 URL パスに&#x200B;*`rootId`*&#x200B;が指定されている場合、そのカタログはこのリクエストの&#x200B;*メイン カタログ*&#x200B;になります。 そうでない場合は、デフォルトのカタログがメインカタログとして使用されます。 同じリクエストで複数の異なる画像カタログを使用できます。

サーバーは最初、`src=`、`mask=`、および`icc=` コマンドで&#x200B;*`rootId`*&#x200B;が省略されていることを前提とし、メインカタログ内のカタログエントリを検索しようとします。 実際、サーバーは&#x200B;*`object`*&#x200B;文字列全体を&#x200B;*`objId.`*&#x200B;として使用しようとしています

カタログエントリが見つかった場合は、そのエントリが使用されます。見つからない場合は、次にサーバーが画像カタログの&#x200B;*`rootId`*&#x200B;と一致させようとします。 カタログが識別された場合は、*`objId`*&#x200B;が検索されます。 とエントリが見つかった場合は、それが使用されます。

それ以外の場合、*`object`*&#x200B;は明示的なファイルパスであると見なされます。 この場合、`attribute::FullMatch`がメインカタログで設定されている場合、このオブジェクトではカタログが無視され、代わりに使用されるデフォルトカタログが無視されます。 `attribute::FullMatch`が設定されていない場合は、メイン カタログを使用してさらに処理を行います。

*`rootId`*&#x200B;と&#x200B;*`objId`*&#x200B;の両方で大文字と小文字が区別されます。 *`path`*&#x200B;では、UNIXでのみ大文字と小文字が区別されます。

先頭の`/`が指定されている場合、メインカタログではなくデフォルトカタログが検索されます。 これは主に、明示的なパスでメインカタログの`attribute::RootPath`ではなく`default::RootPath`が必要な場合に役立ちますが、デフォルトのカタログのエントリへのアクセスを取得するために使用することもできます。このアクセスは、メインカタログのエントリによって上書きされます。

*`path`*&#x200B;を物理ファイルパスに変換する方法の詳細については、*サーバー設定ガイド*&#x200B;の&#x200B;*コンテンツの管理*&#x200B;を参照してください。

>[!NOTE]
>
>コンマ「,」文字は&#x200B;*`object.`*&#x200B;では使用できません

## サポートされる画像ファイル形式 {#section-12c85aead78e4f759856ca9ff10637d7}

サポートされているファイル形式の完全なリストについては、IC （画像コンバータ）ユーティリティの説明を参照してください。

Dynamic MediaのピラミッドTIFF（PTIF）の多解像度フォーマットを使用する場合、複数の異なる解像度の画像データを必要とするアプリケーションが最も効果的に機能します。 IC ユーティリティは、サポートされている任意の画像形式からPTIF画像を作成するために使用されます。

## 例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**2つの異なる画像カタログ内の画像とICC プロファイルへのアクセス**

画像&#39; [!DNL myImage]&#39;を&#39; [!DNL myCatalog]&#39;として識別された画像カタログで取得し、&#39; [!DNL myProfiles]&#39;という名前の画像カタログにあるICC プロファイル &#39; [!DNL sRGB]&#39;を添付します。

` http:// *` サーバー`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

レイヤーを使用した単一の画像カタログの使用

**3つのレイヤーで構成されるシンプルな合成イメージを作成し、すべて&#39;[!DNL myCatalog]&#39;から取得しました：**

` http:// *` サーバー`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**カタログを使用して属性を提供しながら、画像ファイルに直接アクセスする**

`myImageCatalog`で設定されたデフォルトのjpg属性を使用して、[!DNL my/image/path/myImage.tif]にアクセスします。

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 関連項目 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC Utility](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)、[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、[mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、[属性：:FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
