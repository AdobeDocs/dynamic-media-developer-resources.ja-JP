---
description: 最終変更の応答ヘッダーを有効にします。 画像サービングから発行されるキャッシュ可能なHTTP応答に最終変更ヘッダーを含める設定を有効または無効にします。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

最終変更の応答ヘッダーを有効にします。 画像サービングから発行されるキャッシュ可能なHTTP応答に最終変更ヘッダーを含める設定を有効または無効にします。

サーバーは、応答に関係するすべてのカタログ/カタログレコードの最新の`catalog::TimeStamp`値を、「最終変更日」ヘッダー値として使用します。

ETAGヘッダーをサポートしていない分散キャッシュネットワークまたはその他のキャッシュシステムを使用する場合にのみ有効にする必要があります。

>[!NOTE]
>
>複数の画像サービングホストが関与する負荷分散環境で最終変更ヘッダーを使用する場合は、注意が必要です。 同じカタログエントリに対して異なるタイムスタンプがサーバーに割り当てられている場合、クライアントのキャッシュが無効になり、サーバーの負荷が増加する可能性があります。 このような状況は、次のように発生する場合があります。
>
>* `catalog::TimeStamp`も`attribute::TimeStamp`もないので、[!DNL catalog.ini]ファイルの変更時刻が`catalog::TimeStamp`のデフォルトとして使用されます。
   >
   >
* ネットワークマウントを介して画像カタログファイルを共有する代わりに、各サーバはローカルファイルシステム上にカタログファイルの独自のインスタンスを持ちます。
>* 同じ[!DNL catalog.ini]ファイルの2つ以上のインスタンスが異なるファイル変更日を持っています。これは、ファイルの不適切なコピーが原因である可能性があります。

>



## プロパティ {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

フラグ。 0は無効、1は最終変更HTTPヘッダーを有効にします。

## 初期設定 {#section-4eb47aadab8b41609bef296a4115f9f4}

`default::UseLastModified`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
