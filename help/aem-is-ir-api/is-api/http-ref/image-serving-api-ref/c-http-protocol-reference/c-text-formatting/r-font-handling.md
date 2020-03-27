---
description: RTF文字列で参照されるすべてのフォントは、初期設定のカタログまたは現在の画像カタログのフォントマップファイルで使用可能である必要があります。使用できない場合は、エラーが返されます。
seo-description: RTF文字列で参照されるすべてのフォントは、初期設定のカタログまたは現在の画像カタログのフォントマップファイルで使用可能である必要があります。使用できない場合は、エラーが返されます。
seo-title: フォント処理
solution: Experience Manager
title: フォント処理
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# フォント処理{#font-handling}

RTF文字列で参照されるすべてのフォントは、初期設定のカタログまたは現在の画像カタログのフォントマップファイルで使用可能である必要があります。使用できない場合は、エラーが返されます。

斜体や太字のテキストに最高の品質を得るには、対応するフォントファイルを登録します。 使用できない場合、サーバは標準面から太字や斜体のフォントを合成できます。 (See ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

で指定したフォントが、RTF文 `attribute::DefaultFont` 字列で明示的に指定されていない場合に使用されます。

画像サービングは、TrueType、OpenType、Adobe Type 1（Windowsのみ）のフォントをサポートします。

## Photofont®フォントのサポート {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` は、次の制限を受けて、Photofont®フォントをサポートしています。

* `\cf` は、Photofontフォントを指定するテキスト範囲では無視されます。Photofontのフォントの色が事前に定義されている
* 合成されたフォントスタイルはサポートされていません。を使用し、対応す `\b` るフォントマ `\i`ップエントリを必要とする場合、それ以外の場合はエラーが返される

* 縦書きのテキストフローはサポートされていません
* 16ビット画像を含むPhotofontフォントはサポートされていません
* 1つの画像に複数のグリフを含むPhotofontフォントはサポートされていません
* Photofontのグリフ画像にカラープロファイルが埋め込まれていない限り、Naiveカラー変換が適用されます。この場合、相対的な色域を維持するレンダリングインテントとブラックポイントの補正が常に適用されます

詳細については、を ` [www.photofont.com](http://www.photofont.com)` 参照してください。

## 関連項目 {#section-6cb8a802aa044836bbe449d559093f3a}

[Font Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribute::SyntesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](http://www.photofont.com)
