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
>ネットパスのパイプ文字 (|) は、エラーのリダイレクトではサポートされていません。

## PS::errorRedirect.rootUrl — リダイレクトサーバ {#section-85f22e48d68842a490b0e1191543b558}

ルート URL ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]]) を使用して、ローカルで失敗した要求をリダイレクトするセカンダリ Image Serving デプロイメントを作成します。 この設定が空または定義されていない場合、エラーのリダイレクトは無効（デフォルト）になります。

## PS::errorRedirect.connectTimeout — リダイレクト接続のタイムアウト {#section-3971be8f720d4b32a2cc7860b4085971}

クライアントにエラーを返す前に、サーバがセカンダリサーバとの接続を確立するのを待機する最大時間（ミリ秒）。

## PS::errorRedirect.socketTimeout — リダイレクト応答のタイムアウト {#section-69d8579f748d4044bca99dfb64dd523c}

セカンダリサーバーがデータを返すのを待ってから、リダイレクトリクエストを破棄してクライアントにエラーを返すまでの最大時間（ミリ秒）です。
