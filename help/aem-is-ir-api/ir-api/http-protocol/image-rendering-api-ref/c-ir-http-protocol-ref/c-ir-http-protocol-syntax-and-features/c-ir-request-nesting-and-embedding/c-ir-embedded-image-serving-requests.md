---
description: Image Server(IS)要求は、マテリアルイメージとして使用できます。
seo-description: Image Server(IS)要求は、マテリアルイメージとして使用できます。
seo-title: 埋め込みImage Serverの要求
solution: Experience Manager
title: 埋め込みImage Serverの要求
topic: Scene7 Image Serving - Image Rendering API
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 埋め込みImage Serverの要求{#embedded-image-server-requests}

Image Server(IS)要求は、マテリアルイメージとして使用できます。

コマンドで次のように要求 `src=` を指定します。

` …&src=is( *[!DNL imageServingRequest]*)&…`

トークン `is` では大文字と小文字が区別されます。

入れ子にされた要求には、画像サービングのルートパス(通常は[!DNL http:// *[!DNL server]*/is/image/&quot;])を含めることはできませんが、前処理ルールトークンを含めることができます。

ネストされたリクエスト（リクエストURLまたはまたは内）で指定した場合、次のISコマンドは無 `catalog::Modifier` 視され `catalog::PostModifier`ます。

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

また、埋め込みIS `attribute::MaxPix` 要求に `attribute::DefaultPix` 適用される画像カタログのも無視されます。

ネストされた要求の結果イメージにマスク（アルファ）データが含まれる場合、そのイメージは常にマテリアルに渡されます。 背景の画像レイヤーをべた塗りにして、不要なアルファを避けます。

埋め込みIS要求の画像結果は、を含めることで、オプションでキャッシュできま `cache=on`す。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間イメージが別の要求で適切な期間内に再利用されると予想される場合にのみ有効にする必要があります。 標準のサーバー側キャッシュ管理が適用されます。 データは可逆圧縮形式でキャッシュされます。
