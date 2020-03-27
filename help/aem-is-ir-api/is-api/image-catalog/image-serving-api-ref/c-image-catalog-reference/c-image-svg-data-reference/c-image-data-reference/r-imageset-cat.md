---
description: 画像セットデータ。 画像の並べ替え済みセットを定義し、Scene7ビューアで使用される属性を制御するメカニズムを提供します。
seo-description: 画像セットデータ。 画像の並べ替え済みセットを定義し、Scene7ビューアで使用される属性を制御するメカニズムを提供します。
seo-title: 画像セット
solution: Experience Manager
title: 画像セット
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a34aaef-4053-4474-abb8-794331898d88
translation-type: tm+mt
source-git-commit: 06f227705765e4173e1c4b49dd7d8202884f5e07

---


# 画像セット{#imageset}

画像セットデータ。 画像の並べ替え済みセットを定義し、Scene7ビューアで使用される属性を制御するメカニズムを提供します。

画像セットは、項目のカンマ区切りリストで構成され、各項目は1つ以上のサブ項目（画像ID、スウォッチID、メディアファイルのパス、ラベルなど）で構成され、セミコロンやコロンで区切られます。

中括弧「{ }」と括弧「( )」は、特定の内容（色の値など）を区切るため、またはネストされたセットを示すために使用できます。 この方法で使用する中括弧または丸括弧は、エンコードしないで、常に一致するペアとして表示する必要があります。それ以外の場合は、カタログの解析エラーが発生します。

>[!NOTE]
>
>次の文字は、セット区切り文字として使用され、セット内でidまたは文字列値の一部として表示される場合はHTTPエンコードする必要があります。
>
>* ,
>* ;
>* 。
>* {
>* }
>* (
>* 。



画像セットの構造と使用に関する詳細は、画像サービングビューアのドキュメントを参照してください。

サーバーは、要求に応じて変更を加えることなく、このフィールドの内容を返 `req=imageset` します。

## 標準セット {#section-5ecc8ffee7224668b63f601383665564}

次のセット定義は画像サービングでネイティブにサポートされ、特定のビューアでのアクセスには、サーバ側の解析、検証、セットの処理が含まれます。 各セットタイプは、に対応する値を指定することで識別できま `catalog::AssetType`す。

**基本スウォッチセット**

基本的なスウォッチセット内の各項目は、画像レコードへの参照と、スウォッチとして使用される画像レコードへのオプションの個別の参照で構成されます。

| ` *`basicSwatchSet`*` | ` *`swatchItemswatchItem`*&#42;[',' *``*]` |
|---|---|
| ` *`swatchItem`*` | ` *`imageIdswatch`*[';' *``*]` |
| ` *`スウォッチ`*` | ` *`swatchId`*|solidColorSpecifier` |
| ` *`imageId`*` | IS画像参照（カタログ/ID） |
| ` *`swatchId`*` | IS画像参照（カタログ/ID） |
| ` *`solidColorSpecifier`*` | ` '{0x' *`rrggbblabel`* [ *``*]'}'` |
| ` *`rrggbb`*` | べた塗りスウォッチの6桁のパック16進数RGBカラー値 |
| ` *`label`*` | べた塗りスウォッチのオプションのテキストラベル |

**階層的スウォッチセット**

階層的スウォッチセット内の各項目は、基本的なスウォッチ項目またはスウォッチセットレコードへの参照で構成できます（この項目にはスウォッチが必要です）。

| ` *`hierarchicalSwatchSet`*` | ` *`hierarchicalSwatchItemhierarchicalSwatchItem`* &#42;[ ',' *``* ]` |
|---|---|
| ` *`hierarchicalSwatchItem`*` | ` *`swatchItembasicSwatchSetIdswatch`* | { *``* ';' *``* }` |
| ` *`basicSwatchSetId`*` | 基本的なスウォッチセットを定義するカタログレコードへのIS参照（カタログ/ID） |

**基本スピンセット**

基本スピンセットは、画像IDの簡単なリストで構成されます。

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**2次元スピンセット**

2次元スピンセットの各項目は、単純な画像、基本スピンセットへの参照または波括弧で区切られたインライン基本スピンセットで構成できます。 波括弧の代わりに丸括弧を使用できます。

| ` *`2dSpinItem`*` | ` *`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| ` *`2dSpinItem`*` | ` *`imageIdbasicSpinSetbasicSpinSetId`* | { '{' *``* '}' } | *``*` |
| ` *`basicSpinSetId`*` | 基本スピンセットを定義するカタログレコードへのIS参照（カタログ/ID） |

**ページセット**

ページセット内の各項目は、コロンで区切った最大3つのページ画像で構成できます。

| ` *`pageSet`*` | ` *`pageItempageItem`* &#42;[ , *``* ]` |
|---|---|
| ` *`pageItem`*` | ` *`imageIdimageIdimageId`* [ : *``* [ : *``* ] ]` |

**メディアセット**

メディアセット内の各項目は、画像、基本スウォッチセット、階層スウォッチセット、基本スピンセット、2次元スピンセット、ページセットまたはビデオアセットで構成できます。 各メディアセット項目には、オプションのスウォッチとタイプ識別子を含めることもできます。

| ` *`mediaSet`*` | ` *`項`* &#42;[ , *`目`* ]` |
|---|---|
| ` *`品目`*` | ` { *`videoItemrecutItemimageItemsetItemIDreserved`* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *``* ] ] ]` |
| ` *`videoItem`*` | ` *`videoswatchId`* ; *``*` |
| ` *`recutItem`*` | ` *`recutswatchId`* ; *``*` |
| ` *`imageItem`*` | ` *`imageIdswatchId`* ; [ *``* ]` |
| ` *`setItem`*` | ` { *`setIdinlineSetswatchId`* | { '{' *``* '}' } } ; *``*` |
| ` *`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| ` *`swatchId`*` | IS画像ID |
| ` *`ビデオ`*` | ビデオ/アニメーションのファイルパスまたは静的カタログID |
| ` *`再編集`*` | 再編集定義XMLファイルのパスまたは静的カタログID |
| ` *`imageId`*` | IS画像ID |
| ` *`setId`*` | IS参照：画像、スピン、eCatalogセット |
| ` *`inlineSet`*` | インライン画像、スピン、eCatalogセット |
| ` *`予約`*` | 将来の使用のために予約 |

**ビデオセット**

ビデオセットは、ビデオIDの単純なリストで構成され、各IDは静的コンテンツカタログのエントリを参照します。

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## プロパティ {#section-17c731e5c46646aa90ac21f39bb693ca}

テキスト文字列。 値のコンマ区切りリスト、Image Server `catalog::Id` の絶対ファイルパス、またはを基準とするファイルパスで `attribute::RootPath`す。 同じ画像がセット内で複数回参照される場合があります。 定義するカタログレコードは、セット内の任意の場所に表示されます。

このフィールドは、テキスト文字列のローカリゼーションに関与します。 文字列（の一部） *`label`* に加えて、少なくとも1つの「 *`solidColorSpecifier`*」ローカリゼーショントークンが含まれる場合は、すべての区切られたフィールドがロー `^loc=…^`カライズされます。 詳しくは、 [](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) HTTPプロトコルリファレンスの *「テキスト文字列のローカリゼーション* 」を参照してください。

## 初期設定 {#section-c3a60e360393478284f0f2d2da5b963b}

なし

## 関連トピック {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Object Id Translation](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Image Serving Viewers Documentation
