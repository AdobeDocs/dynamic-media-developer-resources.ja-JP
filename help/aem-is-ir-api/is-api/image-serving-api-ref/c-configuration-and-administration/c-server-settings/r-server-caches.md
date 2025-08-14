---
description: サーバーキャッシュには、これらのサーバー設定を使用します。
solution: Experience Manager
title: サーバーキャッシュ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# サーバーキャッシュ{#server-caches}

サーバーキャッシュには、これらのサーバー設定を使用します。

## PS::cache.rootPaths - キャッシュデータフォルダー {#section-f0aa808304d74ecdb0c3644f11906c53}

[!DNL Platform Server] のディスクキャッシュのルートフォルダー。 1 つ以上の絶対ファイルパスまたは *[!DNL install_folder]* に対する相対パス。セミコロン（;）で区切ります。 HTTP 応答キャッシュのデータは、指定されたすべてのフォルダーに均等に配分されます。 補助キャッシュのキャッシュ（コンパイル済みの画像カタログおよび外部画像データ）は、プライマリキャッシュフォルダー（リストの最初のフォルダー）に配置されます。

## PS::cache.maxSize – 応答データのキャッシュ サイズ {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

HTTP 応答キャッシュの最大サイズ （バイト単位）です。 この設定では、キャッシュする実際のデータの量が制限されます。ファイルシステムのオーバーヘッドは考慮されません。 （[ 応答データキャッシュ ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca) を参照）複数のキャッシュデータフォルダーが指定されている場合、キャッシュデータはすべてのフォルダーに均等に配分されます。 `cache.maxSize` 単位の [!DNL PlatformServer.conf] の値はバイト単位です。

## PS::cache.maxEntries – 応答データキャッシュの最大エントリ数 {#section-5603e327e90542a5b50aeeb27b080410}

メモリ内 HTTP 応答キャッシュ インデックスに割り当てられたエントリ数です。

>[!NOTE]
>
>Linux の場合、i ノードが不足しないように、キャッシュパーティションに十分な i ノードが割り当てられていることを確認します。

## IS::TempDirectory - Image Server 一時ファイルフォルダー {#section-42ea1e7a68c444878f7245c5bbcb1672}

Image Server は、場合によっては、中間データをディスクに保存する必要があります。 パスは絶対パスでも、*[!DNL install_folder]* からの相対パスでも構いません。

>[!NOTE]
>
>この設定を変更する前に、新規フォルダーを作成する必要があります。 Image Server がフォルダーを完全に制御できるようにアクセス権限が設定されていることを確認します。

## SV::temp - Server Supervisor 一時ファイル フォルダ {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

サーバースーパーバイザーは、場合によっては、中間データをディスクに保存する必要があります。 パスは絶対パスでも、*[!DNL install_folder]* からの相対パスでも構いません。 デフォルトは [!DNL *[!DNL install_folder]*/temp] です。

>[!NOTE]
>
>この設定を変更する前に、新規フォルダーを作成する必要があります。 サーバースーパーバイザーがフォルダーを完全に制御できるようにアクセス権限が設定されていることを確認します。
