---
description: 画像セットデータ。 Dynamic Media ビューアで使用される画像の並べ替えられたセットやコントロール属性を定義するメカニズムを提供します。
solution: Experience Manager
title: 画像セット
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 1%

---

# 画像セット{#imageset}

画像セットデータ。 Dynamic Media ビューアで使用される画像の並べ替えられたセットやコントロール属性を定義するメカニズムを提供します。

画像セットは、並べ替えられたコンマ区切りの項目のリストで構成されます。 各項目は、1 つ以上のサブアイテム（画像 ID、スウォッチ ID、メディアファイルパス、ラベルなど）で構成され、セミコロン、コロン、またはその両方で区切られています。

中括弧 `{ }` と中括弧 `( )`、特定のコンテンツ（色の値など）を区切るために使用したり、ネストされたセットを示すために使用したりできます。 この方法で使用される中括弧はエンコードせず、常に一致したペアとして表示する必要があります。そうしないと、カタログの解析エラーが発生します。

>[!NOTE]
>
>次の文字はセットの区切り文字として使用され、セットに ID または文字列値の一部として含まれる場合は HTTP エンコードする必要があります。
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


画像セットの構造と使用について詳しくは、画像サービングビューアのドキュメントを参照してください。

サーバーは、`req=imageset` リクエストに応答して、変更なしでこのフィールドのコンテンツを返します。

## 標準セット {#section-5ecc8ffee7224668b63f601383665564}

次のセット定義は、画像サービングでネイティブにサポートされています。特定のビューアでのアクセスには、セットのサーバー側の解析、検証、処理が含まれます。 各セットタイプは、対応する値を `catalog::AssetType` で指定することで識別できます。

**基本スウォッチセット**

基本スウォッチセットの各項目は、画像レコードへの参照と、スウォッチとして使用される画像レコードへのオプションの個別参照で構成されます。

| `*`basicSwatchSet`*` | `*`swatchItem`*&#42;[',' *`swatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageId`*[';' *`swatch`*]` |
| `*`swatch`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | 画像参照（カタログ/ID） |
| `*`swatchId`*` | 画像参照（カタログ/ID） |
| `*`solidColorSpecifier`*` | ` '{0x' *`rrggbb`* [ *`label`*]'}'` |
| `*`rrggbb`*` | ソリッドカラースウォッチのパックされた 6 桁の hex RGB カラー値 |
| `*` ラベル `*` | ソリッドカラースウォッチのオプションのテキストラベル |

**階層スウォッチセット**

階層スウォッチセット内の各項目は、基本的なスウォッチ項目またはスウォッチセットレコードへの参照で構成できます（このような項目にはスウォッチが必要です）。

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`swatchItem`* | { *`basicSwatchSetId`* ';' *`swatch`* }` |
| `*`basicSwatchSetId`*` | 基本スウォッチセットを定義するカタログレコードへの参照（カタログ/ID） |

**基本スピンセット**

基本スピンセットは、画像 ID の単純なリストで構成されます。

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**2 次元スピンセット**

2 次元スピンセットの各項目は、単純な画像、基本スピンセットへの参照、または中括弧で区切られたインライン基本スピンセットで構成することができます。 中括弧の代わりに括弧を使用することもできます。

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | 基本スピンセットを定義するカタログレコードへの参照（カタログ/ID） |

**ページセット**

ページセット内の各項目は、コロンで区切られた最大 3 ページの画像で構成できます。

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**メディアセット**

メディアセット内の各項目は、画像、基本スウォッチセット、階層スウォッチセット、基本スピンセット、2 次元スピンセット、ページセットまたはビデオアセットで構成されます。 各メディアセット項目には、オプションのスウォッチとタイプ識別子を含めることもできます。

| `*`mediaSet`*` | `*`item`* &#42;[ , *`item`* ]` |
|---|---|
| `*` 項目 `*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`reserved`* ] ] ]` |
| `*`videoItem`*` | `*`video`* ; *`swatchId`*` |
| `*`recutItem`*` | `*`recut`* ; *`swatchId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`swatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | 画像 ID |
| `*` ビデオ `*` | ビデオ/アニメーション ファイル パスまたは静的カタログ ID |
| `*`recut`*` | 再入力定義 XML ファイルのパスまたは静的カタログ ID |
| `*`imageId`*` | 画像 ID |
| `*`setId`*` | 画像、スピン、eCatalog セットへの参照 |
| `*`inlineSet`*` | インライン画像、スピン、eCatalog セット |
| `*` 予約済み `*` | 将来の使用のために予約済み |

**ビデオセット**

ビデオセットは、ビデオ ID の単純なリストで構成され、各 ID は静的コンテンツカタログのエントリを参照します。

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## プロパティ {#section-17c731e5c46646aa90ac21f39bb693ca}

テキスト文字列 `catalog::Id` 値のコンマ区切りリスト、Image Server の絶対ファイルパス、または `attribute::RootPath` を基準としたファイルパス。 同じ画像がセット内で複数回参照される場合があります。 定義するカタログレコードは、セットの任意の場所に表示されます。

このフィールドは、テキスト文字列のローカリゼーションに参加します。 *`label`* 文字列（*`solidColorSpecifier`* の一部）に加えて、区切りフィールドに少なくとも 1 つの「`^loc=…^`」ローカリゼーショントークンが含まれている場合、すべてのフィールドがローカライズされます。 詳しくは、[HTTP プロトコルリファレンス &#x200B;](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) の *テキスト文字列のローカリゼーション* を参照してください。

## 初期設定 {#section-c3a60e360393478284f0f2d2da5b963b}

なし

## 関連トピック {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)、[Object Id Translation](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md)、[Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)、画像サービングビューアのドキュメント
