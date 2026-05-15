---
description: 画像セットデータ： Dynamic Media ビューアで使用される画像と制御属性の並べ替えセットを定義するメカニズムを提供します。
solution: Experience Manager
title: 画像セット
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
TQID: 'https://experienceleague.adobe.com/wh25AlzBQv0W-lEugybS8B-cIYYFoK8o9I2uGb52Ui4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 681
ht-degree: 1%

---

# 画像セット{#imageset}

画像セットデータ： Dynamic Media ビューアで使用される画像と制御属性の並べ替えセットを定義するメカニズムを提供します。

画像セットは、並べ替えられたコンマ区切りのアイテムのリストで構成されます。 各アイテムは、1つ以上のサブアイテム（画像ID、スウォッチ ID、メディアファイルのパス、ラベルなど）、セミコロン、コロン、またはその両方で区切られています。

中括弧`{ }`と括弧`( )`は、特定のコンテンツ（カラー値など）を区切ったり、ネストされたセットを示したりするために使用できます。 この方法で使用される括弧または括弧はエンコードしてはならず、常に一致したペアとして表示する必要があります。そうしないと、カタログ解析エラーが発生します。

>[!NOTE]
>
>次の文字はセット区切り文字として使用され、IDまたは文字列値の一部としてセットに表示される場合はHTTP エンコードする必要があります。
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


画像セットの構造と使用について詳しくは、画像サービングビューアのドキュメントを参照してください。

サーバーは、`req=imageset` リクエストに応答して、このフィールドの内容を変更せずに返します。

## 標準セット {#section-5ecc8ffee7224668b63f601383665564}

次のセット定義は画像サービングでネイティブにサポートされており、特定のビューアでのアクセスには、セットのサーバーサイドの解析、検証、処理が必要です。 各セットの種類は、`catalog::AssetType`で対応する値を指定することで特定できます。

**基本スウォッチセット**

基本的なスウォッチセットの各アイテムは、画像レコードへの参照と、スウォッチとして使用される画像レコードへのオプションの別個の参照で構成されます。

| `*`basicSwatchSet`*` | `*`swatchItem`*&#42;[',' *`swatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageId`*[';' *` スウォッチ `*]` |
| `*` スウォッチ `*` | `*`swatchId`*`\|`solidColorSpecifier` |
| `*`imageId`*` | IS画像参照（カタログ/ID） |
| `*`swatchId`*` | IS画像参照（カタログ/ID） |
| `*`solidColorSpecifier`*` | ` '{0x' *`rrggbb`* [ *` ラベル `*]'}'` |
| `*`rrggbb`*` | 単色スウォッチの16進数RGB カラー値を詰め込んだ6桁 |
| `*` ラベル `*` | 単色スウォッチのオプションのテキストラベル |

**階層スウォッチセット**

階層型スウォッチセットの各アイテムは、基本的なスウォッチアイテムまたはスウォッチセットレコードへの参照で構成できます（スウォッチは必要です）。

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`swatchItem`*` \| `{` *`basicSwatchSetId`* &#39;;&#39; *`swatch`* `}` |
| `*`basicSwatchSetId`*` | IS参照（カタログ/ID）は、基本スウォッチセットを定義するカタログレコードに対して参照されます |

**基本スピンセット**

基本的なスピンセットは、画像IDの簡単なリストで構成されます。

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**2次元スピンセット**

2次元スピンセットの各項目は、単純な画像、基本スピンセットへの参照、または中括弧で区切られたインラインの基本スピンセットで構成できます。 中括弧の代わりに、括弧を使用できます。

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`*` \| `{` &#39;{&#39; *`basicSpinSet`* &#39;}&#39; `}` \| `*`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | IS参照（カタログ/ID）は、基本スピンセットを定義するカタログレコードに対して参照されます |

**ページセット**

ページセット内の各項目は、コロンで区切られた最大3 ページの画像で構成できます。

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**メディアセット**

メディアセットの各アイテムは、画像、基本スウォッチセット、階層スウォッチセット、基本スピンセット、2次元スピンセット、ページセット、ビデオアセットで構成できます。 各メディアセット項目には、オプションのスウォッチおよびタイプ識別子を含めることもできます。

| `*`mediaSet`*` | `*`項目`* &#42;[ , *`項目`* ]` |
|---|---|
| `*`項目`*` | `{ *`videoItem`*` \| *`recutItem`* \| *`imageItem`*`}}`\|*`setItem`*`}` `[` ; `[`*`ID`*`]` `[` ; `[`*`reserved`*`] ] ]` |
| `*`videoItem`*` | `*` ビデオ `* ; *`swatchId`*` |
| `*`recutItem`*` | `*`recut`* ; *`swatchId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | `{ *`setId`*` \| `{` &#39;{&#39; *`inlineSet`* &#39;}&#39; `} }` ; *`swatchId`* |
| `*`ID`*` | `media type identifier` `[` img \| basic \| advanced_image \| img \| img_set \| advanced_imageset \| advanced_swatchset \| spin \| video `]` |
| `*`swatchId`*` | IS画像ID |
| `*` ビデオ `*` | ビデオ/アニメーションファイルのパスまたは静的カタログ ID |
| `*`繰り返し`*` | 再帰定義XML ファイルのパスまたは静的カタログ ID |
| `*`imageId`*` | IS画像ID |
| `*`setId`*` | 画像、スピン、またはecatalog セットを参照しています |
| `*`inlineSet`*` | インライン画像、スピン、またはe カタログセット |
| `*`reserved`*` | 将来の使用のために予約済み |

**ビデオセット**

ビデオセットは、各IDが静的コンテンツカタログのエントリを参照するビデオ IDの簡単なリストで構成されます。

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## プロパティ {#section-17c731e5c46646aa90ac21f39bb693ca}

テキスト文字列。 `catalog::Id`の値、絶対Image Server ファイル パス、または`attribute::RootPath`に対する相対ファイルパスをカンマで区切ったリスト。 同じ画像がセット内で複数回参照される場合があります。 定義されたカタログレコードは、任意の場所でセットに表示される場合があります。

このフィールドは、テキスト文字列のローカライズに参加します。 *`label`*&#x200B;個の文字列（*`solidColorSpecifier`*&#x200B;の一部）に加えて、区切られたフィールドはすべて、1つ以上の&#39; `^loc=…^`&#39;ローカライズトークンが含まれている場合にローカライズされます。 詳しくは、*HTTP プロトコルリファレンス*&#x200B;の[ テキスト文字列のローカライゼーション ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)を参照してください。

## 初期設定 {#section-c3a60e360393478284f0f2d2da5b963b}

なし

## 関連トピック {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、[属性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)、[ オブジェクト Id翻訳](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md)、[ テキスト文字列のローカライゼーション ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)、画像サービングビューアのドキュメント
