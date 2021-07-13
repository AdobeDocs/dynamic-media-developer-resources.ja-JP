---
description: イメージデータは、リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=imgまたはreq=tmbが含まれていない場合に返されます。
solution: Experience Manager
title: 画像
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---

# 画像{#images}

イメージデータは、リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=imgまたはreq=tmbが含まれていない場合に返されます。

HTTP応答のMIMEタイプは`fmt=`によって決まります。`fmt=`が指定されていない場合は`<image/jpeg>`になります。

リクエストメソッドが無条件の`GET`または`HEAD`の場合、HTTP応答のステータスは「200 OK」です。

サーバーはステータス「304」（変更なし）で応答し、（有効な`If-Modified-Since`または`If-None-Match`ヘッダーを含む）条件付き`GET`リクエストに応答して画像データを返さない場合があります。
