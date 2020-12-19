---
description: リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=に次の値imgのいずれかが含まれている場合、イメージデータが返されます。debug
seo-description: リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=に次の値imgのいずれかが含まれている場合、イメージデータが返されます。debug
seo-title: 画像
solution: Experience Manager
title: 画像
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---


# 画像{#images}

リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=に次のいずれかの値が含まれている場合、画像データが返されます。img、debug

HTTP応答のMIMEタイプは`fmt=`によって決定されます。`fmt=`が指定されていない場合は、`attribute::Format`の値に依存します。

リクエストメソッドが無条件`GET`または`HEAD`の場合、HTTPレスポンスステータスは「200 OK」です。

サーバーはステータス&#39;304&#39;（変更されていません）で応答する場合があり、（`request-header`に[!DNL If-Modified-Since]フィールドが存在する）条件付き`GET`リクエストに応答して画像データを返しません。
