---
description: RTF文字列で参照されるすべてのフォントは、デフォルトのカタログまたは現在の画像カタログのフォントマップファイルで使用可能である必要があります。それ以外の場合は、エラーが返されます。
solution: Experience Manager
title: フォントの処理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# フォントの処理{#font-handling}

RTF文字列で参照されるすべてのフォントは、デフォルトのカタログまたは現在の画像カタログのフォントマップファイルで使用可能である必要があります。それ以外の場合は、エラーが返されます。

斜体と太字のテキストに対する最高の品質は、対応するフォントファイルを登録することで達成されます。 サーバが使用できない場合は、標準の面から太字や斜体のフォントを合成できます。 （` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`を参照）。

`attribute::DefaultFont`で指定されたフォントは、RTF文字列で明示的に何も指定されていない場合に使用されます。

画像サービングは、TrueType、OpenType、Adobe Type1（Windowsのみ）のフォントをサポートします。

## Photofont®フォントのサポート {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` は、次の制限を含むPhotofont®フォントをサポートしています。

* `\cf` は、Photofontフォントを指定するテキスト範囲では無視されます。フォトフォントの面には、定義済みの色が設定されています
* 合成フォントスタイルはサポートされていません。`\b`と`\i`を使用する場合は、対応するフォントマップエントリが必要です。それ以外の場合は、エラーが返されます

* 縦書きテキストの流れはサポートされていません
* 16ビット画像のフォトフォントはサポートされていません
* 1つの画像に複数のグリフを含むフォトフォントはサポートされていません
* フォトフォントのグリフ画像にカラープロファイルが埋め込まれていない限り、ナイブカラー変換が適用されます。この場合、相対的な比色レンダリングインテントと黒点補正が常に適用されます

詳しくは、[www.photofont.com](https://www.photofont.com)を参照してください。

## 関連項目 {#section-6cb8a802aa044836bbe449d559093f3a}

[フォントマップリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)、 [attribute::SyntesifyFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)、 [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)、  [ [!DNL www.photofont.com] ](https://www.photofont.com)
