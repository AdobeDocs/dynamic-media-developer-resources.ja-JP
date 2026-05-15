---
description: 最終変更後の応答ヘッダーを有効にします。 画像サービングによって発行されるキャッシュ可能なHTTP応答にLast-Modified ヘッダーを含めることを有効または無効にします。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
TQID: 'https://experienceleague.adobe.com/jmwz9jThBnFtTZBRoI0kbKwoxf1MU7rn1CpKrSU4f04'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

最終変更後の応答ヘッダーを有効にします。 画像サービングによって発行されるキャッシュ可能なHTTP応答にLast-Modified ヘッダーを含めることを有効または無効にします。

サーバーは、応答に含まれるすべてのカタログ/カタログレコードの最新の`catalog::TimeStamp`値を最終変更ヘッダー値として使用します。

etag ヘッダーをサポートしていない分散型キャッシングネットワークまたは他のキャッシングシステムを使用している場合にのみ、有効にする必要があります。

>[!NOTE]
>
>複数のImage Serving ホストを含む負荷分散環境でLast-Modified ヘッダーを使用する場合は、注意が必要です。 同じカタログエントリに対してサーバーに異なるタイムスタンプがある場合、クライアントのキャッシュが失敗し、サーバーの負荷が増加する可能性があります。 このような状況は、次のように発生する可能性があります。
>
>* `catalog::TimeStamp`も`attribute::TimeStamp`も使用しないため、[!DNL catalog.ini] ファイルの変更時間が`catalog::TimeStamp`のデフォルトとして使用されます。
>
>* ネットワークマウントを介して画像カタログファイルを共有する代わりに、各サーバーはローカルファイルシステム上にカタログファイルの独自のインスタンスを持ちます。
>* 同じ[!DNL catalog.ini] ファイルの2つ以上のインスタンスで、ファイルの変更日が異なります。これは、ファイルの不適切なコピーが原因である可能性があります。
>

## プロパティ {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

フラグ： 0を無効にし、1を有効にしてLast-Modified HTTP ヘッダーを有効にします。

## 初期設定 {#section-4eb47aadab8b41609bef296a4115f9f4}

定義されていない場合や空の場合は、`default::UseLastModified`から継承されます。

## 関連項目 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[カタログ：:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
