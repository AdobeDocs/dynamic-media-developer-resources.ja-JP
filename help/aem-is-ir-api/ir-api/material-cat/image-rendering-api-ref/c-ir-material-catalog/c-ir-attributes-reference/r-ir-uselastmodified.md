---
description: 最終変更の応答ヘッダーを有効にします。 画像レンダリングによって生成されるキャッシュ可能なHTTP応答にLast-Modifiedヘッダーを含めるかどうかを指定します。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

最終変更の応答ヘッダーを有効にします。 画像レンダリングによって生成されるキャッシュ可能なHTTP応答にLast-Modifiedヘッダーを含めるかどうかを指定します。

サーバは、応答に含まれるすべてのビネットおよびマテリアルカタログ/カタログレコードの最新の`vignette::TimeStamp`値と`catalog::TimeStamp`値をLast-Modifiedヘッダー値として使用します。

Akamaiなどの分散キャッシュネットワークを使用し、ETAGヘッダーをサポートしていない場合にのみ有効にする必要があります。

>[!NOTE]
>
>複数の画像サービング/レンダリングホストが関与する負荷分散環境で最終変更ヘッダーを使用する場合は、注意が必要です。 同じカタログエントリに対して異なるタイムスタンプがサーバーに割り当てられている場合、クライアントのキャッシュが無効になり、サーバーの負荷が増加する可能性があります。 このような状況は、次のように発生する場合があります。

* `catalog::TimeStamp`、`vignette::TimeStamp`、`attribute::TimeStamp`は定義されていないので、[!DNL catalog.ini]ファイルの変更時刻が`catalog::TimeStamp`のデフォルトとして使用されます。

* ネットワークマウントを介してマテリアルカタログファイルを共有する代わりに、各サーバはローカルファイルシステム上にカタログファイルの独自のインスタンスを持ちます。
* 同じ[!DNL catalog.ini]ファイルの2つ以上のインスタンスが異なるファイル変更日を持っています。これは、ファイルの不適切なコピーが原因である可能性があります。

## プロパティ {#section-453952244193452caccfaf7f601007c1}

フラグ。 0は無効、1は最終変更HTTPヘッダーを有効にします。

## 初期設定 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

`default::UseLastModified`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
