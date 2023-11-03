---
description: 画像サービングは、ソースデータとして Scalable Vector Graphics(SVG) ファイルをサポートしています。 SVG1.1 への準拠が必要です。
solution: Experience Manager
title: SVGのサポート
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# SVGのサポート{#svg-support}

画像サービングは、ソースデータとして Scalable Vector Graphics(SVG) ファイルをサポートしています。 SVG1.1 への準拠が必要です。

画像サービングは静的なSVGコンテンツのみを認識します。アニメーション、スクリプティング、その他のインタラクティブコンテンツはサポートされません。

SVGは、画像ファイルが許可されている場所 (URL パス、 `src=`、および `mask=`) をクリックします。 ラスタライズされたSVGファイルのコンテンツは、画像と同じように処理されます。

画像と同様に、SVGファイルは、画像カタログエントリまたは相対ファイルパスとして指定できます。

## 代替変数 {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` 代替変数は、値文字列のSVG・ファイルに含めることができます。 `<text>` 要素および任意の要素属性。

重要埋め込み画像サービング要求のクエリ部分の変数は、直接置き換えられません。 代わりに、使用可能なすべての変数定義が要求に追加され、画像サービングは要求の解析時に変数を置き換えることができます。

詳しくは、 [代替変数](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) を参照してください。

## 画像参照 {#section-a7680f9e6aca4b1a83560637cc9fac66}

画像をSVGに挿入するには、 `<image>` 要素を選択します。 で参照される画像 `xlink::href` の属性 `<image>` 要素は、有効な画像サービング要求である必要があります。 外部 URL は許可されていません。

次の文字列で始まる完全な画像サービング要求を指定します。 `http://`または相対 url （で始まる） `/is/image`. 完全な HTTP パスを指定した場合、そのパスからドメイン名が削除され、相対形式に変換されます。 フル HTTP パスを使用すると、サードパーティのSVGレンダラーでファイルをプレビューできるので、便利です。

>[!NOTE]
>
>このリリースの画像サービングでの画像のレンダリングのサポートは制限されています。 SVG内から画像を参照する場合は、従来の画像サービングのレイヤーとテンプレート化のメカニズムが不十分で目的の結果が得られない場合にのみ使用してください。 状況に応じて、SVGを使用してマルチイメージコンポジットを生成しないでください。

>[!NOTE]
>
>SVGに埋め込まれた画像は、現時点では自動的にサイズ変更されません。 必要な画像サイズ（例： ）を設定するために、すべての画像の href に必要な画像サービングコマンドが含まれていることを確認します。 `wid=`) をクリックします。 画像サイズを明示的に設定しない場合、 `attribute::DefaultPix` が適用されます。

## カラーマネジメント {#section-ea76e2bc4e1842638aa97a2d470c8a68}

SVGファイルに埋め込まれ、代替変数を使用してSVGテンプレートに渡されるすべての色の値は、 `sRgb` カラースペース。

画像が画像に埋め込まれる場合、色変換はSVGされません。 色の忠実性を確保するには、必ず `icc=sRgb` すべての埋め込みイメージリクエストに対して。

ラスタライズ後は、SVG画像は他の画像と同様にカラーマネジメントに参加します。

## 例 {#section-036cdd45abd449849ee00a8f21788c28}

次のSVGテンプレートは、画像参照と変数の使用方法を示しています。

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

このSVGテンプレートは、次のように使用できます。

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## 制限事項 {#section-daa5eccd07204aaf993be41e87822d54}

SVGファイルは、スタンドアロンである必要があり、画像サービングまたは画像レンダリング要求で参照される外部画像を除き、セカンダリファイルやリソースを参照しないでください（上記を参照）。

静的コンテンツのみがレンダリングされます。 アニメーション、インタラクティブ機能（ボタンなど）。 が存在するが、期待どおりにレンダリングされない場合があります。

現時点では、ICC プロファイルベースのカラー仕様はサポートされていません。

`<script>` 要素は存在する場合がありますが、常に無視されます。

## 関連項目 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG1.1 の仕様](https://www.w3.org/TR/SVG11/)
