---
description: 画像マスク。 マスク（アルファ チャンネル）データを要求します。
solution: Experience Manager
title: マスク
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# マスク{#mask}

画像マスク。 マスク（アルファ チャンネル）データを要求します。

`req=mask`

`req=img` と同じコマンドをサポートします。 サーバも同じように処理しますが、RGBや RGBA のデータを返すのではなく、カラー情報を破棄し、マスク（アルファチャンネル）のデータのみを返します。 返信データの形式と応答の MIME タイプは、`fmt=` によって決まります。

HTTP 応答は、`catalog::Expiration` に基づく TTL でキャッシュ可能です。
