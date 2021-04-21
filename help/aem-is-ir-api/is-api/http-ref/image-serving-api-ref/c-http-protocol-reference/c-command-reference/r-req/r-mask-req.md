---
description: 画像マスク マスク(アルファチャネル)データを要求します。
solution: Experience Manager
title: mask
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# mask{#mask}

画像マスク マスク(アルファチャネル)データを要求します。

`req=mask`

`req=img`と同じコマンドをサポートします。 サーバーでも同じように処理されますが、RGBデータやRGBAデータを返す代わりに、カラーチャネルを破棄し、マスク（アルファ情報）データのみを返します。 応答データの形式と応答のMIMEタイプは`fmt=`によって決定されます。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。
