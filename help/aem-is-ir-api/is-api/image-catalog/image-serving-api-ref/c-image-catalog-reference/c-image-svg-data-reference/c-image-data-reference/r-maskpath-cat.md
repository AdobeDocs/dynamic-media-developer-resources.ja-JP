---
description: マスクファイルのパス このカタログレコードに関連付けられているマスク画像ファイルの相対パスまたは絶対パスと名前。
seo-description: マスクファイルのパス このカタログレコードに関連付けられているマスク画像ファイルの相対パスまたは絶対パスと名前。
seo-title: MaskPath
solution: Experience Manager
title: MaskPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a2d1f08a-0a26-41a6-9be2-f5cc2afb15c4
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---


# MaskPath{#maskpath}

マスクファイルのパス このカタログレコードに関連付けられているマスク画像ファイルの相対パスまたは絶対パスと名前。

画像に別々のマスクを割り当てることができます。

サーバーは、[ソースデータの管理](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md)で説明されているパス解決規則を使用して、データファイルを検索します。

## プロパティ {#section-cdc3b7e2811e41008479cd97887c01b7}

テキスト文字列の値。 （オプション）指定する場合は、有効なImage Serverの相対ファイルパスまたは絶対ファイルパスを指定する必要があります。 `attribute::DefaultExt` ファイルのサフィックスがない場合は、

カタログレコードでメイン画像(`catalog::Path`)とマスク画像(`catalog::MaskPath`)の両方が定義されている場合、両方ともまったく同じピクセルサイズである必要があります。 マスク画像は8ビットのグレースケールにする必要があります。

`mask=` 」が上書きされ `catalog::MaskPath`ます。

`catalog::MaskPath` メインイメージ(  `catalog::Path`)のアルファチャネルが存在する場合、およびアルファチャネルが関連付けられていない場合（つまり、事前に乗算されていない場合）は、アルファイルが上書きされます。画像のアルファが事前に乗算される場合、`catalog::MaskPath`は無視され、アルファチャネルが常に使用されます。

## 初期設定 {#section-78533e35bfec469ba087cb68a35bb81b}

なし

## 関連項目 {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md),  [catalog:Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), mask= [, ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md) [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
