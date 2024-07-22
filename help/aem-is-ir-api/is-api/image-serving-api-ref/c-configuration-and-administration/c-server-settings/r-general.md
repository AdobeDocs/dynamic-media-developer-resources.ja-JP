---
description: サーバーの一般設定
solution: Experience Manager
title: 一般
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 一般{#general}

サーバーの一般設定

## TC::PsPort - メインリスニングポート {#section-d31d3051aa994a76b60b70c3d9f7e89f}

[!DNL Platform Server] のメイン リスニング ポートを指定します。 また、画像サービング、画像レンダリングおよびDynamic Media ビューア（インストールされている場合）のドキュメントページやサンプルページにもアクセスするために使用します。

## IS::CacheServerUrl - キャッシュサービスのルート Url {#section-bcca227a1f91453b834db4ea050968e2}

Image Server がキャッシュサービスにアクセスできるようにする HTTP ルートパスを指定します。 `TC::PsPort` に一致するポート番号を使用して、[!DNL http://localhost:TC::PsPort /is/cache/secondary] に設定する必要があります。

## IS::RemoteUrlDefaultExpiration - リモートImage Sourceのデフォルト TTL {#section-e4c31228b459492cacd2f482d9575f71}

`src={…}` 構文を使用して、リモートソースから HTTP を介して取得したキャッシュ画像の TTL。 リモートサーバーの HTTP 応答に有効期限ヘッダーが含まれていない場合にのみ使用されます。 秒単位の整数値。

## IS::RemoteUrlTimeout - リモート Image Source タイムアウト {#section-437646c479cc4bea81dae42100a3c50a}

Image Server が、リクエストされた画像ファイルを HTTP 経由でリモートサーバーが配信するまでエラーを返さない時間。 秒単位の整数値。

## PS::allowDefaultCatalogRequests - デフォルトのカタログリクエストを有効/無効にする {#section-484e442a115a49b4ac269d1718b351e1}

パスに有効なカタログ ID を含まないリクエストを許可しない場合は、false に設定します。 デフォルトは `true` です。 `false` に設定すると、カタログ ID を持たないリクエストに対してエラーが返されます。

>[!NOTE]
>
>`req=catalogprops` はこの設定の対象ではありません。

## PS::saveToFile.saveTimeout - ファイル保存のタイムアウト {#section-d22afd8ad86144b28684ed95a59db40e}

`timeout=` が指定されていない場合の `req=saveToFile` のデフォルトのタイムアウト値。 `msec`。 指定した時間内に保存操作が完了しない場合は、エラーが返されます。
