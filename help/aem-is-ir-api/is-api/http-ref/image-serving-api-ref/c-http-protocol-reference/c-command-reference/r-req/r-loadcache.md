---
description: サーバーキャッシュをプリロードします。 req=imgと同様に要求を実行しますが、画像を返す代わりに、サーバーはMIMEタイプがtext/plainのテキストデータとして形式設定された返信画像(image.length)の長さを返します。
seo-description: サーバーキャッシュをプリロードします。 req=imgと同様に要求を実行しますが、画像を返す代わりに、サーバーはMIMEタイプがtext/plainのテキストデータとして形式設定された返信画像(image.length)の長さを返します。
seo-title: loadcache
solution: Experience Manager
title: loadcache
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 44f0db05-2323-4aa2-853c-f78e656a4308
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# loadcache{#loadcache}

サーバーキャッシュをプリロードします。 req=imgと同様に要求を実行しますが、画像を返す代わりに、サーバーはMIMEタイプがtext/plainのテキストデータとして形式設定された返信画像(image.length)の長さを返します。

`req=loadcache`

HTTP応答はキャッシュできません。

リクエスト内の他のコマンドは、ドキュメントに従って適用されます。
