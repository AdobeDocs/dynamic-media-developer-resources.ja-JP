---
description: リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=に次の値のいずれかが含まれている場合、画像データが返されます。
solution: Experience Manager
title: 画像
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---

# 画像{#images}

イメージデータは、リクエストが正常に完了し、リクエストにreq=コマンドが含まれていない場合、またはreq=に次の値のいずれかが含まれている場合に返されます。img, debug

HTTP応答のMIMEタイプは`fmt=`によって決まります。`fmt=`が指定されていない場合は、`attribute::Format`の値に依存します。

リクエストメソッドが無条件の`GET`または`HEAD`の場合、HTTP応答のステータスは「200 OK」です。

サーバーは、ステータス「304」（変更なし）で応答し、（`request-header`に[!DNL If-Modified-Since]フィールドが存在する）条件付き`GET`要求に応答して画像データを返さない場合があります。
