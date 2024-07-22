---
title: UseLastModified
description: 最終変更日の応答ヘッダーを有効にします。 画像レンダリングによって生成されるキャッシュ可能な HTTP 応答に Last-Modified ヘッダーを含めるかどうかを有効または無効にします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

最終変更日の応答ヘッダーを有効にします。 画像レンダリングによって生成されるキャッシュ可能な HTTP 応答に Last-Modified ヘッダーを含めるかどうかを有効または無効にします。

サーバーは、応答に関係するすべてのビネットおよび材料カタログ/カタログレコードの最新の `vignette::TimeStamp` と `catalog::TimeStamp` 値を Last-Modified ヘッダー値として使用します。

etag ヘッダーをサポートしない、Akamai などの分散キャッシュネットワークを使用する場合にのみ有効にしてください。

>[!NOTE]
>
>複数の画像サービング/レンダリングホストを含む負荷分散された環境で Last-Modified ヘッダーを使用する場合は、注意が必要です。 何らかの理由でサーバーのタイムスタンプが同じカタログエントリごとに異なる場合、クライアントキャッシュが無効になり、サーバー負荷が増加する可能性があります。 このような状況は、次のように発生する場合があります。

* `catalog::TimeStamp`、`vignette::TimeStamp`、または `attribute::TimeStamp` が定義されていないので、[!DNL catalog.ini] ファイルの変更時間が `catalog::TimeStamp` の既定として使用されます。

* ネットワーク マウントを使用してマテリアル カタログ ファイルを共有する代わりに、各サーバはローカル ファイル システム上にカタログ ファイルの独自のインスタンスを持ちます。
* 同じ [!DNL catalog.ini] ファイルの 2 つ以上のインスタンスのファイル変更日が異なります。ファイルのコピーが正しく行われていないことが原因の可能性があります。

## プロパティ {#section-453952244193452caccfaf7f601007c1}

フラグ。 0 を指定すると無効になり、1 を指定すると Last-Modified HTTP ヘッダーが有効になります。

## 初期設定 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

定義されていない場合または空の場合は `default::UseLastModified` から継承します。

## 関連項目 {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
