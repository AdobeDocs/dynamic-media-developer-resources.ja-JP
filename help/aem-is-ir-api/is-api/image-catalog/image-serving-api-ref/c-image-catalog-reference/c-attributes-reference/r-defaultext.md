---
description: 初期設定の画像ファイルのサフィックス パスにファイルのサフィックスが含まれていない場合は、カタログの「パス」（またはカタログの「マスクパス」）フィールドの値に追加されます。
seo-description: 初期設定の画像ファイルのサフィックス パスにファイルのサフィックスが含まれていない場合は、カタログの「パス」（またはカタログの「マスクパス」）フィールドの値に追加されます。
seo-title: DefaultExt
solution: Experience Manager
title: DefaultExt
topic: Scene7 Image Serving - Image Rendering API
uuid: aa245d18-15cc-41cb-a49d-757d74fe6231
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# DefaultExt{#defaultext}

初期設定の画像ファイルのサフィックス パスにファイルのサフィックスが含まれていない場合は、catalog::Path（またはcatalog::MaskPath）フィールドの値に追加されます。

ファイルのサフィックスは、ピリオドと、文字列のピリオドから末尾までの1文字以上で構成されます。 パスがカタログエントリに解決されない場合、および最後のパス要素にファイルのサフィックスが含まれていない場合は、httpパスにサフィックスが追加されます。

## プロパティ {#section-b024e6450b414ccc8b83a48a3b4e00f9}

テキスト文字列。 先頭に「。」を含める必要があります。 および1つ以上の文字。

## 初期設定 {#section-1194c36ffe0748c5b9ff7d732a506588}

定義されていな `default::DefaultExt` い場合は、から継承。 定義済みで空の場合、このカタログを使用する際に画像名に初期設定のサフィックスが適用されません。

## 関連項目 {#section-d7c408b979844643adff8258f500eb7c}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) 、 [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
