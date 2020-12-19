---
description: 画像カタログサービスでは、以下のサーバ設定を使用します。
seo-description: 画像カタログサービスでは、以下のサーバ設定を使用します。
seo-title: 画像カタログサービス
solution: Experience Manager
title: 画像カタログサービス
topic: Scene7 Image Serving - Image Rendering API
uuid: 601b1c30-7d51-448b-97b5-5ad9cb383975
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# 画像カタログサービス{#image-catalog-service}

画像カタログサービスでは、以下のサーバ設定を使用します。

## CS::catalog.rootPath — 画像カタログフォルダ{#section-02d107f157384b18835f884f24fea3aa}

画像カタログフォルダーの場所（すべての[!DNL catalog.ini]ファイルを置く必要がある場所）。 ファイルの絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;を基準とした相対パスを指定できます。 サーバはこのフォルダを継続的に監視し、新しいメインカタログファイル（ファイル名が[!DNL .ini]である）が検出された場合、または既存のメインカタログファイルの最終変更時刻が変更された場合に、カタログを読み込むか再読み込みします。

## CS::catalog.cacheRoot — カタログキャッシュフォルダ{#section-73e499c3a5974f1aa4251e70272ff503}

カタログシステムのキャッシュのルートフォルダーです。 `PS::cache.rootPaths`内のフォルダーと同じに設定できます。 この設定を変更する前に、フォルダーを手動で作成する必要があります。

## CS::catalog.modificationWaitTime — カタログファイルの解析遅延{#section-7348065bcc124cb68ea947bf1b9b0845}

[!DNL catalog.ini]ファイルが変更されてからセカンダリカタログファイルが読み込まれるまで、カタログサービスが待機する時間（ミリ秒）です。 この遅延により、すべてのセカンダリカタログファイルを最新の状態にしてから、カタログサービスで読み込みを試みることができます。 整数値（ミリ秒）

## CS::catalog.refreshInterval — カタログファイルのチェック頻度{#section-517fefc1d8784777a1026abec8630d58}

カタログサービスが画像カタログの変更を確認する頻度。 整数値（ミリ秒）
