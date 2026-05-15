---
description: IS サーバーは、正常に開いたり読み取ったりできないソースイメージを含むリクエストに対して、代替サーバーにフェイルオーバーするように設定できます。
solution: Experience Manager
title: エラー時にリダイレクト
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
TQID: 'https://experienceleague.adobe.com/jNvJP4nJ7W1thf-ZDbSCzry54H8wI4DVGK8FW6koNCw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 0%

---

# エラー時にリダイレクト{#redirect-on-error}

IS サーバーは、正常に開いたり読み取ったりできないソースイメージを含むリクエストに対して、代替サーバーにフェイルオーバーするように設定できます。

次のタイプのリクエストはリダイレクトされます。

* IS カタログ内の画像で、ディスク上にない画像。

  画像がカタログ内にない場合、画像が見つからないときにエラーリダイレクトは発生しません。

* 画像、カラープロファイル、またはフォントが破損している。
* 静的コンテンツがディスク上に見つかりません。

  参照された静的コンテンツにカタログレコードがない場合でも、ディスク上に静的コンテンツリクエストが見つからない場合にリダイレクトされます。

エラーリダイレクトは、他の場合には発生しません。

有効な場合と、リクエストの処理中にそのようなエラーが発生した場合、プライマリサーバーはリクエストをセカンダリサーバーに送信して処理します。 応答は、成功または失敗を示すかどうかに関係なく、クライアントに直接転送されます。 プライマリサーバーは、そのような転送済み要求のログエントリをキャッシュ使用`REMOTE`でマークします。 応答データは、プライマリサーバーによってローカルにキャッシュされません。

エラーリダイレクトは、セカンダリサーバーのHTTP ドメイン名とポート番号に`PS::errorRedirect.rootUrl`を設定することで有効になります。 さらに、接続タイムアウトは`PS::errorRedirect.connectTimeout`で設定され、プライマリサーバーがセカンダリサーバーからの応答を待ってからクライアントにエラーを返す最大時間は`PS::errorRedirect.socketTimeout`で設定されます。

>[!NOTE]
>
>セカンダリサーバーに接続できない場合、デフォルトの画像またはエラーイメージが設定されていても、テキストエラー応答がクライアントに返されます。

>[!NOTE]
>
>ネットパスのパイプ文字（|）は、エラーリダイレクトではサポートされていません。

## 関連項目 {#section-2e8bfc128b944baf8108279d16492f3f}

[エラーリダイレクト](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
