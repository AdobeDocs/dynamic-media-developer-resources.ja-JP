---
description: 画像アンカー： この画像をテンプレートまたは複合画像内のレイヤーとして使用する場合の起点。
solution: Experience Manager
title: アンカー
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
TQID: 'https://experienceleague.adobe.com/OKTbXTF3uzVcQeLQIGIJhCukQFzdW5gZMzatSdWP7yY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 4%

---

# アンカー{#anchor}

画像アンカー： この画像をテンプレートまたは複合画像内のレイヤーとして使用する場合の起点。

回転のデフォルトの中心点も定義します。

## プロパティ {#section-95740f14160744e7bc763094b8be40d8}

2つの整数。コンマで区切ります。 フル解像度イメージの左上隅を基準としたピクセルオフセット。

`anchor=`で上書きされました（次に`origin=`で上書きできます）。

## 初期設定 {#section-ca3a4cc837d643519eff15951f2b47a1}

画像の中心点は、このフィールドが存在しない場合、またはフィールドが空の場合、およびこれが有効な画像レコードの場合（つまり、`catalog::Path`が有効な場合）に使用されます。

## 関連項目 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md)、[origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
