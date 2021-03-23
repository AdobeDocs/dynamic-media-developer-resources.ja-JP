---
description: 次のサーバー設定を使用して、エラーをリダイレクトします。
seo-description: 次のサーバー設定を使用して、エラーをリダイレクトします。
seo-title: エラーリダイレクト
solution: Experience Manager
title: エラーリダイレクト
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# エラーリダイレクト{#error-redirection}

次のサーバー設定を使用して、エラーをリダイレクトします。

>[!NOTE]
>
>ネットパスのパイプ文字(|)は、エラーリダイレクトに対してはサポートされていません。

## PS::errorRedirect.rootUrl — リダイレクトサーバー{#section-85f22e48d68842a490b0e1191543b558}

ルートURL ([!DNL HTTP:// *[!DNL domain]*[:*[!DNL port]*])を参照)に設定されます。 この設定が空か、定義されていない場合、エラーリダイレクトは無効になっています（デフォルト）。

## PS::errorRedirect.connectTimeout — リダイレクト接続のタイムアウト{#section-3971be8f720d4b32a2cc7860b4085971}

クライアントにエラーを返す前に、サーバーがセカンダリサーバーとの接続が確立されるのを待機する最大時間（ミリ秒）です。

## PS::errorRedirect.socketTimeout — リダイレクト応答のタイムアウト{#section-69d8579f748d4044bca99dfb64dd523c}

リダイレクト要求を破棄してクライアントにエラーを返す前に、セカンダリサーバーがデータを返すまでの最大待機時間（ミリ秒）。
