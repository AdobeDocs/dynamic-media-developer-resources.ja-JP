---
description: 最終変更の応答ヘッダーを有効にします。 画像サービングから発行されるキャッシュ可能なHTTP応答に、最終変更日時のヘッダを含めるかどうかを指定します。
seo-description: 最終変更の応答ヘッダーを有効にします。 画像サービングから発行されるキャッシュ可能なHTTP応答に、最終変更日時のヘッダを含めるかどうかを指定します。
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

最終変更の応答ヘッダーを有効にします。 画像サービングから発行されるキャッシュ可能なHTTP応答に、最終変更日時のヘッダを含めるかどうかを指定します。

サーバーは、応答に含まれるす `catalog::TimeStamp` べてのカタログ/カタログレコードの最新の値を、最終変更時のヘッダー値として使用します。

etagヘッダーをサポートしていない分散キャッシュネットワークまたは他のキャッシュシステムを使用する場合にのみ有効にする必要があります。

>[!NOTE]
>
>複数の画像サービングホストが関与する負荷分散環境で、最終変更日時のヘッダーを使用する場合は、注意が必要です。 同じカタログエントリに対して異なるタイムスタンプを持つサーバーでは、クライアントのキャッシュが無効になり、サーバーの読み込みが増加する場合があります。 このような状況は、次のように発生します。
>
>* または `catalog::TimeStamp` どちらも `attribute::TimeStamp`ないので、ファイルの変更時刻が [!DNL catalog.ini] のデフォルトとして使用されます `catalog::TimeStamp`。
   >
   >
* ネットワークマウントを介して画像カタログファイルを共有する代わりに、各サーバは、ローカルファイルシステム上のカタログファイルの独自のインスタンスを持ちます。
>* 同じファイルの複数のインスタンスが異な [!DNL catalog.ini] るファイル変更日を持つ。ファイルの不適切なコピーが原因である可能性があります。
>



## プロパティ {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

フラグ。 0を指定すると無効になり、1を指定すると最終変更HTTPヘッダーが有効になります。

## 初期設定 {#section-4eb47aadab8b41609bef296a4115f9f4}

定義されていな `default::UseLastModified` い場合や空の場合に継承されます。

## 関連項目 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
