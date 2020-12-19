---
description: 画像アンカー この接触チャネルがテンプレートまたは合成画像のレイヤーとして使用される場合の画像ポイント。
seo-description: 画像アンカー この接触チャネルがテンプレートまたは合成画像のレイヤーとして使用される場合の画像ポイント。
seo-title: アンカー
solution: Experience Manager
title: アンカー
topic: Scene7 Image Serving - Image Rendering API
uuid: 81069578-8470-4ec0-b755-47b0a8124024
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# アンカー{#anchor}

画像アンカー この接触チャネルがテンプレートまたは合成画像のレイヤーとして使用される場合の画像ポイント。

また、回転のデフォルトの中心点も定義します。

## プロパティ {#section-95740f14160744e7bc763094b8be40d8}

カンマで区切られた2つの整数。 最大解像度の画像の左上隅を基準とするピクセルオフセット。

`anchor=`によって上書きされます（これは`origin=`によって上書きできます）。

## 初期設定 {#section-ca3a4cc837d643519eff15951f2b47a1}

このフィールドが存在しない場合や空の場合、および有効な画像レコード（`catalog::Path`が有効な場合）は、画像の中心点が使用されます。

## 関連項目 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) 、 [接触チャネル=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
