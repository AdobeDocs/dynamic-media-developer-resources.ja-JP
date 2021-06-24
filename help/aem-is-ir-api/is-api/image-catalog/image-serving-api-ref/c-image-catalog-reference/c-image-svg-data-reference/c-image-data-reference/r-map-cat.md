---
description: 画像マップデータ。 ない、または完全なHTMLの<AREA>要素（前後に並べ替え）。
solution: Experience Manager
title: マップ
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 5%

---

# マップ{#map}

画像マップデータ。 HTMLの`<AREA>`要素が1つもないか、1つ前後に並べ替えられた完全な要素。

サーバはSHAPE属性とCOORDS属性を解釈し、変更する場合があります。 （このリリースでは、SHAPE=CIRCLEはサポートされていません）。 `<AREA>`のその他の属性は、すべて変更されずに渡されます。 COORDS属性で指定する座標値は、変更されていないソースイメージの左上隅からのピクセルオフセットでなければなりません。 （`%`座標はこのリリースではサポートされていないので、正しく処理されない可能性があります）。

## プロパティ {#section-f52d89fd399b4356ac05277e6c12f956}

テキスト文字列の値。 指定する場合は、1つ以上の完全なHTML `<AREA>`要素である必要があります。

このフィールドは、テキスト文字列のローカライゼーションに関与します。 詳しくは、「*HTTPプロトコルリファレンス*」の「[テキスト文字列のローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)」を参照してください。

## 初期設定 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

なし

## 関連項目 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) 、  [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、テキスト文字列のローカ [ライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
