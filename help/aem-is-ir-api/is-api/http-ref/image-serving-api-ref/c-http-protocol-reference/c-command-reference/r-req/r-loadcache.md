---
description: サーバーキャッシュをプリロードします。 req=imgと同様に要求を実行しますが、画像を返す代わりに、サーバーはMIMEタイプがtext/plainのテキストデータとして書式設定された返信画像の長さ(image.length)を返します。
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# loadcache{#loadcache}

サーバーキャッシュをプリロードします。 req=imgと同様に要求を実行しますが、画像を返す代わりに、サーバーはMIMEタイプがtext/plainのテキストデータとして書式設定された返信画像の長さ(image.length)を返します。

`req=loadcache`

HTTP応答はキャッシュできません。

リクエスト内の他のコマンドは、説明に従って適用されます。
