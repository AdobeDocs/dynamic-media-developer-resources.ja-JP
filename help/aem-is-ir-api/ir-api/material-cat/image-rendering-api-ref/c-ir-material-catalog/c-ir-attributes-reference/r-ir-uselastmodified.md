---
description: 最終変更の応答ヘッダーを有効にします。 画像レンダリングから発生するキャッシュ可能なHTTP応答に、最終変更日時のヘッダを含めるかどうかを指定します。
seo-description: 最終変更の応答ヘッダーを有効にします。 画像レンダリングから発生するキャッシュ可能なHTTP応答に、最終変更日時のヘッダを含めるかどうかを指定します。
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

最終変更の応答ヘッダーを有効にします。 画像レンダリングから発生するキャッシュ可能なHTTP応答に、最終変更日時のヘッダを含めるかどうかを指定します。

サーバは、応答に含まれるす `vignette::TimeStamp` べてのビネット `catalog::TimeStamp` およびマテリアルカタログ/カタログレコードの最新の値と値を、最終変更時のヘッダ値として使用します。

etagヘッダーをサポートしていない分散キャッシュネットワーク（Akamaiなど）が使用されている場合にのみ有効にする必要があります。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>複数の画像サービング/レンダリングホストが関与する負荷分散環境で、最終変更時のヘッダを使用する場合は注意が必要です。 同じカタログエントリに対して異なるタイムスタンプを持つサーバーでは、クライアントのキャッシュが無効になり、サーバーの読み込みが増加する場合があります。 このような状況は、次のように発生します。

* また、ま `catalog::TimeStamp`たはが定 `vignette::TimeStamp`義されて `attribute::TimeStamp` いないので、ファイルの変更時刻がのデフォル [!DNL catalog.ini] トとして使用されま `catalog::TimeStamp`す。

* ネットワークマウントを介してマテリアルカタログファイルを共有する代わりに、各サーバはローカルファイルシステム上のカタログファイルの独自のインスタンスを持ちます。
* 同じファイルの複数のインスタンスが異な [!DNL catalog.ini] るファイル変更日を持つ。ファイルの不適切なコピーが原因である可能性があります。

## プロパティ {#section-453952244193452caccfaf7f601007c1}

フラグ。 0を指定すると無効になり、1を指定すると最終変更HTTPヘッダーが有効になります。

## 初期設定 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

定義されていな `default::UseLastModified` い場合や空の場合に継承されます。

## 関連項目 {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
