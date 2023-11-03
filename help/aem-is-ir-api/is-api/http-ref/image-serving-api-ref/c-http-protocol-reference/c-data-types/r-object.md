---
description: ソースオブジェクト指定子。 画像、SVG、ICC プロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます
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

ソースオブジェクト指定子。 画像、SVG、ICC プロファイルオブジェクトは、画像カタログエントリまたは相対ファイルパスとして指定できます

`*`object`*[/]{[ *`rootId`*/] *`objId`*}| *`パス`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>画像カタログの名前 ( <span class="codeph"> attribute::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span> </span> </p> </td> 
  <td class="stentry"> <p>指定された、メインまたはデフォルトの画像カタログ内の画像、SVG、テンプレート、または ICC プロファイルレコードの id </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> パス </span> </span> </p> </td> 
  <td class="stentry"> <p>相対的な画像、マスク、または ICC プロファイルのファイルパスと名前 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object </span> </span> </p> </td> 
  <td class="stentry"> <p>は、メイン URL パスまたは <span class="codeph"> src= </span>, <span class="codeph"> mask= </span>または <span class="codeph"> icc= </span> command </p> </td> 
 </tr> 
</table>

*`rootId`* は、画像カタログを識別します。 ( 詳しくは、 [画像カタログ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) （詳細は） 次の場合 *`rootId`* が URL パスで指定されている場合、そのカタログは *メインカタログ* を設定します。 それ以外の場合は、デフォルトのカタログがメインカタログとして使用されます。 同じリクエストで複数の異なる画像カタログを使用できます。

サーバーは最初に、 *`rootId`* が `src=`, `mask=`、および `icc=` コマンドを実行し、メインカタログ内のカタログエントリを検索します。 サーバーは、 *`object`* 文字列 *`objId.`*

カタログエントリが見つかった場合は、そのエントリが使用されます。それ以外の場合は、サーバは次に *`rootId`* 画像カタログの。 カタログが特定された場合は、そのカタログが検索されます。 *`objId`*. とが見つかった場合は、それが使用されます。

それ以外の場合は、 *`object`* は、明示的なファイルパスと見なされます。 この場合、 `attribute::FullMatch` がメインカタログに設定されている場合、このオブジェクトではカタログは無視され、代わりにデフォルトのカタログが使用されます。 次の場合 `attribute::FullMatch` が設定されていない場合、メインカタログを使用して以降の処理がおこなわれます。

両方 *`rootId`* および *`objId`* は大文字と小文字を区別します。 *`path`* は、UNIX でのみ大文字と小文字が区別されます。

先頭に `/` を指定すると、デフォルトのカタログがメインカタログではなく検索されます。 これは、主に、明示的なパスで `default::RootPath` メインカタログの `attribute::RootPath`を使用することもできますが、デフォルトのカタログ内のエントリにアクセスするために使用することもできます。これは、メインカタログ内のエントリによって上書きされます。

参照： *コンテンツの管理* （内） *サーバー設定ガイド* 詳細は、 *`path`* は物理ファイルパスに変換されます。

>[!NOTE]
>
>では、コンマ「,」文字は使用できません *`object.`*

## サポートされる画像ファイル形式 {#section-12c85aead78e4f759856ca9ff10637d7}

サポートされるファイル形式の完全なリストについては、IC（画像コンバータ）ユーティリティの説明を参照してください。

複数の異なる解像度の画像データを必要とするアプリケーションは、Dynamic MediaピラミッドTIFF(PTIF) 複数解像度形式を使用する場合に最も高いパフォーマンスを発揮します。 IC ユーティリティは、サポートされている任意の画像形式から PTIF 画像を作成するために使用します。

## 例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**2 つの異なる画像カタログ内の画像と ICC プロファイルへのアクセス**

画像「 」を取得します [!DNL myImage]&#39; （画像カタログ内）が「 [!DNL myCatalog]「 」と ICC プロファイル「 」を添付します。 [!DNL sRGB]「 」 （「 」という名前の画像カタログ内） [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

レイヤー付きの単一の画像カタログの使用

**3 つのレイヤーで構成され、すべて「 」から取得した単純な合成イメージを作成します。 [!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**カタログを使用して属性を提供しながら、画像ファイルに直接アクセス**

アクセス [!DNL my/image/path/myImage.tif]で設定したデフォルトの jpg 属性を使用 `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 関連項目 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC ユーティリティ](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
