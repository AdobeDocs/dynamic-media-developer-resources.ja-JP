---
description: これらのサーバー設定を使用して、エラーをリダイレクトします。
seo-description: これらのサーバー設定を使用して、エラーをリダイレクトします。
seo-title: エラーリダイレクト
solution: Experience Manager
title: エラーリダイレクト
topic: Scene7 Image Serving - Image Rendering API
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# エラーリダイレクト{#error-redirection}

これらのサーバー設定を使用して、エラーをリダイレクトします。

>[!NOTE]
>
>ネットパスのパイプ文字(|)は、エラーリダイレクトに対してはサポートされていません。

## PS::errorRedirect.rootUrl — リダイレクトサーバー {#section-85f22e48d68842a490b0e1191543b558}

ルートURL ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]])を参照してください。 この設定が空か、定義されていない場合、エラーリダイレクトは無効（デフォルト）になります。

## PS::errorRedirect.connectTimeout — リダイレクト接続のタイムアウト {#section-3971be8f720d4b32a2cc7860b4085971}

クライアントにエラーを返す前に、サーバがセカンダリサーバとの接続が確立されるのを待機する最大時間（ミリ秒）。

## PS::errorRedirect.socketTimeout — リダイレクト応答のタイムアウト {#section-69d8579f748d4044bca99dfb64dd523c}

リダイレクト要求を中断してクライアントにエラーを返す前に、サーバーがセカンダリサーバーがデータを返すのを待機する最大時間（ミリ秒）。
