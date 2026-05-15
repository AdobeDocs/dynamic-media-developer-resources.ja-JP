---
description: サーバーキャッシュのプリロード。 req=imgと同じようにリクエストを実行しますが、画像を返す代わりに、MIME タイプ text/plainを持つテキストデータとしてフォーマットされた返信画像（image.length）の長さを返します。
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
TQID: 'https://experienceleague.adobe.com/Llp-0huLGkxBVxSgRngyAtNKqeHuZ02xJu71MM-Nqww'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# loadcache{#loadcache}

サーバーキャッシュのプリロード。 req=imgと同じようにリクエストを実行しますが、画像を返す代わりに、MIME タイプ text/plainを持つテキストデータとしてフォーマットされた返信画像（image.length）の長さを返します。

`req=loadcache`

HTTP応答はキャッシュできません。

リクエスト内のその他のコマンドは、ドキュメントに従って適用されます。
