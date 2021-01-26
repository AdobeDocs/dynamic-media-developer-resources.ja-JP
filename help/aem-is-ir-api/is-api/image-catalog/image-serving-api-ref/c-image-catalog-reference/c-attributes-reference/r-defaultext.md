---
description: 初期設定の画像ファイルサフィックス パスにファイルのサフィックスが含まれない場合は、カタログの「パス」（または「カタログのMaskPath」）フィールドの値に追加されます。
seo-description: 初期設定の画像ファイルサフィックス パスにファイルのサフィックスが含まれない場合は、カタログの「パス」（または「カタログのMaskPath」）フィールドの値に追加されます。
seo-title: DefaultExt
solution: Experience Manager
title: DefaultExt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: aa245d18-15cc-41cb-a49d-757d74fe6231
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# DefaultExt{#defaultext}

初期設定の画像ファイルサフィックス パスにファイルのサフィックスが含まれない場合は、catalog::Path（またはcatalog::MaskPath）フィールドの値に追加されます。

ファイルのサフィックスは、ピリオドと、ピリオドから文字列の末尾までの1文字以上で構成されます。 パスがカタログエントリに解決されない場合、および最後のパス要素にファイルサフィックスが含まれない場合は、httpパスにサフィックスが追加されます。

## プロパティ {#section-b024e6450b414ccc8b83a48a3b4e00f9}

テキスト文字列。 先頭に「。」を付ける必要があります。 および1つ以上の文字。

## 初期設定 {#section-1194c36ffe0748c5b9ff7d732a506588}

定義されていない場合は`default::DefaultExt`から継承されます。 定義済みで空の場合、このカタログを使用するときに、画像名に初期設定のサフィックスが適用されません。

## 関連項目 {#section-d7c408b979844643adff8258f500eb7c}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
