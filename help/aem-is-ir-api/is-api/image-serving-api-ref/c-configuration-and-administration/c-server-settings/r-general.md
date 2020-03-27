---
description: 一般的なサーバー設定
seo-description: 一般的なサーバー設定
seo-title: 一般
solution: Experience Manager
title: 一般
topic: Scene7 Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 一般{#general}

一般的なサーバー設定

## TC::PsPort — メインリスニングポート {#section-d31d3051aa994a76b60b70c3d9f7e89f}

プラットフォームサーバーのメインリスニングポートを指定します。 このポートは、画像サービング、画像レンダリングおよびScene7ビューア（インストールされている場合）のドキュメントおよびサンプルページにアクセスするためにも使用されます。

## IS::CacheServerUrl — キャッシュサービスのルートURL {#section-bcca227a1f91453b834db4ea050968e2}

Image ServerがキャッシュサービスにアクセスできるようにするHTTPルートパスを指定します。 に設定し、ポート番 [!DNL http://localhost:TC::PsPort /is/cache/secondary]号が一致する必要がありま `TC::PsPort`す。

## IS::RemoteUrlDefaultExpiration — リモートイメージソースのデフォルトTTL {#section-e4c31228b459492cacd2f482d9575f71}

構成体を使用してリモートソースからHTTP経由で取得したキャッシュイメージのTTL `src={…}` です。 リモートサーバーのHTTP応答に有効期限ヘッダーが含まれていない場合にのみ使用されます。 秒単位の整数値。

## IS::RemoteUrlTimeout — リモートイメージソースのタイムアウト {#section-437646c479cc4bea81dae42100a3c50a}

Image Serverが要求されたイメージファイルをHTTP経由で配信するのをリモートサーバーが待機してからエラーを返すまでの時間。 秒単位の整数値。

## PS::allowDefaultCatalogRequests — 初期設定のカタログ要求を有効化/無効化 {#section-484e442a115a49b4ac269d1718b351e1}

パスに有効なカタログIDを含まない要求を許可しない場合は、falseに設定します。 初期設定は `true`. に設定すると、カ `false`タログIDを持たないリクエストに対してエラーが返されます。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>`req=catalogprops` がこの設定の対象ではありません。

## PS::saveToFile.saveTimeout — ファイルの保存タイムアウト {#section-d22afd8ad86144b28684ed95a59db40e}

指定しなかった場合のデフォ `req=saveToFile` ルトの `timeout=`タイムアウト値です。 `msec`. 指定した時間内に保存操作が完了しなかった場合は、エラーが返されます。
