---
description: 最終変更日の応答ヘッダーを有効にします。 画像サービングによって生成されるキャッシュ可能な HTTP 応答に Last-Modified ヘッダーを含めるかどうかを有効または無効にします。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

最終変更日の応答ヘッダーを有効にします。 画像サービングによって生成されるキャッシュ可能な HTTP 応答に Last-Modified ヘッダーを含めるかどうかを有効または無効にします。

サーバーは、応答に関係するすべてのカタログまたはカタログレコードの最新の `catalog::TimeStamp` 値を Last-Modified ヘッダー値として使用します。

は、etag ヘッダーをサポートしない分散キャッシュネットワークまたはその他のキャッシュシステムを使用する場合にのみ有効にしてください。

>[!NOTE]
>
>複数の画像サービングホストを含む負荷分散された環境で Last-Modified ヘッダーを使用する場合は、注意が必要です。 何らかの理由でサーバーのタイムスタンプが同じカタログエントリごとに異なる場合、クライアントキャッシュが無効になり、サーバー負荷が増加する可能性があります。 このような状況は、次のように発生する場合があります。
>
>* `catalog::TimeStamp` も `attribute::TimeStamp` も指定されていないため、[!DNL catalog.ini] ファイルの変更時間が `catalog::TimeStamp` のデフォルトとして使用されます。
>
>* ネットワーク・マウントを使用してイメージ・カタログ・ファイルを共有する代わりに、各サーバはローカル・ファイル・システム上にカタログ・ファイルの独自のインスタンスを持ちます。
>* 同じ [!DNL catalog.ini] ファイルの 2 つ以上のインスタンスのファイル変更日が異なります。ファイルのコピーが正しく行われていないことが原因の可能性があります。
>

## プロパティ {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

フラグ。 0 を指定すると無効になり、1 を指定すると Last-Modified HTTP ヘッダーが有効になります。

## 初期設定 {#section-4eb47aadab8b41609bef296a4115f9f4}

定義されていない場合または空の場合は `default::UseLastModified` から継承します。

## 関連項目 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[カタログ：：タイムスタンプ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
