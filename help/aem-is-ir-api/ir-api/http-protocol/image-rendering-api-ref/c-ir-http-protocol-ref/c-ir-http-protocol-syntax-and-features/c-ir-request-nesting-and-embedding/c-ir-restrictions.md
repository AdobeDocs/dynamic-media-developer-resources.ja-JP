---
description: ネストと埋め込みに関しては、いくつかの制限があります。
solution: Experience Manager
title: 制限事項
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# 制限{#restrictions}

ネストと埋め込みに関しては、いくつかの制限があります。

サーバのパフォーマンスを高めるために、ネストされた要求によって返される画像の解像度は、マテリアルを適用するオブジェクトのテクスチャ解像度と適切に一致する必要があります。

外部画像はローカルにキャッシュされます。 このような画像に対する変更は、ローカルキャッシュエントリが古くなった後（期限切れのHTTPヘッダーに基づいて）にのみ検出されます。
