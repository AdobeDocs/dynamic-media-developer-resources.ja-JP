---
title: UseLastModified
description: 最終変更の応答ヘッダーを有効にします。 画像レンダリングから発行されるキャッシュ可能な HTTP 応答に Last-Modified ヘッダーを含めるかどうかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

最終変更の応答ヘッダーを有効にします。 画像レンダリングから発行されるキャッシュ可能な HTTP 応答に Last-Modified ヘッダーを含めるかどうかを指定します。

サーバーが最新の `vignette::TimeStamp` および `catalog::TimeStamp` 応答に関係するすべてのビネットおよびマテリアルカタログ/カタログレコードの値を、最終変更ヘッダー値として指定します。

etag ヘッダーをサポートしない分散キャッシュネットワーク（Akamai など）が使用されている場合にのみ有効にしてください。

>[!NOTE]
>
>複数の画像サービング/レンダリングホストが関係する負荷分散環境で最終変更ヘッダーを使用する場合は、注意が必要です。 同じカタログエントリに対して異なるタイムスタンプがサーバーに割り当てられている場合、クライアントのキャッシュが無効になり、サーバーの負荷が増加する可能性があります。 このような状況は、次のように発生する場合があります。

* `catalog::TimeStamp`, `vignette::TimeStamp`または `attribute::TimeStamp` が定義されていないので、 [!DNL catalog.ini] ファイルが `catalog::TimeStamp`.

* ネットワークマウントを介してマテリアルカタログファイルを共有する代わりに、各サーバはローカルファイルシステム上のカタログファイルのインスタンスを持ちます。
* 同じ [!DNL catalog.ini] ファイルの変更日が異なります。ファイルが不適切にコピーされたことが原因である可能性があります。

## プロパティ {#section-453952244193452caccfaf7f601007c1}

フラグ。 0 は無効、1 は最終変更 HTTP ヘッダーを有効にします。

## 初期設定 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

継承元 `default::UseLastModified` が定義されていない場合、または空の場合は。

## 関連項目 {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
