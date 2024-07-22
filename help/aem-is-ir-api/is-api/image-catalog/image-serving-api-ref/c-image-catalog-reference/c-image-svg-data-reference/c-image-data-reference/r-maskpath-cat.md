---
description: マスクファイルパス。 このカタログレコードに関連付けられているマスク画像ファイルの相対パスまたは絶対パスと名前。
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# MaskPath{#maskpath}

マスクファイルパス。 このカタログレコードに関連付けられているマスク画像ファイルの相対パスまたは絶対パスと名前。

画像に個別のマスクを付加できます。

サーバーは、[Source データの管理 ](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) に記載されているパス解決ルールを使用して、データファイルを検索します。

## プロパティ {#section-cdc3b7e2811e41008479cd97887c01b7}

テキスト文字列値。 オプション。 Image Server の有効な相対ファイルパスまたは絶対ファイルパスを指定する必要があります。 ファイルのサフィックスが存在しない場合は、`attribute::DefaultExt` が追加されます。

メイン画像（`catalog::Path`）とマスク画像（`catalog::MaskPath`）の両方がカタログレコードで定義されている場合、両方ともピクセルサイズがまったく同じである必要があります。 マスク イメージは 8 ビット グレースケールでなければなりません。

リクエストの `mask=` は `catalog::MaskPath` を上書きします。

`catalog::MaskPath` は、メイン イメージ内のアルファ チャンネル（`catalog::Path`）が存在する場合、およびアルファ チャンネルが関連付けられていない（つまり、事前に合成されていない）場合は、そのアルファ チャンネルをオーバーライドします。 イメージのアルファ値が事前に乗算されている場合、`catalog::MaskPath` は無視され、アルファ チャンネルが常に使用されます。

## 初期設定 {#section-78533e35bfec469ba087cb68a35bb81b}

なし

## 関連項目 {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)、[attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md)、[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c)、[mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md)、[req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
