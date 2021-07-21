---
description: 画像カタログサービスの次のサーバ設定を使用します。
solution: Experience Manager
title: 画像カタログサービス
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# 画像カタログサービス{#image-catalog-service}

画像カタログサービスの次のサーバ設定を使用します。

## CS::catalog.rootPath — 画像カタログフォルダ {#section-02d107f157384b18835f884f24fea3aa}

画像カタログフォルダーの場所（すべての[!DNL catalog.ini]ファイルが配置されている必要があります）。 ファイルの絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;に対する相対パスを指定できます。 サーバーはこのフォルダーを継続的に監視し、新しいメインカタログファイル（[!DNL .ini]ファイルサフィックスを持つ）が検出された場合、または既存のメインカタログファイルの最終変更時刻が変更された場合に、カタログを読み込みまたは再読み込みします。

## CS::catalog.cacheRoot — カタログキャッシュフォルダ {#section-73e499c3a5974f1aa4251e70272ff503}

カタログシステムのキャッシュのルートフォルダー。 `PS::cache.rootPaths`内のフォルダーの1つと同じに設定できます。 この設定を変更する前に、フォルダーを手動で作成する必要があります。

## CS::catalog.modificationWaitTime — カタログファイルの解析遅延 {#section-7348065bcc124cb68ea947bf1b9b0845}

[!DNL catalog.ini]ファイルが変更されてから、セカンダリカタログファイルが読み込まれるまで、カタログサービスが待機する時間（ミリ秒）。 この遅延により、カタログサービスが読み込みを試みる前に、すべてのセカンダリカタログファイルが最新の状態に保たれます。 整数値（ミリ秒）。

## CS::catalog.refreshInterval — カタログファイルのチェック頻度 {#section-517fefc1d8784777a1026abec8630d58}

カタログサービスが画像カタログの変更を確認する頻度。 整数値（ミリ秒）。
