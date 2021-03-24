---
description: リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=に次の値imgのいずれかが含まれている場合、イメージデータが返されます。debug
solution: Experience Manager
title: 画像
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 1%

---


# 画像{#images}

リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=に次のいずれかの値が含まれている場合、画像データが返されます。img、debug

HTTP応答のMIMEタイプは`fmt=`によって決定されます。`fmt=`が指定されていない場合は、`attribute::Format`の値に依存します。

リクエストメソッドが無条件`GET`または`HEAD`の場合、HTTPレスポンスステータスは「200 OK」です。

サーバーはステータス&#39;304&#39;（変更されていません）で応答する場合があり、（`request-header`に[!DNL If-Modified-Since]フィールドが存在する）条件付き`GET`リクエストに応答して画像データを返しません。
