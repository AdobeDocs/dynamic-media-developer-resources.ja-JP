---
description: サーバーキャッシュに対して、これらのサーバー設定を使用します。
solution: Experience Manager
title: サーバーキャッシュ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# サーバーキャッシュ{#server-caches}

サーバーキャッシュに対して、これらのサーバー設定を使用します。

## PS::cache.rootPaths — データフォルダをキャッシュする {#section-f0aa808304d74ecdb0c3644f11906c53}

Platform Serverのディスクキャッシュのルートフォルダー。 *[!DNL install_folder]*&#x200B;に対する絶対ファイルパスまたは相対パス(セミコロン(;)区切り)。 HTTP応答キャッシュのデータは、指定されたすべてのフォルダーに均等に配分されます。 補助キャッシュ（コンパイルされた画像カタログと外部画像データ）のキャッシュは、プライマリキャッシュフォルダ（リストの最初のフォルダ）に配置されます。

## PS::cache.maxSize — 応答データのキャッシュサイズ {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

HTTP応答キャッシュの最大サイズ（バイト単位）。 この設定は、キャッシュする実際のデータの量を制限します。ファイル・システムのオーバーヘッドは考慮されません。 （[応答データキャッシュ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca)を参照）。 複数のキャッシュデータフォルダーを指定した場合、キャッシュデータはすべてのフォルダーに均等に分散されます。 [!DNL PlatformServer.conf]の`cache.maxSize`の値はバイト単位です。

## PS::cache.maxEntries — 応答データキャッシュの最大エントリ数 {#section-5603e327e90542a5b50aeeb27b080410}

メモリ内HTTP応答キャッシュインデックスに割り当てられたエントリの数。

>[!NOTE]
>
>Linuxでは、iノードが不足しないように、十分なiノードがキャッシュパーティションに割り当てられていることを確認します。

## IS::TempDirectory - Image Server一時ファイルフォルダ {#section-42ea1e7a68c444878f7245c5bbcb1672}

Image Serverは、中間データをディスクに保存する必要が生じる場合があります。 パスは、絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;に対する相対パスで指定できます。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 Image Serverがフォルダーを完全に制御できるように、アクセス権限が設定されていることを確認します。

## SV::temp — サーバスーパーバイザ一時ファイルフォルダ {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

サーバスーパーバイザは、中間データをディスクに保存する必要が生じる場合があります。 パスは、絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;に対する相対パスで指定できます。 デフォルトは[!DNL *[!DNL install_folder]*/temp]です。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 サーバスーパーバイザがフォルダを完全に制御できるように、アクセス権限が設定されていることを確認します。
