---
description: リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=imgまたはreq=tmbが含まれていない場合は、画像データが返されます。
seo-description: リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=imgまたはreq=tmbが含まれていない場合は、画像データが返されます。
seo-title: 画像
solution: Experience Manager
title: 画像
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# 画像{#images}

リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=imgまたはreq=tmbが含まれていない場合は、画像データが返されます。

HTTP応答のMIMEタイプは`fmt=`によって決定されます。`fmt=`が指定されていない場合は`<image/jpeg>`になります。

リクエストメソッドが無条件`GET`または`HEAD`の場合、HTTPレスポンスステータスは「200 OK」です。

サーバーはステータス&#39;304&#39; （変更されていません）で応答し、条件付き`GET`要求（有効な`If-Modified-Since`または`If-None-Match`ヘッダーを含む）に応答して画像データを返しません。
