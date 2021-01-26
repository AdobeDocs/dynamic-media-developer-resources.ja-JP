---
description: ネストと埋め込みに関しては、いくつかの制限があります。
seo-description: ネストと埋め込みに関しては、いくつかの制限があります。
seo-title: 制限事項
solution: Experience Manager
title: 制限事項
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# 制限{#restrictions}

ネストと埋め込みに関しては、いくつかの制限があります。

サーバのパフォーマンスを高めるために、ネストされた要求によって返される画像の解像度は、マテリアルを適用するオブジェクトのテクスチャ解像度と適切に一致する必要があります。

外部画像はローカルにキャッシュされます。 このような画像に対する変更は、ローカルキャッシュエントリが古くなった後（期限切れのHTTPヘッダーに基づいて）にのみ検出されます。
