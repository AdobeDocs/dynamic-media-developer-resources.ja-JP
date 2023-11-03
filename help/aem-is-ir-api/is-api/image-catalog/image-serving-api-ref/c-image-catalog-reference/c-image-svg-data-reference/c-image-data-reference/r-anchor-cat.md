---
description: 画像アンカー。 この画像がテンプレートまたは合成画像のレイヤーとして使用される場合の基準点。
solution: Experience Manager
title: アンカー
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# アンカー{#anchor}

画像アンカー。 この画像がテンプレートまたは合成画像のレイヤーとして使用される場合の基準点。

回転の既定の中心点も定義します。

## プロパティ {#section-95740f14160744e7bc763094b8be40d8}

コンマで区切られた 2 つの整数。 最大解像度の画像の左上隅を基準としたピクセルオフセット。

上書き元 `anchor=`（次に、を使用して上書きできます）。 `origin=`) をクリックします。

## 初期設定 {#section-ca3a4cc837d643519eff15951f2b47a1}

このフィールドが存在しない場合、または空の場合は画像の中心点が使用され、これが有効な画像レコード ( `catalog::Path` は有効です )。

## 関連項目 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
