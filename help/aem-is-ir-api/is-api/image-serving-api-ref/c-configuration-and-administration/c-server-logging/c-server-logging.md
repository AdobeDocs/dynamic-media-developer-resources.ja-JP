---
description: すべてのログ ファイルは、TC ディレクトリで指定された同じログ フォルダに書き込まれます。
solution: Experience Manager
title: サーバーログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# サーバーログ{#server-logging}

すべてのログファイルは、TC::directory で指定した同じログフォルダに書き込まれます。

通常、ログファイルは毎日作成およびローテーションされます。 ログフォルダー内の古いログファイルは、指定した日数（`TC::maxDays`）が経過すると自動的に削除されます。

重要：ディスク領域が不足しないように、ログファイル用に十分なディスク領域を予約する必要があります。 頻繁に使用されるサーバーとデフォルトのログ設定では、1～2 GB/日が必要になる場合があります。

[!DNL Platform Server] と Image Server は、以下に説明する 3 種類のログファイルを作成します。

他の画像サービングコンポーネントや、Dynamic Media ビューアなどの他の特定のDynamic Media パッケージでも、同じフォルダーにログファイルを作成する場合があります。 これらのログファイルはDynamic Mediaの内部使用のためのものであり、トラブルシューティング目的でDynamic Media テクニカルサポートからリクエストされる場合があります。

* [アクセスログ](c-access-log.md)
* [トレース ログ](c-trace-log.md)
* [Image Server ログ](c-image-server-log.md)

## 関連項目 {#section-5ff5e46031b1461c92de24e632610d6d}

[ アクセス ログ ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)、[ デバッグ/トレース ログ ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
