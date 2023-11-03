---
description: 画像カタログサービス用に、次のサーバ設定を使用します。
solution: Experience Manager
title: 画像カタログサービス
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# 画像カタログサービス{#image-catalog-service}

画像カタログサービス用に、次のサーバ設定を使用します。

## CS::catalog.rootPath — 画像カタログフォルダ {#section-02d107f157384b18835f884f24fea3aa}

画像カタログフォルダの場所 ( ここで、 [!DNL catalog.ini] ファイルを指定する必要があります )。 ファイルの絶対パスまたは *[!DNL install_folder]*. サーバはこのフォルダを継続的に監視し、( [!DNL .ini] ファイルサフィックス ) が検出されたか、既存のメインカタログファイルの最終変更時刻が変更された場合に検出されます。

## CS::catalog.cacheRoot — カタログキャッシュフォルダ {#section-73e499c3a5974f1aa4251e70272ff503}

カタログシステムキャッシュのルートフォルダー。 を `PS::cache.rootPaths`. この設定を変更する前に、フォルダーを手動で作成する必要があります。

## CS::catalog.modificationWaitTime — カタログファイルの解析遅延 {#section-7348065bcc124cb68ea947bf1b9b0845}

カタログサービスが待機する時間（ミリ秒）。 [!DNL catalog.ini] ファイルは、セカンダリカタログファイルが読み込まれるまで変更されます。 この遅延により、すべてのセカンダリカタログファイルが最新の状態に保たれてから、カタログサービスによって読み込みが試行されます。 整数値（ミリ秒）。

## CS::catalog.refreshInterval — カタログファイルのチェック頻度 {#section-517fefc1d8784777a1026abec8630d58}

カタログサービスが画像カタログの変更を確認する頻度。 整数値（ミリ秒）。
