---
description: 一般的なサーバー設定
solution: Experience Manager
title: 一般
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# 一般{#general}

一般的なサーバー設定

## TC::PsPort — メインリスニングポート {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Platform Serverのメインリスニングポートを指定します。 また、このポートは、画像サービング、画像レンダリング、Dynamic Mediaビューア（インストールされている場合）のドキュメントおよび例のページにアクセスするためにも使用されます。

## IS::CacheServerUrl — サービスのルートURLのキャッシュ {#section-bcca227a1f91453b834db4ea050968e2}

Image ServerがキャッシュサービスにアクセスできるようにするHTTPルートパスを指定します。 [!DNL http://localhost:TC::PsPort /is/cache/secondary]に設定し、ポート番号を`TC::PsPort`に一致させる必要があります。

## IS::RemoteUrlDefaultExpiration — リモートImage SourceのデフォルトTTL {#section-e4c31228b459492cacd2f482d9575f71}

`src={…}`構文を使用してリモートソースからHTTP経由で取得したキャッシュイメージのTTL。 リモートサーバーのHTTP応答にExpirationヘッダーが含まれていない場合にのみ使用されます。 秒単位の整数値。

## IS::RemoteUrlTimeout — リモートImage Sourceタイムアウト {#section-437646c479cc4bea81dae42100a3c50a}

リモートサーバーが要求されたイメージファイルをHTTP経由で配信するのを待ってから、エラーが返されるまでの時間。 秒単位の整数値。

## PS::allowDefaultCatalogRequests — デフォルトのカタログ要求を有効化/無効化 {#section-484e442a115a49b4ac269d1718b351e1}

パスに有効なカタログIDを含まない要求を許可しない場合は、falseに設定します。 初期設定は `true`. `false`に設定すると、カタログIDのないリクエストに対してエラーが返されます。

>[!NOTE]
>
>`req=catalogprops` はこの設定の対象ではありません。

## PS::saveToFile.saveTimeout — ファイル保存タイムアウト {#section-d22afd8ad86144b28684ed95a59db40e}

`timeout=`が指定されていない場合の`req=saveToFile`のデフォルトのタイムアウト値。 `msec`. 指定された時間内に保存操作が完了しない場合は、エラーが返されます。
