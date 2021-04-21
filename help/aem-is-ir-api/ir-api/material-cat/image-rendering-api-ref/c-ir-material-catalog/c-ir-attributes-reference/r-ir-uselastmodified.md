---
description: 最終変更応答ヘッダーを有効にする。 画像レンダリングから発行されるキャッシュ可能なHTTP応答に、最終変更日のヘッダーを含める設定を有効または無効にします。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---


# UseLastModified{#uselastmodified}

最終変更応答ヘッダーを有効にする。 画像レンダリングから発行されるキャッシュ可能なHTTP応答に、最終変更日のヘッダーを含める設定を有効または無効にします。

サーバは、応答に関係するすべてのビネットおよびマテリアルカタログ/カタログレコードの最新の`vignette::TimeStamp`値と`catalog::TimeStamp`値を、最終変更ヘッダ値として使用します。

etagヘッダーをサポートしない分散キャッシュネットワーク（Akamaiなど）が使用されている場合にのみ有効にする必要があります。

>[!NOTE]
>
>複数の画像サービング/レンダリングホストが関係するロードバランシング環境で、最終変更日のヘッダーを使用する場合は、注意が必要です。 同じカタログエントリに対して異なるタイムスタンプをサーバーが持つ場合、クライアントのキャッシュが無効になり、サーバーの読み込みが増加する可能性があります。 このような状況は、次のように発生します。

* `catalog::TimeStamp`、`vignette::TimeStamp`、`attribute::TimeStamp`のいずれも定義されていないので、[!DNL catalog.ini]ファイルの変更時刻が`catalog::TimeStamp`のデフォルトとして使用されます。

* ネットワークマウントを介してマテリアルカタログファイルを共有する代わりに、各サーバはローカルファイルシステム上のカタログファイルの独自のインスタンスを持ちます。
* 同じ[!DNL catalog.ini]ファイルの2つ以上のインスタンスが異なるファイル変更日を持っています。ファイルの不適切なコピーが原因の可能性があります。

## プロパティ {#section-453952244193452caccfaf7f601007c1}

フラグ。 0を指定すると無効になり、1を指定すると最終変更日時のHTTPヘッダーが有効になります。

## 初期設定 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

定義されていない場合や空の場合は`default::UseLastModified`から継承されます。

## 関連項目 {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
