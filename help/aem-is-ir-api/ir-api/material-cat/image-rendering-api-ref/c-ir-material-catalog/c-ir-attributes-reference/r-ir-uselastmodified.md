---
title: UseLastModified
description: 最終変更後の応答ヘッダーを有効にします。 画像レンダリングで生成されるキャッシュ可能なHTTP応答にLast-Modified ヘッダーを含めることを有効または無効にします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
TQID: 'https://experienceleague.adobe.com/X-d-02WckbxVyDxRvZDIcOghkk8Z8yYbGOZ3Aigx4ts'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

最終変更後の応答ヘッダーを有効にします。 画像レンダリングで生成されるキャッシュ可能なHTTP応答にLast-Modified ヘッダーを含めることを有効または無効にします。

サーバーは、応答に含まれるすべての周辺光量補正およびマテリアルカタログ/カタログレコードの最新の`vignette::TimeStamp`および`catalog::TimeStamp`値を最終変更ヘッダー値として使用します。

etag ヘッダーをサポートしない分散型キャッシングネットワーク（Akamaiなど）が使用されている場合にのみ、有効にする必要があります。

>[!NOTE]
>
>複数の画像サービング/レンダリングホストを含む負荷分散環境でLast-Modified ヘッダーを使用する場合は、注意が必要です。 同じカタログエントリに対してサーバーに異なるタイムスタンプがある場合、クライアントのキャッシュが失敗し、サーバーの負荷が増加する可能性があります。 このような状況は、次のように発生する可能性があります。

* `catalog::TimeStamp`、`vignette::TimeStamp`、または`attribute::TimeStamp`が定義されていないため、[!DNL catalog.ini] ファイルの変更時間が`catalog::TimeStamp`のデフォルトとして使用されます。

* ネットワーク・マウントを介してマテリアル・カタログ・ファイルを共有する代わりに、各サーバはローカル・ファイル・システム上にカタログ・ファイルの独自のインスタンスを持ちます。
* 同じ[!DNL catalog.ini] ファイルの2つ以上のインスタンスで、ファイルの変更日が異なります。これは、ファイルの不適切なコピーが原因である可能性があります。

## プロパティ {#section-453952244193452caccfaf7f601007c1}

フラグ： 0を無効にし、1を有効にしてLast-Modified HTTP ヘッダーを有効にします。

## 初期設定 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

定義されていない場合や空の場合は、`default::UseLastModified`から継承されます。

## 関連項目 {#section-1536715169da48b0aecc4ab7326c86db}

[ カタログ：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)、[ ビネット：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)

