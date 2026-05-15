---
description: サーバーのキャッシュには、これらのサーバー設定を使用します。
solution: Experience Manager
title: サーバーキャッシュ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
TQID: 'https://experienceleague.adobe.com/UUki7PR7tT4njGw6HktkaobgrM7iwdBZsP-Nbz2TdIY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 0%

---

# サーバーキャッシュ{#server-caches}

サーバーのキャッシュには、これらのサーバー設定を使用します。

## PS::cache.rootPaths - Cache Data Folders {#section-f0aa808304d74ecdb0c3644f11906c53}

[!DNL Platform Server]のディスクキャッシュのルートフォルダー。 1つ以上の絶対ファイルパスまたは&#x200B;*[!DNL install_folder]*&#x200B;からの相対パスを、セミコロン（;）で区切ります。 HTTP応答キャッシュのデータは、指定されたすべてのフォルダーに均等に分散されます。 補助キャッシュ（コンパイルされた画像カタログと外部の画像データ）のキャッシュは、プライマリキャッシュフォルダー（リストの最初のフォルダー）にあります。

## PS::cache.maxSize – 応答データキャッシュサイズ {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

HTTP応答キャッシュの最大サイズ （バイト単位）。 この設定は、実際にキャッシュするデータの量を制限します。ファイルシステムのオーバーヘッドは考慮されません。 （[応答データキャッシュ ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca)を参照）。 複数のキャッシュデータフォルダーを指定した場合、キャッシュデータはすべてのフォルダーに均等に分散されます。 [!DNL PlatformServer.conf]の`cache.maxSize`の値はバイト単位です。

## PS::cache.maxEntries - Response Data Cache Max Entries {#section-5603e327e90542a5b50aeeb27b080410}

メモリ内HTTP応答キャッシュ インデックスに割り当てられたエントリの数。

>[!NOTE]
>
>Linuxでは、i ノードの不足を避けるために、キャッシュパーティションに十分なi ノードが割り当てられていることを確認してください。

## IS::TempDirectory - Image Server Temporary Files Folder {#section-42ea1e7a68c444878f7245c5bbcb1672}

Image Serverは、中間データをディスクに保存する必要がある場合があります。 パスは、絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;からの相対パスにすることができます。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 Image Serverがフォルダーを完全に制御できるように、アクセス権限が設定されていることを確認します。

## SV::temp - Server Supervisor Temporary Files Folder {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

サーバースーパーバイザは、中間データをディスクに保存する必要がある場合があります。 パスは、絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;からの相対パスにすることができます。 デフォルトは[!DNL *[!DNL install_folder]*/temp]です。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 サーバースーパーバイザーがフォルダーを完全に制御できるように、アクセス権限が設定されていることを確認します。
