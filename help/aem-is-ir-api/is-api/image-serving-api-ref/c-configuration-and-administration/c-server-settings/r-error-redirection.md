---
description: これらのサーバー設定を使用して、エラーをリダイレクトします。
solution: Experience Manager
title: エラーリダイレクト
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
TQID: 'https://experienceleague.adobe.com/3fcob7pfE-bMms-4PtD5MKkcolKHmXEWdzEL7vgzLhc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# エラーリダイレクト{#error-redirection}

これらのサーバー設定を使用して、エラーをリダイレクトします。

>[!NOTE]
>
>ネットパスのパイプ文字（|）は、エラーリダイレクトではサポートされていません。

## PS::errorRedirect.rootUrl - リダイレクトサーバー {#section-85f22e48d68842a490b0e1191543b558}

ローカルで失敗したリクエストをリダイレクトするセカンダリ Image Serving デプロイメントのルート URL （ [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]）。 この設定が空であるか定義されていない場合、エラーリダイレクトは無効（デフォルト）になります。

## PS::errorRedirect.connectTimeout - リダイレクト接続タイムアウト {#section-3971be8f720d4b32a2cc7860b4085971}

サーバーがセカンダリサーバーとの接続が確立されるのを待ってから、クライアントにエラーを返す最大時間（ミリ秒単位）。

## PS::errorRedirect.socketTimeout - リダイレクト応答タイムアウト {#section-69d8579f748d4044bca99dfb64dd523c}

リダイレクトリクエストを放棄してクライアントにエラーを返す前に、セカンダリサーバーがデータを返すのをサーバーが待機する最大時間（ミリ秒）。
