---
description: 最終変更応答ヘッダーを有効にする。 画像サービングから発行されるキャッシュ可能なHTTP応答に、最終変更日のヘッダを含める設定を有効または無効にします。
seo-description: 最終変更応答ヘッダーを有効にする。 画像サービングから発行されるキャッシュ可能なHTTP応答に、最終変更日のヘッダを含める設定を有効または無効にします。
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# UseLastModified{#uselastmodified}

最終変更応答ヘッダーを有効にする。 画像サービングから発行されるキャッシュ可能なHTTP応答に、最終変更日のヘッダを含める設定を有効または無効にします。

サーバーは、応答に関係するすべてのカタログ/カタログレコードの最新の`catalog::TimeStamp`値を、「最終変更日」のヘッダー値として使用します。

etagヘッダーをサポートしない分散キャッシュネットワークまたは他のキャッシュシステムを使用する場合にのみ有効にする必要があります。

>[!NOTE]
>
>複数の画像サービングホストが関与するロードバランシング環境で、最終変更日時のヘッダーを使用する場合は、注意が必要です。 同じカタログエントリに対して異なるタイムスタンプをサーバーが持つ場合、クライアントのキャッシュが無効になり、サーバーの読み込みが増加する可能性があります。 このような状況は、次のように発生します。
>
>* `catalog::TimeStamp`と`attribute::TimeStamp`のどちらもないので、[!DNL catalog.ini]ファイルの変更時刻が`catalog::TimeStamp`のデフォルトとして使用されます。
   >
   >
* ネットワークマウントを介して画像カタログファイルを共有する代わりに、各サーバはローカルファイルシステム上に独自のカタログファイルのインスタンスを持ちます。
>* 同じ[!DNL catalog.ini]ファイルの2つ以上のインスタンスが異なるファイル変更日を持っています。ファイルの不適切なコピーが原因の可能性があります。

>



## プロパティ {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

フラグ。 0を指定すると無効になり、1を指定すると最終変更日時のHTTPヘッダーが有効になります。

## 初期設定 {#section-4eb47aadab8b41609bef296a4115f9f4}

定義されていない場合や空の場合は`default::UseLastModified`から継承されます。

## 関連項目 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
