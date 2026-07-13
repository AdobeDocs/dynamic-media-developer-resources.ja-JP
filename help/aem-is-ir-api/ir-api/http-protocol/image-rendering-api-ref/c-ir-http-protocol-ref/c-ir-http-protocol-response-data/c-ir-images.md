---
title: 図
description: リクエストが正常に完了した場合、およびリクエストにreq= コマンドが含まれていない場合、またはreq=に次の値imgがある場合は、debugを返します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
TQID: 'https://experienceleague.adobe.com/4wHyyXX0gxz9ojr5g5Puu5fBhKXo4hZDjyBuVTao3rQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 1%

---

# 画像{#images}

リクエストが正常に完了した場合、およびリクエストにreq= コマンドが含まれていない場合、またはreq=に次のいずれかの値がある場合は、画像データが返されます。img, debug

HTTP応答のMIME タイプは`fmt=`によって決まります。または、`fmt=`が指定されていない場合は、`attribute::Format`の値によって決まります。

リクエストメソッドが無条件の`GET`または`HEAD`の場合、HTTP応答のステータスは「200 OK」です。

サーバーは、ステータス &#39;304&#39; （変更なし）で応答し、条件付き`GET`要求（`request-header`に[!DNL If-Modified-Since] フィールドが存在）に応答して画像データを返さない場合があります。

