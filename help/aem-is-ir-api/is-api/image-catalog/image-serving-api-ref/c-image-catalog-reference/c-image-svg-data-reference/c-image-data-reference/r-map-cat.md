---
description: 画像マップデータ。 なしまたはそれ以上の完全なHTML <area> 要素（前後に並べ替え）
solution: Experience Manager
title: マップ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---

# マップ{#map}

画像マップデータ。 なしまたはそれ以上の完全なHTML `<AREA>` 要素（前後に並べ替え）

サーバは SHAPE 属性と COORDS 属性を解釈し、変更する場合があります（このリリースでは SHAPE=CIRCLE はサポートされていません）。 のその他すべての属性 `<AREA>` は、変更されずに渡されます。 COORDS 属性で指定する座標値は、変更されていないソースイメージの左上隅からのピクセルオフセットである必要があります。 (`%` 座標はこのリリースではサポートされていないので、正しく処理されない可能性があります )。

## プロパティ {#section-f52d89fd399b4356ac05277e6c12f956}

テキスト文字列値。 指定する場合は、1 つ以上の完全なHTML `<AREA>` 要素。

このフィールドは、テキスト文字列のローカライゼーションに参加します。 参照： [テキスト文字列のローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) （内） *HTTP プロトコルリファレンス* 」を参照してください。

## 初期設定 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

なし

## 関連項目 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [テキスト文字列のローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
