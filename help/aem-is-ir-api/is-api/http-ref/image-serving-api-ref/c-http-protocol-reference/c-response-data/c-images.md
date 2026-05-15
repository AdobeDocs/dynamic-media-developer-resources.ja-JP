---
description: リクエストが正常に完了した場合、およびリクエストにreq= コマンドが含まれていない場合、またはreq=imgまたはreq=tmbの場合、画像データが返されます。
solution: Experience Manager
title: 画像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
TQID: 'https://experienceleague.adobe.com/1tStTbuCLrOG8XrPgOw5qH-VujpHXX8Pt0IWXg9329Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 1%

---

# 画像{#images}

リクエストが正常に完了した場合、およびリクエストにreq= コマンドが含まれていない場合、またはreq=imgまたはreq=tmbの場合、画像データが返されます。

HTTP応答のMIME タイプは`fmt=`によって決定されます。または、`fmt=`が指定されていない場合は`<image/jpeg>`です。

リクエストメソッドが無条件の`GET`または`HEAD`の場合、HTTP応答のステータスは「200 OK」です。

サーバーは、ステータス &#39;304&#39; （変更なし）で応答し、条件付き`GET` リクエスト （有効な`If-Modified-Since`または`If-None-Match` ヘッダーを含む）に応答して画像データを返さない場合があります。
