---
title: 制限事項
description: ネストと埋め込みには、一部の制限が適用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# 制限事項{#restrictions}

ネストと埋め込みには、一部の制限が適用されます。

サーバのパフォーマンスを高めるために、ネストされた要求で返される画像の解像度は、マテリアルが適用されるオブジェクトのテクスチャ解像度に合理的に一致する必要があります。

外部画像はローカルにキャッシュされます。 このような画像に対する変更は、ローカルキャッシュエントリが古くなった（期限切れの HTTP ヘッダーに基づく）後にのみ検出されます。
