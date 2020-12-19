---
description: 画像マスク マスク(アルファチャネル)データを要求します。
seo-description: 画像マスク マスク(アルファチャネル)データを要求します。
seo-title: mask
solution: Experience Manager
title: mask
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# mask{#mask}

画像マスク マスク(アルファチャネル)データを要求します。

`req=mask`

`req=img`と同じコマンドをサポートし、サーバで同じように処理されますが、RGBやRGBAデータを返す代わりに、サーバは色情報を破棄し、マスク(アルファチャネル)データのみを返します。 応答データの形式と応答のMIMEタイプは`fmt=`によって決定されます。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。
