---
description: サーバーキャッシュには、次のサーバー設定を使用します。
seo-description: サーバーキャッシュには、次のサーバー設定を使用します。
seo-title: サーバーキャッシュ
solution: Experience Manager
title: サーバーキャッシュ
topic: Scene7 Image Serving - Image Rendering API
uuid: 73745363-2011-453f-b7a0-96de4b44186d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# サーバーキャッシュ{#server-caches}

サーバーキャッシュには、次のサーバー設定を使用します。

## PS::cache.rootPaths — データフォルダをキャッシュする {#section-f0aa808304d74ecdb0c3644f11906c53}

プラットフォームサーバーのディスクキャッシュのルートフォルダーです。 セミコロン(;)で区切られた、相対的な1つ以上の *[!DNL install_folder]*&#x200B;絶対ファイルパスまたは絶対パス。 HTTP応答キャッシュのデータは、指定したすべてのフォルダーに均等に配分されます。 補助キャッシュ（コンパイルされた画像カタログと外部画像データ）のキャッシュは、プライマリキャッシュフォルダ（リストの最初のフォルダ）に配置されます。

## PS::cache.maxSize — 応答データキャッシュサイズ {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

HTTP応答キャッシュの最大サイズ（バイト単位）。 この設定では、実際にキャッシュされるデータの量が制限されます。ファイルシステムのオーバーヘッドは考慮されません。 (Response Data Cache [を参照](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca))。複数のキャッシュデータフォルダーを指定した場合、キャッシュデータはすべてのフォルダーに均等に分散されます。 inの値はバ `cache.maxSize` イト [!DNL PlatformServer.conf] 単位です。

## PS::cache.maxEntries — 応答データキャッシュの最大エントリ数 {#section-5603e327e90542a5b50aeeb27b080410}

メモリ内HTTP応答キャッシュインデックスに割り当てられたエントリの数。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Linuxでは、iノードの不足を避けるために、キャッシュパーティションに十分なiノードが割り当てられていることを確認します。

## IS::TempDirectory - Image Serverの一時ファイルフォルダ {#section-42ea1e7a68c444878f7245c5bbcb1672}

Image Serverは、中間データをディスクに保存する必要がある場合があります。 パスは、絶対パスまたは相対パスで指定できま *[!DNL install_folder]*&#x200B;す。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>この設定を変更する前に、新しいフォルダを作成する必要があります。 Image Serverがフォルダーのフルコントロールを持つように、アクセス権限が設定されていることを確認します。

## SV::temp — サーバスーパーバイザ一時ファイルフォルダ {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

サーバスーパーバイザは、中間データをディスクに保存する必要がある場合があります。 パスは、絶対パスまたは相対パスで指定できま *[!DNL install_folder]*&#x200B;す。 デフォルトは[!DNL *[!DNL install_folder]*/temp]です。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>この設定を変更する前に、新しいフォルダを作成する必要があります。 サーバスーパーバイザがフォルダのフルコントロールを持つように、アクセス権限が設定されていることを確認します。

