---
title: 制限
description: ネストと埋め込みには、いくつかの制限があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# 制限{#restrictions}

ネストと埋め込みには、いくつかの制限があります。

サーバのパフォーマンスを向上させるには、ネストされたリクエストによって返されるイメージの解像度を、マテリアルが適用されているオブジェクトのテクスチャ解像度と合理的に一致させる必要があります。

外部画像はローカルにキャッシュされます。 このような画像に対する変更は、ローカルキャッシュエントリが古くなった後（expires HTTP ヘッダーに基づく）にのみ検出されます。
