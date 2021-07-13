---
description: 画像セットデータ。 Dynamic Mediaビューアで使用される画像の並べ替えセットと制御属性を定義するメカニズムを提供します。
solution: Experience Manager
title: 画像セット
feature: Dynamic Media Classic,SDK/API，画像セット
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 2%

---

# 画像セット{#imageset}

画像セットデータ。 Dynamic Mediaビューアで使用される画像の並べ替えセットと制御属性を定義するメカニズムを提供します。

画像セットは、項目のコンマ区切りのリストで構成され、各項目は1つ以上のサブ項目（画像ID、スウォッチID、メディアファイルのパス、ラベルなど）で構成され、セミコロンやコロンで区切られます。

中括弧`{ }`と括弧`( )`を使用して、特定のコンテンツ（色値など）を区切ったり、ネストされたセットを示したりできます。 この方法で使用する中括弧や括弧は、エンコードせず、常に一致するペアとして表示する必要があります。そうしないと、カタログ解析エラーが発生します。

>[!NOTE]
>
>次の文字は、セット区切り文字として使用され、セット内でidまたは文字列値の一部として使用される場合はHTTPエンコードが必要です。
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



画像セットの構造と使用について詳しくは、画像サービングビューアのドキュメントを参照してください。

サーバーは、`req=imageset`リクエストに応じて、変更せずにこのフィールドのコンテンツを返します。

## 標準セット {#section-5ecc8ffee7224668b63f601383665564}

次のセット定義は画像サービングでネイティブにサポートされ、特定のビューアでアクセスするには、セットのサーバー側の解析、検証、処理が必要です。 各セットタイプは、対応する値を`catalog::AssetType`で指定することで識別できます。

**基本スウォッチセット**

基本的なスウォッチセットの各項目は、画像レコードへの参照と、スウォッチとして使用される画像レコードへのオプションの個別の参照で構成されます。

| `*`basicSwatchSet`*` | `*``*&#42;[',' *`swatchItemswatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*``*[';' *`imageIdswatch`*]` |
| `*`スウォッチ`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | IS画像参照（カタログ/ID） |
| `*`swatchId`*` | IS画像参照（カタログ/ID） |
| `*`solidColorSpecifier`*` | ` '{0x' *``* [ *`rrggbblabel`*]'}'` |
| `*`rrggbb`*` | べた塗りカラースウォッチの6桁のパック16進数RGBカラー値 |
| `*`label`*` | べた塗りスウォッチのオプションのテキストラベル |

**階層的スウォッチセット**

階層的スウォッチセット内の各項目は、基本的なスウォッチ項目またはスウォッチセットレコードへの参照で構成できます（そのような項目にはスウォッチが必要です）。

| `*`hierarchySwatchSet`*` | `*``* &#42;[ ',' *`hierarchicalSwatchItemhierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| `*`basicSwatchSetId`*` | 基本的なスウォッチセットを定義するカタログレコードへのIS参照（カタログ/ID） |

**基本スピンセット**

基本的なスピンセットは、画像IDの単純なリストで構成されます。

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**2Dスピンセット**

2次元スピンセットの各項目は、単純な画像、基本スピンセットへの参照、または中括弧で区切られたインライン基本スピンセットで構成できます。 括弧は中括弧の代わりに使用できます。

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| `*`basicSpinSetId`*` | 基本スピンセットを定義するカタログレコードへのIS参照（カタログ/ID） |

**ページセット**

ページセット内の各項目は、コロンで区切られた最大3つのページ画像で構成できます。

| `*`pageSet`*` | `*``* &#42;[ , *`pageItempageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*``* [ : *``* [ : *`imageIdimageIdimageIdimageId`* ] ]` |

**メディアセット**

メディアセット内の各項目は、画像、基本スウォッチセット、階層スウォッチセット、基本スピンセット、2次元スピンセット、ページセットまたはビデオアセットで構成できます。 各メディアセット項目には、オプションのスウォッチとタイプ識別子を含めることもできます。

| `*`mediaSet`*` | `*``* &#42;[ , *`itemitem`* ]` |
|---|---|
| `*`品目`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemrecutItemimageItemsetItemIDreserved`* ] ] ]` |
| `*`videoItem`*` | `*``* ; *`videoswatchId`*` |
| `*`recutItem`*` | `*``* ; *`recutswatchId`*` |
| `*`imageItem`*` | `*``* ; [ *`imageIdswatchId`* ]` |
| `*`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | IS画像ID |
| `*`video`*` | ビデオ/アニメーションのファイルパスまたは静的カタログID |
| `*`再編集`*` | 再編集定義XMLファイルパスまたは静的カタログID |
| `*`imageId`*` | IS画像ID |
| `*`setId`*` | 画像、スピン、eCatalogセットへのIS参照 |
| `*`inlineSet`*` | インライン画像、スピン、eCatalogセット |
| `*`予約`*` | 将来の使用のために予約 |

**ビデオセット**

ビデオセットは、ビデオIDのシンプルなリストで構成され、各IDは静的コンテンツカタログのエントリを参照します。

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## プロパティ {#section-17c731e5c46646aa90ac21f39bb693ca}

テキスト文字列。 `catalog::Id`値のコンマ区切りリスト、Image Serverの絶対ファイルパス、または`attribute::RootPath`を基準とした相対パス。 同じ画像をセット内で複数回参照できます。 定義するカタログレコードは、セット内の任意の場所に表示されます。

このフィールドは、テキスト文字列のローカライゼーションに関与します。 *`label`*&#x200B;文字列（*`solidColorSpecifier`*&#x200B;の一部）に加えて、区切られたすべてのフィールドは、少なくとも1つの「`^loc=…^`」ローカライゼーショントークンが含まれる場合、ローカライズされます。 詳しくは、「*HTTPプロトコルリファレンス*」の「[テキスト文字列のローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)」を参照してください。

## 初期設定 {#section-c3a60e360393478284f0f2d2da5b963b}

なし

## 関連トピック {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) 、 [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)、 [オブジェクトIDの変換](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) 、 [テキスト文字列のローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 、画像サービングビューアのドキュメント
