---
description: 画像マスク マスク（アルファチャンネル）データを要求します。
seo-description: 画像マスク マスク（アルファチャンネル）データを要求します。
seo-title: mask
solution: Experience Manager
title: mask
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mask{#mask}

画像マスク マスク（アルファチャンネル）データを要求します。

`req=mask`

と同じコマンドをサポートし、 `req=img`サーバでも同じ方法で処理されますが、RGBまたはRGBAデータを返す代わりに、サーバはカラー情報を破棄し、マスク（アルファチャンネル）データのみを返します。 応答データの形式と応答のMIMEタイプは、によって決定されま `fmt=`す。

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.
