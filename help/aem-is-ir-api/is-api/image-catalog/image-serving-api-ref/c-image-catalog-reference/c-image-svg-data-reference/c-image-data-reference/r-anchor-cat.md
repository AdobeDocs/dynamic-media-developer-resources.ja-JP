---
description: 画像アンカー この接触チャネルがテンプレートまたは合成画像のレイヤーとして使用される場合の画像ポイント。
solution: Experience Manager
title: アンカー
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '119'
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
