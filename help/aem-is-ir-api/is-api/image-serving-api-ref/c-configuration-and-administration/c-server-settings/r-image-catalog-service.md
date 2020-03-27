---
description: 画像カタログサービスの次のサーバ設定を使用します。
seo-description: 画像カタログサービスの次のサーバ設定を使用します。
seo-title: 画像カタログサービス
solution: Experience Manager
title: 画像カタログサービス
topic: Scene7 Image Serving - Image Rendering API
uuid: 601b1c30-7d51-448b-97b5-5ad9cb383975
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 画像カタログサービス{#image-catalog-service}

画像カタログサービスの次のサーバ設定を使用します。

## CS::catalog.rootPath — 画像カタログフォルダ {#section-02d107f157384b18835f884f24fea3aa}

画像カタログフォルダの場所(すべてのファ [!DNL catalog.ini] イルが存在する場所)。 ファイルの絶対パスまたはを基準とした相対パスを指定できま *[!DNL install_folder]*&#x200B;す。 サーバは、このフォルダを継続的に監視し、新しいメインカタログファイル（ファイルのサフィックスが付く）が検出された場合、または既存のメインカタログファイルの最終変更時刻が変更された場合に、カタログを読み込みまたは再読み込みします。 [!DNL .ini]

## CS::catalog.cacheRoot — カタログキャッシュフォルダ {#section-73e499c3a5974f1aa4251e70272ff503}

カタログシステムのキャッシュのルートフォルダー。 のフォルダの1つと同じに設定できます `PS::cache.rootPaths`。 この設定を変更する前に、フォルダーを手動で作成する必要があります。

## CS::catalog.modificationWaitTime — カタログファイルの解析遅延 {#section-7348065bcc124cb68ea947bf1b9b0845}

ファイルが変更されてからセカンダリカタログファイルが読み込ま [!DNL catalog.ini] れるまで、カタログサービスが待機する時間（ミリ秒）。 この遅延により、カタログサービスが読み込みを試行する前に、すべてのセカンダリカタログファイルが最新の状態に保たれます。 整数値（ミリ秒）。

## CS::catalog.refreshInterval — カタログファイルのチェックの頻度 {#section-517fefc1d8784777a1026abec8630d58}

カタログサービスが画像カタログの変更を確認する頻度。 整数値（ミリ秒）。
