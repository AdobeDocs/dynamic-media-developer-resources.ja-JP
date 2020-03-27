---
description: すべてのログファイルは、TCディレクトリで指定された同じログフォルダに書き込まれます。
seo-description: すべてのログファイルは、TCディレクトリで指定された同じログフォルダに書き込まれます。
seo-title: サーバーログ
solution: Experience Manager
title: サーバーログ
topic: Scene7 Image Serving - Image Rendering API
uuid: f6145737-e4c3-4533-9be5-5b5a0202fe33
translation-type: tm+mt
source-git-commit: 5717550d2dea8ec086875e770ff8f200aaa75ff3

---


# サーバーログ{#server-logging}

すべてのログファイルは、TC::directoryで指定された同じログフォルダに書き込まれます。

ログファイルは通常、毎日作成および回転されます。 ログフォルダー内の古いログファイルは、指定された日数( `TC::maxDays`)が経過すると自動的に削除されます。

重要：ディスク容量の不足を避けるために、ログファイル用に十分な容量のディスクを確保する必要があります。 1 ～ 2 GB/日で、頻繁に使用されるサーバーとデフォルトのログ設定が必要になる場合があります。

Platform ServerとImage Serverは、以下に示す3種類のログファイルを作成します。

また、他の画像サービングコンポーネントや、Scene7ビューアなどの特定のScene7パッケージでも、同じフォルダにログファイルが作成される場合があります。 これらのログファイルはScene7内部での使用を目的としており、Scene7サポートから問題の発生を防ぐための要求がある場合があります。

* [アクセスログ](c-access-log.md)
* [トレースログ](c-trace-log.md)
* [Image Serverログ](c-image-server-log.md)

## 関連項目 {#section-5ff5e46031b1461c92de24e632610d6d}

[アクセスログ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)、デバ [ッグ/トレースログ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
