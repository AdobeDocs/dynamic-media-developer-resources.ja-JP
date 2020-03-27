---
description: ネストと埋め込みには、いくつかの制限が適用されます。
seo-description: ネストと埋め込みには、いくつかの制限が適用されます。
seo-title: 制限
solution: Experience Manager
title: 制限
topic: Scene7 Image Serving - Image Rendering API
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Restrictions{#restrictions}

ネストと埋め込みには、いくつかの制限が適用されます。

サーバのパフォーマンスを高めるには、ネストされた要求によって返される画像の解像度は、マテリアルが適用されるオブジェクトのテクスチャ解像度と適切に一致する必要があります。

外部画像はローカルにキャッシュされます。 このような画像に対する変更は、ローカルキャッシュエントリが古くなった後（期限切れのHTTPヘッダーに基づく）にのみ検出されます。
