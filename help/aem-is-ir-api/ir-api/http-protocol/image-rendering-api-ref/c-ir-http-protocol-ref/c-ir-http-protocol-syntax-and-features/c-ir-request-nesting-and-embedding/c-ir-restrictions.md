---
description: ネストと埋め込みには、一部の制限が適用されます。
solution: Experience Manager
title: 制限事項
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# 制限事項{#restrictions}

ネストと埋め込みには、一部の制限が適用されます。

サーバのパフォーマンスを向上させるために、ネストされた要求で返される画像の解像度は、マテリアルが適用されるオブジェクトのテクスチャ解像度と合理的に一致する必要があります。

外部画像はローカルにキャッシュされます。 このような画像に対する変更は、ローカルキャッシュエントリが古くなった後に（期限切れのHTTPヘッダーに基づいて）検出されます。
