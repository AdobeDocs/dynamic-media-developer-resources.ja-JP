---
title: 埋め込み Image Server の要求
description: Image Server(IS) 要求は、マテリアルイメージとして使用できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 埋め込み Image Server の要求{#embedded-image-server-requests}

Image Server(IS) 要求は、マテリアルイメージとして使用できます。

リクエストを `src=` コマンドを次のように指定します。

` …&src=is( *[!DNL imageServingRequest]*)&…`

この `is` トークンでは大文字と小文字が区別されます。

ネストされた要求に画像サービングのルートパスを含めることはできません ( 通常は [!DNL http:// *[!DNL server]*/is/image/"]) ですが、前処理ルールトークンを含めることができます。

ネストされたリクエストで（リクエスト URL またはで）指定した場合、次の IS コマンドは無視されます。 `catalog::Modifier` または `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

また、無視されます `attribute::MaxPix` および `attribute::DefaultPix` 埋め込み IS 要求に適用される画像カタログの

ネストされたリクエストの結果イメージにマスク（アルファ）データが含まれる場合、そのイメージは常にマテリアルに渡されます。 不要なアルファを避けるには、べた塗りの背景画像レイヤーを使用します。

埋め込まれた IS リクエストのイメージ結果は、必要に応じて `cache=on`. デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間画像が別のリクエストで妥当な期間内に再利用される場合にのみ有効にする必要があります。 標準のサーバー側キャッシュ管理が適用されます。 データはロスレス形式でキャッシュされます。
