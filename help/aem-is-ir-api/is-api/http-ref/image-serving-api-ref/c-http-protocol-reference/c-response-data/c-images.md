---
description: リクエストが正常に完了し、リクエストに req= コマンドが含まれていない場合、または req=img または req=tmb である場合、画像データが返されます。
solution: Experience Manager
title: 画像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---

# 画像{#images}

リクエストが正常に完了し、リクエストに req= コマンドが含まれていない場合、または req=img または req=tmb である場合、画像データが返されます。

HTTP 応答の MIME タイプは、`fmt=` によって決定されます。`fmt=` を指定しない場合は、`<image/jpeg>` になります。

リクエストメソッドが無条件の `GET` または `HEAD` の場合、HTTP 応答のステータスは「200 OK」です。

サーバーは、ステータス「304」（未変更）で応答し、条件付き `GET` リクエスト（有効な `If-Modified-Since` または `If-None-Match` ヘッダーを含む）に応答して画像データを返さない場合があります。
