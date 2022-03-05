---
description: サーバーキャッシュに対して、これらのサーバー設定を使用します。
solution: Experience Manager
title: サーバーキャッシュ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# サーバーキャッシュ{#server-caches}

サーバーキャッシュに対して、これらのサーバー設定を使用します。

## PS::cache.rootPaths — データフォルダをキャッシュする {#section-f0aa808304d74ecdb0c3644f11906c53}

Platform Server のディスクキャッシュのルートフォルダーです。 ファイルの絶対パスまたはファイルの絶対パス ( *[!DNL install_folder]*( セミコロン (;) で区切られます )。 HTTP 応答キャッシュのデータは、指定されたすべてのフォルダーに均等に配分されます。 補助キャッシュ（コンパイル済みの画像カタログと外部の画像データ）のキャッシュは、プライマリキャッシュフォルダ（リスト内の最初のフォルダ）に配置されます。

## PS::cache.maxSize — 応答データのキャッシュサイズ {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

HTTP 応答キャッシュの最大サイズ（バイト単位）です。 この設定により、キャッシュする実際のデータの量が制限されます。ファイル・システムのオーバーヘッドは考慮されません。 ( [応答データキャッシュ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) 複数のキャッシュデータフォルダーを指定した場合、キャッシュデータはすべてのフォルダーに均等に分散されます。 の値 `cache.maxSize` in [!DNL PlatformServer.conf] はバイト単位です。

## PS::cache.maxEntries — 応答データキャッシュの最大エントリ数 {#section-5603e327e90542a5b50aeeb27b080410}

インメモリ HTTP 応答キャッシュインデックスに割り当てられたエントリの数。

>[!NOTE]
>
>Linux では、i ノードが不足するのを避けるために、十分な i ノードがキャッシュパーティションに割り当てられていることを確認します。

## IS::TempDirectory - Image Server 一時ファイルフォルダ {#section-42ea1e7a68c444878f7245c5bbcb1672}

Image Server は、中間データをディスクに保存する必要が生じる場合があります。 パスは、絶対パスまたは相対パスにすることができます *[!DNL install_folder]*.

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダを作成する必要があります。 Image Server がフォルダーを完全に制御できるように、アクセス権限が設定されていることを確認します。

## SV::temp - Server Supervisor Temporary Files Folder {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

サーバスーパーバイザは、中間データをディスクに保存する必要が生じる場合があります。 パスは、絶対パスまたは相対パスにすることができます *[!DNL install_folder]*. デフォルトは [!DNL  *[!DNL install_folder]*/temp] と入力します。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダを作成する必要があります。 サーバスーパーバイザがフォルダを完全に制御できるように、アクセス権限が設定されていることを確認します。
