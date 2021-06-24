---
description: Image Server(IS)要求は、マテリアルイメージとして使用できます。
solution: Experience Manager
title: 埋め込み画像サーバーのリクエスト
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# 埋め込み画像サーバーのリクエスト{#embedded-image-server-requests}

Image Server(IS)要求は、マテリアルイメージとして使用できます。

`src=`コマンドで、次のように要求を指定します。

` …&src=is( *[!DNL imageServingRequest]*)&…`

`is`トークンでは大文字と小文字が区別されます。

ネストされたリクエストには、画像サービングのルートパス(通常は[!DNL http:// *[!DNL server]*/is/image/&quot;])を含めることはできませんが、前処理ルールトークンを含めることもできます。

ネストされたリクエストで（リクエストURL、`catalog::Modifier`、`catalog::PostModifier`のいずれかで）指定された場合、次のISコマンドは無視されます。

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

また、埋め込みISリクエストに適用される画像カタログの`attribute::MaxPix`と`attribute::DefaultPix`も無視されます。

ネストされたリクエストの結果イメージにマスク（アルファ）データが含まれる場合、常にマテリアルに渡されます。 不要なアルファを避けるには、べた塗りの背景画像レイヤーを使用します。

埋め込みIS要求のイメージ結果は、必要に応じて`cache=on`を含めることでキャッシュできます。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間画像が適切な期間内に別のリクエストで再利用されると予想される場合にのみ有効にする必要があります。 標準のサーバー側キャッシュ管理が適用されます。 データは可逆形式でキャッシュされます。
