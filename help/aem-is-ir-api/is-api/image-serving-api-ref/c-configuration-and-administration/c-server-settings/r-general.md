---
description: 一般的なサーバー設定
seo-description: 一般的なサーバー設定
seo-title: 一般
solution: Experience Manager
title: 一般
topic: Scene7 Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 2%

---


# 一般{#general}

一般的なサーバー設定

## TC::PsPort — メインリスニングポート {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Platformサーバーのメインリスニングポートを指定します。 このポートは、画像サービング、画像レンダリング、Scene7ビューア（インストールされている場合）のドキュメントおよびサンプルページにアクセスするためにも使用されます。

## IS::CacheServerUrl — キャッシュサービスのルートURL {#section-bcca227a1f91453b834db4ea050968e2}

Image ServerがキャッシュサービスにアクセスできるようにするHTTPルートパスを指定します。 ポート番号が一致す [!DNL http://localhost:TC::PsPort /is/cache/secondary]るようにに設定する必要があり `TC::PsPort`ます。

## IS::RemoteUrlDefaultExpiration — リモートイメージソースのデフォルトTTL {#section-e4c31228b459492cacd2f482d9575f71}

構成体を使用してリモートソースからHTTP経由で取得したキャッシュ済みイメージのTTLで `src={…}` す。 リモートサーバーのHTTP応答に有効期限ヘッダーが含まれていない場合にのみ使用されます。 秒単位の整数値。

## IS::RemoteUrlTimeout — リモートイメージソースのタイムアウト {#section-437646c479cc4bea81dae42100a3c50a}

Image Serverが、要求されたイメージファイルをHTTP経由でリモートサーバから配信するのを待ってから、エラーが返されるまでの時間です。 秒単位の整数値。

## PS::allowDefaultCatalogRequests — 初期設定のカタログ要求を有効化/無効化 {#section-484e442a115a49b4ac269d1718b351e1}

パスに有効なカタログIDを含まない要求を許可しない場合は、falseに設定します。 初期設定は `true`. に設定すると `false`、カタログIDのない要求に対してエラーが返されます。

>[!NOTE]
>
>`req=catalogprops` は、この設定の対象ではありません。

## PS::saveToFile.saveTimeout — ファイル保存のタイムアウト {#section-d22afd8ad86144b28684ed95a59db40e}

指定しなかった場合 `req=saveToFile` のデフォルト `timeout=`のタイムアウト値。 `msec`. 指定した時間内に保存操作が完了しない場合は、エラーが返されます。
