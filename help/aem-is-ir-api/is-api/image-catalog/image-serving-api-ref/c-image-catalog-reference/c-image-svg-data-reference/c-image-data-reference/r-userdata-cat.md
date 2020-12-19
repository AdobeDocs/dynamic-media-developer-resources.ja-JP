---
description: ユーザデータ. サーバーは、req=userdataに応答して、このフィールドの内容をクライアントに返します。
seo-description: ユーザデータ. サーバーは、req=userdataに応答して、このフィールドの内容をクライアントに返します。
seo-title: ユーザデータ
solution: Experience Manager
title: ユーザデータ
topic: Scene7 Image Serving - Image Rendering API
uuid: cadc9f3c-c0ca-4c88-bc8a-97c28b439b01
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 9%

---


# ユーザデータ{#userdata}

ユーザデータ. サーバーは、req=userdataに応答して、このフィールドの内容をクライアントに返します。

## プロパティ {#section-06f2002b77d54a64be07f12fff54ad13}

テキスト文字列の値。 [プロパティデータ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md)の形式を使用することをお勧めします。 プロパティデータの形式設定を使用しない場合、テキスト文字列に「=」文字を含めることはできません。

ズーム、スピン、パンフレットの各ビューアのお客様は、このフィールドでプロパティデータの形式設定が使用されると想定しています。 これらのクライアントは、ビューアの設定とカスタマイズにこのフィールドを使用します。 詳しくは、Viewerのドキュメントを参照してください。

このフィールドは、テキスト文字列ローカライゼーションに関与します。 詳しくは、『*HTTPプロトコルリファレンス*』の[テキスト文字列ローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)を参照してください。

## 初期設定 {#section-7ee879762130467199745f2abc662f1e}

なし

## 関連項目 {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [テキスト文字列ローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
