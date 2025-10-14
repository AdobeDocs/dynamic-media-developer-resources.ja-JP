---
description: 画像サービングは、ソースデータとして Scalable Vector Graphics （SVG）ファイルをサポートします。 SVG 1.1 への準拠が必要です。
solution: Experience Manager
title: SVG サポート
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# SVG サポート{#svg-support}

画像サービングは、ソースデータとして Scalable Vector Graphics （SVG）ファイルをサポートします。 SVG 1.1 への準拠が必要です。

画像サービングでは、静的なSVG コンテンツのみが認識されます。アニメーション、スクリプティング、その他のインタラクティブコンテンツはサポートされていません。

SVGは、画像ファイルが許可されている場所（URL パス、`src=`、`mask=`）であればどこでも指定できます。 SVG ファイルのコンテンツがラスタライズされると、画像のように処理されます。

画像と同様に、SVG ファイルは、画像カタログエントリまたは相対ファイルパスとして指定できます。

## 代替変数 {#section-83b149f13f244193901df39b204c975b}

代替変数 ` $ *[!DNL var]*$`、要素および任意の要素属性の値文字列 `<text>`SVG ファイルに含めることができます。

埋め込み画像サービングリクエストのクエリ部分にある重要な変数は、直接置き換えられません。 代わりに、使用可能なすべての変数定義がリクエストに追加され、リクエストの解析時に画像サービングで変数を置き換えることができます。

詳細は、[&#x200B; 代替変数 &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) を参照してください。

## 画像参照 {#section-a7680f9e6aca4b1a83560637cc9fac66}

画像は、`<image>` 要素を使用してSVGに挿入できます。 `xlink::href` 要素の `<image>` 属性で参照される画像は、有効な画像提供リクエストである必要があります。 外部 URL は許可されていません。

`http://` で始まる完全な画像サービングリクエストまたは `/is/image` で始まる相対 URL を指定します。 完全な HTTP パスを指定すると、相対形式に変換するためにパスからドメイン名が削除されます。 完全な HTTP パスを使用すると、ファイルをサードパーティのSVG レンダラーでプレビューできるので便利です。

>[!NOTE]
>
>このリリースの画像サービングでの画像のレンダリングのサポートは制限されています。 SVG内からの画像の参照は、従来の画像サービングレイヤーやテンプレートのメカニズムでは目的の結果を得ることができない場合にのみ使用してください。 どのような状況でも、SVGを使用して複数画像の合成を生成しないでください。

>[!NOTE]
>
>現時点では、SVGに埋め込まれた画像のサイズは自動的には変更されません。 目的の画像サイズを設定するために必要な画像サービングコマンド（例：`wid=`）がすべての画像共有に含まれていることを確認します。 画像サイズが明示的に設定されていない場合は、`attribute::DefaultPix` が適用されます。

## カラーマネジメント {#section-ea76e2bc4e1842638aa97a2d470c8a68}

SVG ファイルに埋め込まれ、代用変数を介してSVG テンプレートに渡されるすべてのカラー値は、`sRgb` カラースペースに存在すると見なされます。

SVGに画像を埋め込む際にカラー変換は行われません。 色を忠実に再現するには、すべての埋め込み画像リクエストで `icc=sRgb` を必ず指定してください。

ラスタライズ後、SVG画像は、他の画像と同様にカラーマネジメントに使用されます。

## 例 {#section-036cdd45abd449849ee00a8f21788c28}

次のSVG テンプレートは、画像の参照と変数の使用を示しています。

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

このSVG テンプレートは、次のように使用できます。

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## 制限 {#section-daa5eccd07204aaf993be41e87822d54}

SVG ファイルはスタンドアロンにする必要があり、画像サービングリクエストまたは画像レンダリングリクエストで参照される外部イメージを除き、セカンダリファイルやリソースを参照しないでください（上記を参照）。

静的コンテンツのみがレンダリングされます。 アニメーション、ボタンなどのインタラクティブ機能。 は存在しても、期待どおりにレンダリングされない場合があります。

ICC プロファイルベースのカラー仕様は、現時点ではサポートされていません。

`<script>` 要素が存在する場合がありますが、常に無視されます。

## 関連項目 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG 1.1 仕様 &#x200B;](https://www.w3.org/TR/SVG11/)
