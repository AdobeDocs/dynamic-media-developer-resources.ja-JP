---
description: ISサーバーは、開くことや読み取りが正常に行われないソースイメージを含む要求に対して、代替サーバーにフェイルオーバーするように設定できます。
solution: Experience Manager
title: エラー時にリダイレクト
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# エラー時にリダイレクト{#redirect-on-error}

ISサーバーは、開くことや読み取りが正常に行われないソースイメージを含む要求に対して、代替サーバーにフェイルオーバーするように設定できます。

次のタイプのリクエストがリダイレクトされます。

* カタログ内にあるがディスク上にはないIS画像。

   画像がカタログ内にない場合、画像が見つからない場合は、エラーリダイレクトは発生しません。

* 破損した画像、カラープロファイルまたはフォント。
* 静的コンテンツがディスクに見つかりません。

   静的コンテンツの要求は、参照先の静的コンテンツにカタログレコードがない場合でも、ディスクに見つからない場合にリダイレクトされます。

エラーのリダイレクトは、それ以外の場合は発生しません。

有効にすると、要求の処理中にこのようなエラーが発生した場合、プライマリサーバは処理のためにセカンダリサーバに要求を送信します。 応答は、成功または失敗を示しているかどうかに関係なく、クライアントに直接転送されます。 プライマリサーバーは、転送された要求のログエントリをキャッシュ使用`REMOTE`でマークします。 応答データは、プライマリサーバーによってローカルにキャッシュされません。

エラーリダイレクトは、`PS::errorRedirect.rootUrl`をセカンダリサーバーのHTTPドメイン名とポート番号に設定することで有効にします。 さらに、接続タイムアウトは`PS::errorRedirect.connectTimeout`で設定され、プライマリサーバーがセカンダリサーバーからの応答を待機する最大時間で、クライアントにエラーが返されるまでの最大時間は`PS::errorRedirect.socketTimeout`で設定されます。

>[!NOTE]
>
>セカンダリサーバーに接続できない場合、デフォルトのイメージまたはエラーイメージが設定されている場合でも、テキストエラー応答がクライアントに返されます。

>[!NOTE]
>
>ネットパスのパイプ文字(|)は、エラーリダイレクトに対してはサポートされていません。

## 関連項目 {#section-2e8bfc128b944baf8108279d16492f3f}

[エラーリダイレクト](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
