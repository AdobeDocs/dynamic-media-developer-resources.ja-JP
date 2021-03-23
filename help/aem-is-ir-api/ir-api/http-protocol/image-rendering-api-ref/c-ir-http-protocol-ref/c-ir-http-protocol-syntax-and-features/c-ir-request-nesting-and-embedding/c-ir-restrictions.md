---
description: ネストと埋め込みに関しては、いくつかの制限があります。
seo-description: ネストと埋め込みに関しては、いくつかの制限があります。
seo-title: 制限事項
solution: Experience Manager
title: 制限事項
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# 制限{#restrictions}

ネストと埋め込みに関しては、いくつかの制限があります。

サーバのパフォーマンスを高めるために、ネストされた要求によって返される画像の解像度は、マテリアルを適用するオブジェクトのテクスチャ解像度と適切に一致する必要があります。

外部画像はローカルにキャッシュされます。 このような画像に対する変更は、ローカルキャッシュエントリが古くなった後（期限切れのHTTPヘッダーに基づいて）にのみ検出されます。
