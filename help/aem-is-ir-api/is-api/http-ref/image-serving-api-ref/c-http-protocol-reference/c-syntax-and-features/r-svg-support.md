---
description: 画像サービングは、ソースデータとしてScalable Vector Graphics(SVG)ファイルをサポートしています。 SVG 1.1への準拠が必要です。
seo-description: 画像サービングは、ソースデータとしてScalable Vector Graphics(SVG)ファイルをサポートしています。 SVG 1.1への準拠が必要です。
seo-title: SVGのサポート
solution: Experience Manager
title: SVGのサポート
topic: Scene7 Image Serving - Image Rendering API
uuid: 30d7b37d-fdef-4518-a4b3-4baee56fa634
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SVGのサポート{#svg-support}

画像サービングは、ソースデータとしてScalable Vector Graphics(SVG)ファイルをサポートしています。 SVG 1.1への準拠が必要です。

画像サービングは静的SVGコンテンツのみを認識します。アニメーション、スクリプティング、その他のインタラクティブコンテンツはサポートされていません。

画像ファイル（URLパス、および）が許可されている場所では、SVGを指 `src=`定でき `mask=`ます。 SVGファイルのコンテンツをラスタライズすると、画像と同じように処理されます。

画像と同様に、SVGファイルは、画像カタログエントリまたは相対ファイルパスとして指定できます。

## 代替変数 {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` 置換変数は、SVGファイルの値文字列要素と要素属性に含める `<text>` ことができます。

重要な変数は、埋め込まれた画像サービング要求のクエリ部分で直接置き換えられるものではありません。 代わりに、使用可能なすべての変数定義がリクエストに追加され、イメージサービングはリクエストの解析時に変数を置き換えることができます。

詳細は [、「置換変数](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) 」を参照してください。

## 画像参照 {#section-a7680f9e6aca4b1a83560637cc9fac66}

要素を使用して画像をSVGに挿入でき `<image>` ます。 要素の属性で参照される `xlink::href` 画像は、有効な `<image>` 画像サービング要求である必要があります。 外部URLは使用できません。

で始まる完全な画像サービング要求またはで始 `http://`まる相対URLを指定します `/is/image`。 完全なHTTPパスを指定した場合、ドメイン名はパスから削除され、相対形式に変換されます。 完全なHTTPパスを使用すると、ファイルをサードパーティのSVGレンダラーでプレビューできるので、便利です。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>このリリースの画像サービングでの画像のレンダリングのサポートは限られています。 SVG内からの画像の参照は、従来の画像サービングのレイヤー化とテンプレート化のメカニズムで目的の結果を得るには不十分な状況でのみ使用してください。 いかなる状況でも、SVGを使用してマルチ画像の合成を生成する必要はありません。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>SVGに埋め込まれた画像は、現時点では自動的にサイズ変更されません。 すべての画像参照に、必要な画像サービングコマンドが含まれていて、必要な画像サイズ(例： `wid=`)。 画像サイズが明示的に設定されていない場合は、 `attribute::DefaultPix` が適用されます。

## Color management {#section-ea76e2bc4e1842638aa97a2d470c8a68}

SVGファイルに埋め込まれ、置換変数を介してSVGテンプレートに渡されるすべてのカラー値は、カラースペースに存在すると見 `sRgb` なされます。

画像がSVGに埋め込まれている場合、色変換は行われません。 色を忠実に再現するには、すべての埋め込み画像要 `icc=sRgb` 求に対してを指定します。

ラスタライズ後、SVG画像は他の画像と同様にカラーマネジメントに関与します。

## 例 {#section-036cdd45abd449849ee00a8f21788c28}

次のSVGテンプレートは、画像参照と変数の使用方法を示しています。

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

このSVGテンプレートは次のように使用します。

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrictions {#section-daa5eccd07204aaf993be41e87822d54}

SVGファイルはスタンドアロンである必要があり、セカンダリファイルやリソースを参照してはなりません。ただし、画像サービングまたは画像レンダリング要求で参照される外部画像は例外です（上記を参照）。

静的コンテンツのみがレンダリングされます。 アニメーション、ボタンなどのインタラクティブ機能 は存在するが、期待どおりにレンダリングされない場合があります。

現時点では、ICCプロファイルベースのカラー仕様はサポートされていません。

`<script>` 要素は存在する場合がありますが、常に無視されます。

## 関連項目 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG 1.1仕様](http://www.w3.org/TR/SVG11/)
