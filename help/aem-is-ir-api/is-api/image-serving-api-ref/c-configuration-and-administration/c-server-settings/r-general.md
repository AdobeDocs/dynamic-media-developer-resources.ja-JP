---
description: 一般的なサーバー設定
solution: Experience Manager
title: 一般
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# 一般{#general}

一般的なサーバー設定

## TC::PsPort — メインリスニングポート {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Platform Server のメインリスニングポートを指定します。 また、このポートは、画像サービング、画像レンダリング、Dynamic Mediaビューア（インストールされている場合）のドキュメントおよび例ページへのアクセスにも使用されます。

## IS::CacheServerUrl — サービスのルート URL をキャッシュする {#section-bcca227a1f91453b834db4ea050968e2}

Image Server がキャッシュサービスにアクセスできるようにする HTTP ルートパスを指定します。 をに設定する必要があります [!DNL http://localhost:TC::PsPort /is/cache/secondary]（ポート番号が一致する） `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration — リモートImage Sourceのデフォルト TTL {#section-e4c31228b459492cacd2f482d9575f71}

HTTP 経由でリモートソースから取得された、キャッシュされた画像の TTL ( `src={…}` 構築。 リモートサーバーの HTTP 応答に Expiration ヘッダーが含まれていない場合にのみ使用されます。 秒単位の整数値。

## IS::RemoteUrlTimeout — リモートImage Sourceタイムアウト {#section-437646c479cc4bea81dae42100a3c50a}

Image Server が、リモートサーバーが要求されたイメージファイルを HTTP 経由で配信してからエラーを返すのを待機する時間です。 秒単位の整数値。

## PS::allowDefaultCatalogRequests — デフォルトのカタログ要求を有効化/無効化 {#section-484e442a115a49b4ac269d1718b351e1}

パスに有効なカタログ ID を含まない要求を許可しない場合は、false に設定します。 初期設定は `true`. に設定する場合 `false`の場合、カタログ ID のないリクエストに対してエラーが返されます。

>[!NOTE]
>
>`req=catalogprops` はこの設定の対象ではありません。

## PS::saveToFile.saveTimeout — ファイルの保存タイムアウト {#section-d22afd8ad86144b28684ed95a59db40e}

のデフォルトのタイムアウト値 `req=saveToFile` when `timeout=`が指定されていません。 `msec`. 指定した時間内に保存操作が完了しなかった場合は、エラーが返されます。
