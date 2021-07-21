---
description: すべてのログファイルは、TCディレクトリで指定された同じログフォルダに書き込まれます。
solution: Experience Manager
title: サーバーログ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# サーバーログ{#server-logging}

すべてのログファイルは、TC::directoryで指定された同じログフォルダに書き込まれます。

ログファイルは、通常、毎日作成および回転されます。 ログフォルダー内の古いログファイルは、指定された日数(`TC::maxDays`)が経過すると自動的に削除されます。

重要：ディスク領域の不足を避けるために、ログファイルに十分な容量のディスクを確保する必要があります。 1 ～ 2 GB/日は、頻繁に使用されるサーバーとデフォルトのログ設定に必要な場合があります。

Platform ServerとImage Serverは、以下に示す3種類のログファイルを作成します。

その他の画像サービングコンポーネントと、Dynamic Mediaビューアなどの特定のDynamic Mediaパッケージでも、同じフォルダーにログファイルが作成される場合があります。 これらのログファイルはDynamic Media内部での使用を目的としており、トラブルシューティングのためにDynamic Mediaテクニカルサポートからリクエストされる場合があります。

* [アクセスログ](c-access-log.md)
* [トレースログ](c-trace-log.md)
* [Image Serverログ](c-image-server-log.md)

## 関連項目 {#section-5ff5e46031b1461c92de24e632610d6d}

[アクセスログ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)、デバ [ッグ/トレースログ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
