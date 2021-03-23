---
description: 画像マスク マスク(アルファチャネル)データを要求します。
seo-description: 画像マスク マスク(アルファチャネル)データを要求します。
seo-title: mask
solution: Experience Manager
title: mask
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# mask{#mask}

画像マスク マスク(アルファチャネル)データを要求します。

`req=mask`

`req=img`と同じコマンドをサポートし、サーバで同じように処理されますが、RGBやRGBAデータを返す代わりに、サーバは色情報を破棄し、マスク(アルファチャネル)データのみを返します。 応答データの形式と応答のMIMEタイプは`fmt=`によって決定されます。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。
