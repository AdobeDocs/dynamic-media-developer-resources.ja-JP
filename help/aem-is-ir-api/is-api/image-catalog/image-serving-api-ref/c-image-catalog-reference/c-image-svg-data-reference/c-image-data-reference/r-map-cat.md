---
description: 画像マップデータ。 完全なHTML <AREA>要素が1つもないかそれ以上なく、前から後ろに並べ替えられます。
seo-description: 画像マップデータ。 完全なHTML <AREA>要素が1つもないかそれ以上なく、前から後ろに並べ替えられます。
seo-title: マップ
solution: Experience Manager
title: マップ
topic: Scene7 Image Serving - Image Rendering API
uuid: 674a7a74-91bf-41c4-ab74-a5cb4f8abe1d
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 5%

---


# マップ{#map}

画像マップデータ。 完全なHTML `<AREA>`要素が1つもないか、それ以上なくて、前から後ろに並べ替えられています。

サーバはSHAPE属性とCOORDS属性を解釈し、変更する場合があります。 （SHAPE=CIRCLEは、このリリースではサポートされていません）。 `<AREA>`のその他の属性は、変更なしに渡されます。 COORDS属性で指定する座標値は、変更されていないソース画像の左上隅からのピクセルオフセットである必要があります。 （`%`座標はこのリリースではサポートされておらず、正しく処理されない場合があります）。

## プロパティ {#section-f52d89fd399b4356ac05277e6c12f956}

テキスト文字列の値。 指定する場合は、1つ以上の完全なHTML `<AREA>`要素である必要があります。

このフィールドは、テキスト文字列ローカライゼーションに関与します。 詳しくは、『*HTTPプロトコルリファレンス*』の[テキスト文字列ローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)を参照してください。

## 初期設定 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

なし

## 関連項目 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) 、 [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、 [テキスト文字列ローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
