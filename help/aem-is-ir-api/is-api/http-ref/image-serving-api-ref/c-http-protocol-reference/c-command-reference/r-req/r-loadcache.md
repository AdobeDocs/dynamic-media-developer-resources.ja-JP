---
description: サーバーキャッシュをプリロードします。 req=imgと同様に要求を実行しますが、画像を返す代わりに、サーバーはMIMEタイプがtext/plainのテキストデータとして形式設定された返信画像(image.length)の長さを返します。
solution: Experience Manager
title: loadcache
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# loadcache{#loadcache}

サーバーキャッシュをプリロードします。 req=imgと同様に要求を実行しますが、画像を返す代わりに、サーバーはMIMEタイプがtext/plainのテキストデータとして形式設定された返信画像(image.length)の長さを返します。

`req=loadcache`

HTTP応答はキャッシュできません。

リクエスト内の他のコマンドは、ドキュメントに従って適用されます。
