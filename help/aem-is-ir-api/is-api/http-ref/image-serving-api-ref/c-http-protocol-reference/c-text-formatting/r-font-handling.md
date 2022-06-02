---
title: フォント処理
description: RTF 文字列で参照されるすべてのフォントは、デフォルトのカタログまたは現在の画像カタログのフォントマップファイルで使用できる必要があります。使用できない場合は、エラーが返されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e1f0f8bdac2b7a8397adac3bb9ba38d0c519f8fb
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# フォント処理{#font-handling}

RTF 文字列で参照されるすべてのフォントは、デフォルトのカタログまたは現在の画像カタログのフォントマップファイルで使用できる必要があります。使用できない場合は、エラーが返されます。

斜体および太字テキストの最高品質は、対応するフォントファイルを登録することで達成されます。 使用できない場合、サーバは標準面から太字や斜体のフォントを合成できます。 ( [attribute::SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

で指定したフォント `attribute::DefaultFont` は、RTF 文字列で明示的に何も指定されていない場合に使用されます。

画像サービングは、TrueType、OpenType、Adobe Type1（Windows のみ）のフォントをサポートしています。

## Photofont®フォントのサポート {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` は Photofont®フォントをサポートし、次の制限があります。

* `\cf` は、Photofont フォントを指定するテキスト範囲では無視されます。フォトフォント面には定義済みの色が含まれています
* 合成されたフォントスタイルはサポートされていません。使用 `\b` および `\i`対応するフォントマップエントリが必要です。それ以外の場合は、エラーが返されます。

* 縦書きテキストの流れはサポートされていません
* 16 ビット画像のフォトフォントはサポートされていません
* 1 つの画像に複数のグリフを持つ PhotoFont フォントはサポートされていません
* フォトフォントのグリフ画像にカラープロファイルが埋め込まれていない限り、ネイブカラー変換が適用される。この場合、相対的な比色レンダリングインテントと黒点補正が常に適用されます

参照： [www.photofont.com](https://www.photofont.com) を参照してください。

## 関連項目 {#section-6cb8a802aa044836bbe449d559093f3a}

[フォントマップリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](https://www.photofont.com)
