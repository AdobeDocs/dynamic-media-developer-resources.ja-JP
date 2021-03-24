---
description: 画像サイズ. カタログパスで参照されている最大解像度の画像のピクセルサイズです。
solution: Experience Manager
title: サイズ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 9%

---


# サイズ{#size}

画像サイズ. catalog::Pathで参照される最大解像度画像のピクセルサイズ。

この値を指定すると、画像サービングはこの値を使用して、実際の画像サイズを取得するために画像を開く必要がなくなります。

>[!NOTE]
>
>`catalog::Size`が指定され、実際の最大解像度の画像サイズと異なる場合、未定義の動作が発生する可能性があります。

## プロパティ {#section-5c914ec8b1444a8e99d811b647cd42a3}

0より大きい2つの整数で、それぞれをコンマで区切ります。 （オプション）

## 初期設定 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

フィールドが存在しない場合、またはフィールドが空の場合は、画像の実際のサイズが使用されます。

## 関連項目 {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) 、 [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
