---
description: サーバーキャッシュをプリロードします。 リクエストを req=img と同様に実行しますが、サーバーは画像を返す代わりに、返信画像の長さ（image.length）を、MIME タイプが text/plain のテキストデータとして書式設定されて返します。
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# loadcache{#loadcache}

サーバーキャッシュをプリロードします。 リクエストを req=img と同様に実行しますが、サーバーは画像を返す代わりに、返信画像の長さ（image.length）を、MIME タイプが text/plain のテキストデータとして書式設定されて返します。

`req=loadcache`

HTTP 応答はキャッシュできません。

リクエスト内の他のコマンドは、ドキュメントに記載されているように適用されます。
