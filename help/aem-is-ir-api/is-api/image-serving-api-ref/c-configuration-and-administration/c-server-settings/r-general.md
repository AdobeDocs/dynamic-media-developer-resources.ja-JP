---
description: 一般的なサーバー設定
solution: Experience Manager
title: 一般
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
TQID: 'https://experienceleague.adobe.com/hjww7EYpf4xNxpUFQ1fudMOqNtokgykthwhonn78ZFE'
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
source-wordcount: 227
ht-degree: 0%

---

# 一般{#general}

一般的なサーバー設定

## TC::PsPort - メイン リスニング ポート {#section-d31d3051aa994a76b60b70c3d9f7e89f}

[!DNL Platform Server]のメイン リスニング ポートを指定します。 このポートは、画像サービング、画像レンダリング、Dynamic Media ビューア（インストールされている場合）のドキュメントとサンプルページにアクセスするためにも使用されます。

## IS::CacheServerUrl - Caching Service ルート Url {#section-bcca227a1f91453b834db4ea050968e2}

Image ServerがキャッシングサービスにアクセスできるようにするためのHTTP ルートパスを指定します。 ポート番号が`TC::PsPort`に一致する[!DNL http://localhost:TC::PsPort /is/cache/secondary]に設定する必要があります。

## IS::RemoteUrlDefaultExpiration - リモート Image Sourceのデフォルト TTL {#section-e4c31228b459492cacd2f482d9575f71}

`src={…}` コンストラクトを使用してリモート ソースからHTTPを介して取得された、キャッシュされた画像のTTL。 リモートサーバーがHTTP応答に有効期限ヘッダーを含まない場合にのみ使用されます。 整数値（秒単位）。

## IS::RemoteUrlTimeout - リモート Image Source タイムアウト {#section-437646c479cc4bea81dae42100a3c50a}

Image Serverが、リクエストされた画像ファイルをHTTP経由でリモートサーバーが配信するのを待ってからエラーを返す時間。 整数値（秒単位）。

## PS::allowDefaultCatalogRequests - デフォルトのカタログリクエストを有効/無効にする {#section-484e442a115a49b4ac269d1718b351e1}

パスに有効なカタログ IDを含まないリクエストを許可しない場合は、falseに設定します。 デフォルトは`true`です。 `false`に設定すると、カタログ IDのないリクエストに対してエラーが返されます。

>[!NOTE]
>
>`req=catalogprops`はこの設定の対象ではありません。

## PS::saveToFile.saveTimeout - ファイルの保存タイムアウト {#section-d22afd8ad86144b28684ed95a59db40e}

`timeout=`が指定されていない場合の`req=saveToFile`のデフォルトのタイムアウト値。 `msec`. 指定した時間内に保存操作が完了しない場合は、エラーが返されます。
