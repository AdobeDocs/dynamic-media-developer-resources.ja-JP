---
description: サーフェスの粗さ： マテリアル サーフェスの相対的な光沢度を指定します。 カタログの種類とカタログ光沢と組み合わせて使用すると、3D リフレクションレンダーエフェクトを制御できます。
solution: Experience Manager
title: ラフネス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
TQID: 'https://experienceleague.adobe.com/YvUmUkOLzzbM7Zs-7T35rwYRNrUeh6-QXW339AA3R8Q'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 2%

---

# ラフネス{#roughness}

サーフェスの粗さ： マテリアル サーフェスの相対的な光沢度を指定します。 catalog::Typeおよびcatalog::Glossと組み合わせて使用すると、3D リフレクションレンダーエフェクトを制御できます。

## プロパティ {#section-70c3f2394fd8477ca83a369448907971}

整数。 0...100の範囲のパーセント値。 すべてのマテリアルに対してオプションです。 複数のリフレクションマップを持つビネットまたは3D リフレクション機能を持つビネットにのみ使用します。 不明な場合や不要な場合は、空のままにするか、-1に設定します。

## 初期設定 {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; サーバーのデフォルトが使用されます。

## 関連項目 {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[ ラフ=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)、[ カタログ：：光沢](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)、[ カタログ：：タイプ ](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)

