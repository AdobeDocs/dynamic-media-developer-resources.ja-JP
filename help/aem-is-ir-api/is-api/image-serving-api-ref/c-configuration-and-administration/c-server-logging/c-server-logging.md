---
description: すべてのログファイルは、TC ディレクトリで指定された同じログフォルダーに書き込まれます。
solution: Experience Manager
title: サーバーログ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
TQID: 'https://experienceleague.adobe.com/9I1gAXWb1Rpuml9WCCVPVC7FrpVazWN79Sk0-bb-tDc'
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
source-wordcount: 170
ht-degree: 1%

---

# サーバーログ{#server-logging}

すべてのログファイルは、TC::directoryで指定された同じログフォルダーに書き込まれます。

ログファイルは通常、毎日作成およびローテーションされます。 ログフォルダー内の古いログファイルは、指定された日数（`TC::maxDays`）が経過すると自動的に削除されます。

重要ディスク容量が不足しないように、ログファイル用に十分な量のディスク容量を確保する必要があります。 頻繁に使用されるサーバーとデフォルトのログ設定には、1～2 GB/日が必要になる場合があります。

[!DNL Platform Server]とImage Serverは、以下に説明する3種類のログファイルを作成します。

その他の画像サービングコンポーネントや、Dynamic Media ビューアなどの特定のDynamic Media パッケージも、同じフォルダーにログファイルを作成できます。 これらのログファイルはDynamic Mediaの内部使用を目的としたもので、Dynamic Media テクニカルサポートからトラブルシューティング用にリクエストされることがあります。

* [アクセスログ](c-access-log.md)
* [トレースログ](c-trace-log.md)
* [Image Server ログ](c-image-server-log.md)

## 関連項目 {#section-5ff5e46031b1461c92de24e632610d6d}

[&#x200B; アクセス ログ &#x200B;](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)、[&#x200B; デバッグ/トレース ログ &#x200B;](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
