---
description: サーバーキャッシュをプリロードします。 req=imgと同様に要求を実行しますが、画像を返す代わりに、サーバーはMIMEタイプがtext/plainのテキストデータとして形式設定された返信画像(image.length)の長さを返します。
seo-description: サーバーキャッシュをプリロードします。 req=imgと同様に要求を実行しますが、画像を返す代わりに、サーバーはMIMEタイプがtext/plainのテキストデータとして形式設定された返信画像(image.length)の長さを返します。
seo-title: loadcache
solution: Experience Manager
title: loadcache
topic: Scene7 Image Serving - Image Rendering API
uuid: 44f0db05-2323-4aa2-853c-f78e656a4308
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# loadcache{#loadcache}

サーバーキャッシュをプリロードします。 req=imgと同様に要求を実行しますが、画像を返す代わりに、サーバーはMIMEタイプがtext/plainのテキストデータとして形式設定された返信画像(image.length)の長さを返します。

`req=loadcache`

HTTP応答はキャッシュできません。

リクエスト内の他のコマンドは、ドキュメントに従って適用されます。
