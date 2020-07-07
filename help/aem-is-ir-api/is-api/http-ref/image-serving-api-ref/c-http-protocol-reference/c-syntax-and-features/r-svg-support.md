---
description: 画像サービングは、ソースデータとしてScalable Vector Graphics(SVG)ファイルをサポートしています。 SVG 1.1への準拠が必要です。
seo-description: 画像サービングは、ソースデータとしてScalable Vector Graphics(SVG)ファイルをサポートしています。 SVG 1.1への準拠が必要です。
seo-title: SVGのサポート
solution: Experience Manager
title: SVGのサポート
topic: Scene7 Image Serving - Image Rendering API
uuid: 30d7b37d-fdef-4518-a4b3-4baee56fa634
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---


# SVGのサポート{#svg-support}

画像サービングは、ソースデータとしてScalable Vector Graphics(SVG)ファイルをサポートしています。 SVG 1.1への準拠が必要です。

画像サービングは静的SVGコンテンツのみを認識します。 アニメーション、スクリプティング、その他のインタラクティブコンテンツはサポートされていません。

画像ファイルが許可されている場所(URLパス、 `src=`および `mask=`)であれば、SVGを指定できます。 SVGファイルのコンテンツがラスタライズされると、画像と同じように処理されます。

画像と同様に、SVGファイルは画像カタログエントリまたは相対ファイルパスとして指定できます。

## 代替変数 {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` 置換変数は、SVGファイルの値文字列要素と要素属性に含めるこ `<text>` とができます。

埋め込まれた画像サービング要求のクエリ部分に含まれる重要な変数は、直接置換されません。 代わりに、使用可能な変数定義がすべてリクエストに追加されるので、画像サービングはリクエストの解析時に変数を置き換えることができます。

詳しくは、 [代替変数](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) (Substitution Variables)を参照してください。

## 画像参照 {#section-a7680f9e6aca4b1a83560637cc9fac66}

要素を使用して画像をSVGに挿入でき `<image>` ます。 要素の `xlink::href` 属性で参照される画像は、有効な画像サービング要求である必要があり `<image>` ます。 外部URLは使用できません。

で始まる完全な画像サービング要求またはで始まる相対URL `http://`を指定し `/is/image`ます。 完全なHTTPパスを指定した場合、ドメイン名はパスから削除され、相対形式に変換されます。 完全なHTTPパスを使用する方がメリットがあるのは、ファイルをサードパーティのSVGレンダラーでプレビューできるからです。

>[!NOTE]
>
>このリリースの画像サービングでは、画像のレンダリングのサポートが制限されています。 SVG内からの画像の参照は、従来の画像サービングのレイヤリングとテンプレート化のメカニズムが不十分で目的の結果を得られない状況でのみ使用してください。 いかなる場合でも、SVGを使用してマルチ画像コンポジットを生成する必要はありません。

>[!NOTE]
>
>SVGに埋め込まれた画像は、この時点で自動的にサイズ変更されません。 必要な画像サイズを設定するために必要な画像サービングコマンドがすべての画像HREFに含まれていることを確認します(例： `wid=`)をクリックします。 画像サイズが明示的に設定されていない場合 `attribute::DefaultPix` は、が適用されます。

## Color management {#section-ea76e2bc4e1842638aa97a2d470c8a68}

SVGファイルに埋め込まれ、置換変数を介してSVGテンプレートに渡されるカラー値は、すべて `sRgb` カラースペースに存在すると見なされます。

画像がSVGに埋め込まれている場合、色変換は行われません。 色を忠実に再現するには、すべての埋め込み画像要求に対して `icc=sRgb` を指定する必要があります。

ラスタライズ後は、SVG画像は他の画像と同様にカラーマネジメントに関与します。

## 例 {#section-036cdd45abd449849ee00a8f21788c28}

次のSVGテンプレートは、画像参照と変数の使用方法を説明しています。

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

このSVGテンプレートは次のように使用できます。

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrictions {#section-daa5eccd07204aaf993be41e87822d54}

SVGファイルはスタンドアロンである必要があり、セカンダリファイルやリソースを参照することはできません。ただし、画像サービングまたは画像レンダリング要求で参照される外部画像は例外です（上記を参照）。

静的コンテンツのみがレンダリングされます。 アニメーション、ボタンなどのインタラクティブ機能 は存在するが、期待どおりにレンダリングされない場合があります。

現時点では、ICCプロファイルベースのカラー仕様はサポートされていません。

`<script>` 要素は存在する場合がありますが、常に無視されます。

## 関連項目 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG 1.1仕様](http://www.w3.org/TR/SVG11/)
