---
description: 画像セットデータ。 Dynamic Mediaビューアで使用する画像の並べ替えセットと制御属性を定義するメカニズムを提供します。
solution: Experience Manager
title: 画像セット
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 2%

---

# 画像セット{#imageset}

画像セットデータ。 Dynamic Mediaビューアで使用する画像の並べ替えセットと制御属性を定義するメカニズムを提供します。

画像セットは、カンマで区切られた項目の並べ替え済みリストで構成されます。 各項目は、1 つ以上のサブ項目（画像 ID、スウォッチ ID、メディアファイルのパス、ラベルなど）で構成され、セミコロンまたはコロン（またはその両方）で区切られます。

波括弧 `{ }` および括弧 `( )` を使用して、特定のコンテンツ（色の値など）を区切ったり、ネストされたセットを示したりできます。 この方法で使用する中括弧や括弧はエンコードできず、常に一致するペアとして表示される必要があります。そうしないと、カタログ解析エラーが発生します。

>[!NOTE]
>
>次の文字は、セット区切り文字として使用され、セット内で id または文字列値の一部として表示される場合は HTTP エンコードする必要があります。
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


画像セットの構造と使用について詳しくは、画像サービングビューアのドキュメントを参照してください。

サーバーは、 `req=imageset` リクエスト。

## 標準セット {#section-5ecc8ffee7224668b63f601383665564}

次のセット定義は画像サービングでネイティブにサポートされており、特定のビューアでアクセスするには、サーバー側の解析、検証、セットの処理が必要です。 各セットタイプは、 `catalog::AssetType`.

**基本スウォッチセット**

基本スウォッチセット内の各項目は、画像レコードへの参照と、スウォッチとして使用する画像レコードへのオプションの個別の参照で構成されます。

| `*`basicSwatchSet`*` | `*`swatchItem`*&#42;[',' *`swatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageId`*[';' *`スウォッチ`*]` |
| `*`スウォッチ`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | IS 画像参照（カタログ/ID） |
| `*`swatchId`*` | IS 画像参照（カタログ/ID） |
| `*`solidColorSpecifier`*` | ` '{0x' *`rrggbb`* [ *`ラベル`*]'}'` |
| `*`rrggbb`*` | 6 桁のパック 16 進RGBのカラー値（べた塗りスウォッチの場合） |
| `*`label`*` | べた塗りスウォッチ用のオプションのテキストラベル |

**階層的スウォッチセット**

階層的スウォッチセット内の各項目は、基本的なスウォッチ項目またはスウォッチセットレコードへの参照で構成できます（そのような項目にはスウォッチが必要です）。

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`swatchItem`* | { *`basicSwatchSetId`* ';' *`スウォッチ`* }` |
| `*`basicSwatchSetId`*` | 基本的なスウォッチセットを定義するカタログレコードへの IS 参照（カタログ/ID） |

**基本スピンセット**

基本的なスピンセットは、画像 ID の単純なリストで構成されます。

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**2D スピンセット**

2 次元スピンセットの各項目は、単純な画像、基本スピンセットへの参照、または中括弧で区切られたインライン基本スピンセットで構成できます。 中括弧の代わりに括弧を使用できます。

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | 基本スピンセットを定義するカタログレコードへの IS 参照（カタログ/ID） |

**ページセット**

ページセット内の各項目は、コロンで区切られた最大 3 ページの画像で構成できます。

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**メディアセット**

メディアセット内の各項目は、画像、基本スウォッチセット、階層スウォッチセット、基本スピンセット、2 次元スピンセット、ページセット、ビデオアセットで構成できます。 各メディアセット項目には、オプションのスウォッチとタイプ識別子を含めることもできます。

| `*`mediaSet`*` | `*`項目`* &#42;[ , *`項目`* ]` |
|---|---|
| `*`品目`*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`予約済み`* ] ] ]` |
| `*`videoItem`*` | `*`ビデオ`* ; *`swatchId`*` |
| `*`recutItem`*` | `*`再編集`* ; *`swatchId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`swatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | IS 画像 ID |
| `*`ビデオ`*` | ビデオ/アニメーションのファイルパスまたは静的カタログ ID |
| `*`再編集`*` | 定義 XML ファイルのパスまたは静的カタログ ID を再編集 |
| `*`imageId`*` | IS 画像 ID |
| `*`setId`*` | 画像、スピン、eCatalog セットへの IS 参照 |
| `*`inlineSet`*` | インライン画像、スピン、eCatalog セット |
| `*`予約`*` | 将来の使用のために予約 |

**ビデオセット**

ビデオセットは、ビデオ ID の単純なリストで構成され、各 ID は静的コンテンツカタログ内のエントリを参照します。

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## プロパティ {#section-17c731e5c46646aa90ac21f39bb693ca}

テキスト文字列。 のコンマ区切りリスト `catalog::Id` 値、Image Server の絶対ファイルパス、または `attribute::RootPath`. 同じ画像をセット内で複数回参照できます。 定義するカタログレコードは、セット内の任意の場所に表示される場合があります。

このフィールドは、テキスト文字列のローカライゼーションに参加します。 に加えて *`label`* 文字列 ( *`solidColorSpecifier`*) すべての区切りフィールド（少なくとも 1 つの「 」が含まれる場合）はローカライズされます `^loc=…^`&#39;ローカリゼーショントークン。 参照： [テキスト文字列のローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) （内） *HTTP プロトコルリファレンス* 」を参照してください。

## 初期設定 {#section-c3a60e360393478284f0f2d2da5b963b}

なし

## 関連トピック {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [オブジェクト ID の変換](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [テキスト文字列のローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 、画像サービングビューアドキュメント
