---
description: すべてのログファイルは、TCディレクトリで指定された同じログフォルダに書き込まれます。
solution: Experience Manager
title: サーバーログ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# サーバーログ{#server-logging}

すべてのログファイルは、TC::directoryで指定された同じログフォルダーに書き込まれます。

ログファイルは通常、毎日作成および回転されます。 ログフォルダー内の古いログファイルは、指定日数(`TC::maxDays`)が経過すると自動的に削除されます。

重要：ディスク容量の不足を回避するために、ログファイル用に十分なディスク容量を確保する必要があります。 1 ～ 2 GB/日は、頻繁に使用されるサーバーとデフォルトのログ設定に必要な場合があります。

プラットフォームサーバとImage Serverは、以下に示す3種類のログファイルを作成します。

その他の画像サービングコンポーネントや、Dynamic Mediaビューアなどの特定のDynamic Mediaパッケージでも、同じフォルダーにログファイルが作成される場合があります。 これらのログファイルはDynamic Media社内での使用を目的としており、トラブルシューティングの目的で、Dynamic Mediaのテクニカルサポートに依頼する場合があります。

* [アクセスログ](c-access-log.md)
* [トレースログ](c-trace-log.md)
* [Image Serverログ](c-image-server-log.md)

## 関連項目 {#section-5ff5e46031b1461c92de24e632610d6d}

[アクセスログ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)、 [デバッグ/トレースログ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
