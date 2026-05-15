---
description: 画像マップデータ： HTML <AREA>の要素が前後順に並べ替えられ、完全に完成したものはありません。
solution: Experience Manager
title: マップ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
TQID: 'https://experienceleague.adobe.com/JY0barcvbF72sTyYW4iIhjFE-8tfqtbI78PDccLcXV0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 2%

---

# マップ{#map}

画像マップデータ： 前面から背面に並べ替えられた、完全なHTML `<AREA>`要素はありません。

サーバーはSHAPEおよびCOORDS属性を解釈し、変更する可能性があります（SHAPE=CIRCLEはこのリリースではサポートされていません）。 `<AREA>`の他のすべての属性は、変更なしで渡されます。 COORDS属性で指定された座標値は、変更されていないソース画像の左上隅からのピクセルオフセットである必要があります。 （`%`座標は、このリリースではサポートされていないため、正しく処理されない可能性があります）。

## プロパティ {#section-f52d89fd399b4356ac05277e6c12f956}

テキスト文字列値。 指定する場合は、1つ以上の完全なHTML `<AREA>`要素である必要があります。

このフィールドは、テキスト文字列のローカライズに参加します。 詳しくは、*HTTP プロトコルリファレンス*&#x200B;の[&#x200B; テキスト文字列のローカライゼーション &#x200B;](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)を参照してください。

## 初期設定 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

なし

## 関連項目 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md)、[req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、[&#x200B; テキスト文字列のローカライズ &#x200B;](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
