---
description: Image Servingは、Scalable Vector Graphics （SVG）ファイルをソースデータとしてサポートしています。 SVG 1.1への準拠が必要です。
solution: Experience Manager
title: SVGサポート
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
TQID: 'https://experienceleague.adobe.com/yN93vSajgH09FJqxpDsa1j3fFlBR9EdCREXvhUy8q2U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 514
ht-degree: 0%

---

# SVGサポート{#svg-support}

Image Servingは、Scalable Vector Graphics （SVG）ファイルをソースデータとしてサポートしています。 SVG 1.1への準拠が必要です。

Image Servingは、静的なSVG コンテンツのみを認識します。アニメーション、スクリプト、およびその他のインタラクティブコンテンツはサポートされていません。

SVGは、画像ファイルが許可されている場所（URL パス、`src=`および`mask=`）で指定できます。 SVG ファイルの内容をラスタライズした後は、画像と同じように処理されます。

画像と同様に、SVG ファイルは、画像カタログエントリまたは相対ファイルパスとして指定できます。

## 置換変数 {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$`個の代用変数を、SVG ファイルの値文字列`<text>`要素および任意の要素属性に含めることができます。

埋め込み画像サービングリクエストのクエリ部分の重要な変数は、直接置き換えられません。 代わりに、使用可能なすべての変数定義がリクエストに追加されます。これにより、画像サービングは、リクエストを解析するときに変数を置き換えることができます。

詳細については、[置換変数](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)を参照してください。

## 画像参照 {#section-a7680f9e6aca4b1a83560637cc9fac66}

画像は、`<image>`要素を使用してSVGに挿入できます。 `<image>`要素の`xlink::href`属性で参照される画像は、有効な画像サービング要求である必要があります。 外部URLは使用できません。

`http://`で始まる完全な画像サービングリクエスト、または`/is/image`で始まる相対URLを指定します。 完全なHTTP パスを指定した場合、ドメイン名はパスから削除され、相対形式に変換されます。 サードパーティのSVG レンダラーを使用してファイルをプレビューできるため、完全なHTTP パスを使用すると便利です。

>[!NOTE]
>
>このリリースの画像サービングでの画像のレンダリングのサポートは限定的です。 SVG内からの画像の参照は、従来の画像サービングのレイヤー化とテンプレート化の仕組みが、望ましい結果を得るのに不十分な場合にのみ使用してください。 いかなる場合も、SVGを使用して複数の画像の合成を生成しないでください。

>[!NOTE]
>
>SVGに埋め込まれた画像は、現時点では自動的にサイズ変更されません。 すべての画像ヘッダーに、目的の画像サイズを設定するために必要な画像サービングコマンド（`wid=`など）が含まれていることを確認してください。 画像サイズが明示的に設定されていない場合、`attribute::DefaultPix`が適用されます。

## カラーマネジメント {#section-ea76e2bc4e1842638aa97a2d470c8a68}

SVG ファイルに埋め込まれ、代用変数を介してSVG テンプレートに渡されるすべてのカラー値は、`sRgb` カラースペースに存在すると見なされます。

SVGに画像を埋め込む場合、カラー変換は行われません。 カラーの忠実性を確保するには、埋め込まれたすべての画像リクエストに`icc=sRgb`を指定してください。

ラスタライズ後、SVG画像は他の画像と同様にカラーマネジメントに参加します。

## 例 {#section-036cdd45abd449849ee00a8f21788c28}

次のSVG テンプレートは、画像の参照と変数の使用を示しています。

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

このSVG テンプレートは、次のように使用できます。

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## 制限 {#section-daa5eccd07204aaf993be41e87822d54}

SVG ファイルはスタンドアロンである必要があり、Image ServingまたはImage Rendering リクエストで参照される外部イメージを除き、セカンダリファイルまたはリソースを参照してはなりません（上記を参照）。

静的コンテンツのみがレンダリングされます。 アニメーション、ボタンなどのインタラクティブ機能など。 存在する可能性がありますが、期待どおりにレンダリングされない可能性があります。

ICC プロファイルベースのカラー仕様は、現時点ではサポートされていません。

`<script>`個の要素が存在する可能性がありますが、常に無視されます。

## 関連項目 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、[mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、[SVG 1.1の仕様](https://www.w3.org/TR/SVG11/)
