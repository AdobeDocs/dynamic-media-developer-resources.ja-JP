---
description: これらのサーバー設定を Image catalog サービスに使用します。
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

これらのサーバー設定を Image catalog サービスに使用します。

## CS::catalog.rootPath – 画像カタログフォルダー {#section-02d107f157384b18835f884f24fea3aa}

画像カタログフォルダーの場所（すべての [!DNL catalog.ini] ファイルが存在する必要がある場所）。 絶対ファイルパスまたは *[!DNL install_folder]* に対する相対パスを指定できます。 サーバは、このフォルダを継続的に監視し、ファイル サフィックスの付いた新しいメイン カタログ ファイルが検出された場合、または既存のメイン カタログ ファイルの最終変更時刻が変更された場合に [!DNL .ini] カタログのロードや再ロードを行います。

## CS::catalog.cacheRoot - カタログのキャッシュフォルダー {#section-73e499c3a5974f1aa4251e70272ff503}

カタログシステムキャッシュのルートフォルダー。 `PS::cache.rootPaths` のいずれかのフォルダーと同じ設定にすることができます。 この設定を変更するには、フォルダーを手動で作成する必要があります。

## CS::catalog.modificationWaitTime - カタログ ファイルの解析遅延 {#section-7348065bcc124cb68ea947bf1b9b0845}

[!DNL catalog.ini] ファイルが変更されてから、カタログ サービスがセカンダリ カタログ ファイルを読み込むまでの待ち時間（ミリ秒）。 この遅延は、カタログサービスがファイルの読み込みを試みる前にすべてのセカンダリカタログファイルが最新の状態になっていることを確認するのに役立ちます。 ミリ秒単位の整数値。

## CS::catalog.refreshInterval - カタログ ファイルのチェック頻度 {#section-517fefc1d8784777a1026abec8630d58}

画像カタログへの変更をカタログサービスが確認する頻度。 ミリ秒単位の整数値。
