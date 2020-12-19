---
description: アセットタイプ. カタログ画像セットに公開するセットの種類を識別するために使用します。
seo-description: アセットタイプ. カタログ画像セットに公開するセットの種類を識別するために使用します。
seo-title: AssetType
solution: Experience Manager
title: AssetType
topic: Scene7 Image Serving - Image Rendering API
uuid: e9e0d7e0-0429-4949-aafa-0ac7032fdfe5
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 14%

---


# AssetType{#assettype}

アセットタイプ. catalog::ImageSetに公開するセットの種類を識別するために使用します。

アセットタイプによって、`req=set`リクエストに対して生成される応答のタイプが決まります。 値が指定されていない場合、自動検出ルールは`req=set`応答タイプを決定します。

## プロパティ {#properties}

次のセットの列挙値：

MEDIASET

SPINSET

SPINSET2D

VIDEOSET

IMAGESET

ECATALOG

## 初期設定 {#section-b94ce61423194729918456103ef3f72c}

なし

## 関連項目 {#section-235f9f5522024d3682ee7cc0101eb7ba}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) 、 [req=set](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、 [メディアセットの要求](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md)
