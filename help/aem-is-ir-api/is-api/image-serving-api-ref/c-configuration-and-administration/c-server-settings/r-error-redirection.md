---
description: これらのサーバー設定を使用して、エラーをリダイレクトします。
solution: Experience Manager
title: エラーリダイレクト
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# エラーリダイレクト{#error-redirection}

これらのサーバー設定を使用して、エラーをリダイレクトします。

>[!NOTE]
>
>ネット パスのパイプ文字（|）は、エラーのリダイレクトではサポートされていません。

## PS::errorRedirect.rootUrl - リダイレクトサーバー {#section-85f22e48d68842a490b0e1191543b558}

ローカルで失敗した要求をリダイレクトする必要があるセカンダリ イメージ サービング展開のルート URL （ HTTP:// *[!DNL domain]*[: *[!DNL port]*]）。 この設定が空か定義されていない場合、エラーのリダイレクトは無効（既定）になります。

## PS::errorRedirect.connectTimeout - リダイレクト接続のタイムアウト {#section-3971be8f720d4b32a2cc7860b4085971}

セカンダリ サーバーとの接続が確立されるまで、サーバーがエラーをクライアントに返すまでの最大時間（ミリ秒）。

## PS::errorRedirect.socketTimeout - リダイレクト応答のタイムアウト {#section-69d8579f748d4044bca99dfb64dd523c}

セカンダリ サーバーがデータを返すのをサーバーが待ってから、リダイレクト要求を破棄してクライアントにエラーを返すまでの最大時間（ミリ秒）。
