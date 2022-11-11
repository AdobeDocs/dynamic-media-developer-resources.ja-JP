---
description: すべてのログファイルは、TC ディレクトリで指定された同じログフォルダに書き込まれます。
solution: Experience Manager
title: サーバーログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# サーバーログ{#server-logging}

すべてのログファイルは、TC::directory で指定された同じログフォルダに書き込まれます。

ログファイルは通常、毎日作成および回転されます。 ログフォルダー内の古いログファイルは、指定された日数 ( `TC::maxDays`) をクリックします。

重要：ログファイルのディスク容量が不足するのを防ぐために、十分な容量のディスクを確保する必要があります。 頻繁に使用されるサーバーとデフォルトのログ設定には、1 ～ 2 GB/日が必要になる場合があります。

この [!DNL Platform Server] Image Server は、以下の 3 種類のログファイルを作成します。

その他の画像サービングコンポーネントと、Dynamic Mediaビューアなどのその他の特定のDynamic Mediaパッケージでも、同じフォルダーにログファイルが作成される場合があります。 これらのログファイルはDynamic Media内部での使用を目的としており、トラブルシューティングの目的でDynamic Mediaテクニカルサポートからリクエストされる場合があります。

* [アクセスログ](c-access-log.md)
* [トレースログ](c-trace-log.md)
* [Image Server ログ](c-image-server-log.md)

## 関連項目 {#section-5ff5e46031b1461c92de24e632610d6d}

[アクセスログ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [デバッグ/トレースログ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
