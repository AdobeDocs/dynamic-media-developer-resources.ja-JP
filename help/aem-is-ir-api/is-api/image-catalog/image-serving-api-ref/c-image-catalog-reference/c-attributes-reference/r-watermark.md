---
description: 透かしの選択 透かしの画像またはテンプレートとして使用するカタログレコードのカタログIDを指定します。
seo-description: 透かしの選択 透かしの画像またはテンプレートとして使用するカタログレコードのカタログIDを指定します。
seo-title: 透かし
solution: Experience Manager
title: 透かし
topic: Scene7 Image Serving - Image Rendering API
uuid: 18add7ab-0797-4ab3-a7e8-05c745abe605
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# 透かし{#watermark}

透かしの選択 透かしの画像またはテンプレートとして使用するカタログレコードのcatalog::Idを指定します。

指定した場合、サーバは要求されたすべてのイメージ要求のイメージデータに透かしを適用し `req=img`ます()。

## プロパティ {#section-fad6ffff4c5f4b5c8010281bc1377055}

テキスト文字列。 指定する場合、この画像カタログ( `Catalog::Id` またはで指定した場合はデフォルトのカタログ)の有効な値である必要があ [!DNL default.ini]ります。

## 初期設定 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

定義されていな `default::Watermark` い場合は、から継承。 定義済みで空白の場合、定義済みの画像カタログでも、透かしは適用さ `default::Watermark` れません。

## 関連項目 {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
