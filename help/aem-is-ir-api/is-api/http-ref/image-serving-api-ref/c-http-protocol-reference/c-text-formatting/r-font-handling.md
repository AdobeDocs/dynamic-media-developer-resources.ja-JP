---
description: RTF文字列で参照されるすべてのフォントは、初期設定のカタログまたは現在の画像カタログのフォントマップファイルで使用できる必要があります。使用できない場合は、エラーが返されます。
seo-description: RTF文字列で参照されるすべてのフォントは、初期設定のカタログまたは現在の画像カタログのフォントマップファイルで使用できる必要があります。使用できない場合は、エラーが返されます。
seo-title: フォント処理
solution: Experience Manager
title: フォント処理
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# フォント処理{#font-handling}

RTF文字列で参照されるすべてのフォントは、初期設定のカタログまたは現在の画像カタログのフォントマップファイルで使用できる必要があります。使用できない場合は、エラーが返されます。

斜体や太字のテキストの最高の品質は、対応するフォントファイルを登録することで達成できます。 使用できない場合は、サーバは標準面から太字または斜体のフォントを合成できます。 （` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`を参照）。

`attribute::DefaultFont`で指定したフォントは、RTF文字列で明示的に何も指定されていない場合に使用されます。

画像サービングは、TrueType、OpenType、AdobeType 1（Windowsのみ）フォントをサポートしています。

## Photofont®フォントのサポート{#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` は、Photofont®フォントをサポートしますが、次の制限があります。

* `\cf` は、Photofontフォントを指定するテキスト範囲では無視されます。フォトフォントの面に定義済みの色がある
* 合成フォントスタイルはサポートされていません。`\b`と`\i`の使用には対応するフォントマップエントリが必要です。それ以外の場合は、エラーが返されます

* 縦書きのテキストフローはサポートされていません
* 16ビット画像のPhotofontはサポートされていません
* 画像ごとに複数のグリフを持つPhotoFontフォントはサポートされていません
* Photofontのグリフ画像にカラープロファイルが埋め込まれていない限り、Navieveカラー変換が適用されます。この場合、相対的な色域を保持するレンダリングインテントとブラックポイントの補正が常に適用されます

詳しくは` [www.photofont.com](http://www.photofont.com)`を参照してください。

## 関連項目 {#section-6cb8a802aa044836bbe449d559093f3a}

[フォントマップリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)、 [attribute::SyntesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)、 [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)、  [ [!DNL www.photofont.com] ](http://www.photofont.com)
