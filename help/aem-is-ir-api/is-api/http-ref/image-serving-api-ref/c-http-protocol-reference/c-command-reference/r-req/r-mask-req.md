---
description: イメージマスク。 マスク（アルファチャンネル）データを要求します。
solution: Experience Manager
title: マスク
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# マスク{#mask}

イメージマスク。 マスク（アルファチャンネル）データを要求します。

`req=mask`

`req=img`と同じコマンドをサポートします。 サーバーでも同じ方法で処理されますが、RGBまたはRGBAデータを返す代わりに、サーバーはカラー情報を破棄し、マスク（アルファチャンネル）データのみを返します。 応答データの形式と応答のMIMEタイプは`fmt=`によって決まります。

HTTP応答は、`catalog::Expiration`に基づいてTTLでキャッシュ可能です。
