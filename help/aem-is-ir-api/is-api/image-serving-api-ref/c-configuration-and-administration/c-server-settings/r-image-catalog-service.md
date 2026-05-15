---
description: これらのサーバー設定を画像カタログサービスに使用します。
solution: Experience Manager
title: 画像カタログサービス
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
TQID: 'https://experienceleague.adobe.com/Fs2xGD3Dpd8pe5jtto4kPMF0BrJiLNRvdBn8RSPiQjw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 0%

---

# 画像カタログサービス{#image-catalog-service}

これらのサーバー設定を画像カタログサービスに使用します。

## CS::catalog.rootPath - イメージ カタログ フォルダー {#section-02d107f157384b18835f884f24fea3aa}

画像カタログ フォルダーの場所（すべての[!DNL catalog.ini] ファイルを配置する必要があります）。 *[!DNL install_folder]*&#x200B;に対する絶対ファイルパスまたは相対パスを指定できます。 サーバーは、このフォルダーを継続的に監視し、新しいメインカタログファイル（[!DNL .ini]個のファイル接尾辞を含む）が検出されたときや、既存のメインカタログファイルの最終更新時間が変更されたときに、カタログを読み込んだり再読み込みしたりします。

## CS::catalog.cacheRoot - カタログキャッシュフォルダー {#section-73e499c3a5974f1aa4251e70272ff503}

カタログシステムキャッシュのルートフォルダー。 `PS::cache.rootPaths`のいずれかのフォルダーと同じに設定できます。 この設定を変更する前に、フォルダーを手動で作成する必要があります。

## CS::catalog.modificationWaitTime - カタログファイルの解析遅延 {#section-7348065bcc124cb68ea947bf1b9b0845}

[!DNL catalog.ini] ファイルが変更された後、セカンダリカタログファイルが読み込まれるまで、カタログサービスが待機する時間（ミリ秒単位）。 この遅延は、カタログサービスが読み込みを試行する前に、すべてのセカンダリカタログファイルが最新であることを確認するのに役立ちます。 整数値（ミリ秒単位）。

## CS::catalog.refreshInterval - カタログファイルのチェック頻度 {#section-517fefc1d8784777a1026abec8630d58}

カタログサービスが画像カタログの変更をチェックする頻度。 整数値（ミリ秒単位）。
