---
description: 画像アンカー この画像をテンプレートまたは合成画像のレイヤーとして使用する場合の原点。
seo-description: 画像アンカー この画像をテンプレートまたは合成画像のレイヤーとして使用する場合の原点。
seo-title: アンカー
solution: Experience Manager
title: アンカー
topic: Scene7 Image Serving - Image Rendering API
uuid: 81069578-8470-4ec0-b755-47b0a8124024
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# アンカー{#anchor}

画像アンカー この画像をテンプレートまたは合成画像のレイヤーとして使用する場合の原点。

また、回転のデフォルトの中心点も定義します。

## プロパティ {#section-95740f14160744e7bc763094b8be40d8}

コンマで区切った2つの整数。 最大解像度の画像の左上隅を基準とするピクセルオフセット。

によって上 `anchor=`書きされます(これは、によって上書きで `origin=`きます)。

## 初期設定 {#section-ca3a4cc837d643519eff15951f2b47a1}

このフィールドが存在しない場合、または空の場合、および有効な画像レコード（が有効な場合）の場合は、画像の中心点が使 `catalog::Path` 用されます。

## 関連項目 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
