---
description: 透かしの選択。 透かしの画像またはテンプレートとして使用するカタログレコードのカタログIDを指定します。
seo-description: 透かしの選択。 透かしの画像またはテンプレートとして使用するカタログレコードのカタログIDを指定します。
seo-title: 透かし
solution: Experience Manager
title: 透かし
topic: Scene7 Image Serving - Image Rendering API
uuid: 18add7ab-0797-4ab3-a7e8-05c745abe605
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# 透かし{#watermark}

透かしの選択。 透かしの画像またはテンプレートとして使用するカタログレコードのcatalog::Idを指定します。

指定した場合、サーバーは要求されたすべてのイメージ要求(`req=img`)のイメージデータに透かしを適用します。

## プロパティ {#section-fad6ffff4c5f4b5c8010281bc1377055}

テキスト文字列。 指定する場合、この画像カタログ（または[!DNL default.ini]で指定する場合は初期設定のカタログ）内の有効な`Catalog::Id`値である必要があります。

## 初期設定 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

定義されていない場合は`default::Watermark`から継承されます。 定義済みで空の場合、`default::Watermark`が定義されていても、この画像カタログに透かしは適用されません。

## 関連項目 {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
