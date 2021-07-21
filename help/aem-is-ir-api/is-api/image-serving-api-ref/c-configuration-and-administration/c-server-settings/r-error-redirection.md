---
description: これらのサーバー設定を使用して、エラーをリダイレクトします。
solution: Experience Manager
title: エラーリダイレクト
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# エラーリダイレクト{#error-redirection}

これらのサーバー設定を使用して、エラーをリダイレクトします。

>[!NOTE]
>
>ネットパス内のパイプ文字(|)は、エラーのリダイレクトに対してはサポートされていません。

## PS::errorRedirect.rootUrl — リダイレクトサーバー {#section-85f22e48d68842a490b0e1191543b558}

ルートURL ( [!DNL HTTP:// *[!DNL domain]*[:*[!DNL port]*])をセカンダリImage Servingデプロイメント用に書き込みます。 この設定が空または定義されていない場合、エラーのリダイレクトは無効（デフォルト）になります。

## PS::errorRedirect.connectTimeout — リダイレクト接続のタイムアウト {#section-3971be8f720d4b32a2cc7860b4085971}

クライアントにエラーを返す前に、セカンダリサーバーとの接続が確立されるのをサーバーが待機する最大時間（ミリ秒）です。

## PS::errorRedirect.socketTimeout — リダイレクト応答のタイムアウト {#section-69d8579f748d4044bca99dfb64dd523c}

最大時間（ミリ秒）。セカンダリサーバーがデータを返すのを待ってから、リダイレクトリクエストを破棄してクライアントにエラーを返します。
