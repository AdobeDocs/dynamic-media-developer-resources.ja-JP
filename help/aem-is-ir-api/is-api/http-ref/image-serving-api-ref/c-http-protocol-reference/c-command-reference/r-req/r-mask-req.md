---
description: イメージマスク。 マスク（アルファチャンネル）データを要求します。
solution: Experience Manager
title: マスク
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# マスク{#mask}

イメージマスク。 マスク（アルファチャンネル）データを要求します。

`req=mask`

`req=img`と同じコマンドをサポートします。 サーバーでも同じ方法で処理されますが、RGBまたはRGBAデータを返す代わりに、サーバーはカラー情報を破棄し、マスク（アルファチャンネル）データのみを返します。 応答データの形式と応答のMIMEタイプは`fmt=`によって決まります。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。
