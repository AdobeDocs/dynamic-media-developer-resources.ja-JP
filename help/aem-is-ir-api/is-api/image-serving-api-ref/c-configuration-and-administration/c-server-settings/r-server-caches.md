---
description: サーバーキャッシュには、次のサーバー設定を使用します。
seo-description: サーバーキャッシュには、次のサーバー設定を使用します。
seo-title: サーバーキャッシュ
solution: Experience Manager
title: サーバーキャッシュ
topic: Scene7 Image Serving - Image Rendering API
uuid: 73745363-2011-453f-b7a0-96de4b44186d
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# サーバーキャッシュ{#server-caches}

サーバーキャッシュには、次のサーバー設定を使用します。

## PS::cache.rootPaths — キャッシュデータフォルダ{#section-f0aa808304d74ecdb0c3644f11906c53}

プラットフォームサーバーのディスクキャッシュのルートフォルダーです。 セミコロン(;)で区切られた、*[!DNL install_folder]*&#x200B;を基準とする1つ以上の絶対ファイルパスまたはパス。 HTTP応答キャッシュのデータは、指定されたすべてのフォルダーに均等に配分されます。 補助キャッシュ(コンパイルされた画像カタログと外部リストデータ)のキャッシュは、プライマリキャッシュフォルダ（フォルダ内の最初のフォルダ）にあります。

## PS::cache.maxSize — 応答データキャッシュサイズ{#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

HTTP応答キャッシュの最大サイズ（バイト単位）です。 この設定は、キャッシュする実際のデータ量を制限します。ファイルシステムのオーバーヘッドは考慮されません。 （[応答データキャッシュ](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca)を参照）。 複数のキャッシュデータフォルダーを指定した場合、キャッシュデータはすべてのフォルダーに均等に分散されます。 [!DNL PlatformServer.conf]の`cache.maxSize`の値はバイト単位です。

## PS::cache.maxEntries — 応答データキャッシュの最大エントリ数{#section-5603e327e90542a5b50aeeb27b080410}

メモリ内HTTP応答キャッシュインデックスに割り当てられたエントリ数。

>[!NOTE]
>
>Linuxでは、iノードの不足を回避するために、キャッシュパーティションに十分なiノードが割り当てられていることを確認します。

## IS::TempDirectory - Image Server一時ファイルフォルダ{#section-42ea1e7a68c444878f7245c5bbcb1672}

Image Serverは、中間データをディスクに保存する必要がある場合があります。 パスは、絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;を基準とした相対パスにすることができます。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 Image Serverがフォルダーのフルコントロールを持つように、アクセス権限が設定されていることを確認します。

## SV::temp — サーバースーパーバイザ一時ファイルフォルダ{#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

サーバスーパーバイザは、中間データをディスクに保存する必要がある場合があります。 パスは、絶対パスまたは&#x200B;*[!DNL install_folder]*&#x200B;を基準とした相対パスにすることができます。 初期設定は[!DNL *[!DNL install_folder]*/temp]です。

>[!NOTE]
>
>この設定を変更する前に、新しいフォルダーを作成する必要があります。 サーバスーパーバイザがフォルダのフルコントロールを持つように、アクセス権限が設定されていることを確認します。

