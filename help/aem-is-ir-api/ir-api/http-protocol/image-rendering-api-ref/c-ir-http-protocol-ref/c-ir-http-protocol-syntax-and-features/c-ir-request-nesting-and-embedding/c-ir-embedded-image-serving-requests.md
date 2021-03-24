---
description: Image Server(IS)要求は、マテリアルイメージとして使用できます。
solution: Experience Manager
title: 埋め込みImage Serverの要求
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# 埋め込みImage Serverの要求{#embedded-image-server-requests}

Image Server(IS)要求は、マテリアルイメージとして使用できます。

`src=`コマンドで次のように要求を指定します。

` …&src=is( *[!DNL imageServingRequest]*)&…`

`is`トークンでは大文字と小文字が区別されます。

入れ子の要求には、画像サービングのルートパス(通常は[!DNL http:// *[!DNL server]*/is/image/&quot;])を含めることはできませんが、前処理規則のトークンを含めることはできます。

ネストされた要求（要求URL、`catalog::Modifier`または`catalog::PostModifier`内）で指定した場合、次のISコマンドは無視されます。

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

また、埋め込みIS要求に適用される画像カタログの`attribute::MaxPix`と`attribute::DefaultPix`も無視されます。

ネストされた要求の結果イメージにマスク（アルファ）データが含まれる場合、その画像は常にマテリアルに渡されます。 べた塗りの背景画像レイヤーを使用して、不要なアルファを回避します。

埋め込みIS要求のイメージ結果は、`cache=on`を含めることで、オプションでキャッシュできます。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間イメージが別の要求で妥当な期間内に再利用されると予想される場合にのみ有効にする必要があります。 標準のサーバー側キャッシュ管理が適用されます。 データは可逆の形式でキャッシュされます。
