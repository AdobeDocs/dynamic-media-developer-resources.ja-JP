---
title: 埋め込み Image Server リクエスト
description: Image Server （IS）リクエストは、素材画像として使用できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 埋め込み Image Server リクエスト{#embedded-image-server-requests}

Image Server （IS）リクエストは、素材画像として使用できます。

`src=` コマンドでリクエストを次のように指定します。

` …&src=is( *[!DNL imageServingRequest]*)&…`

`is` トークンでは大文字と小文字が区別されます。

ネストされたリクエストには、画像サービングのルートパス（通常は  [!DNL http:// *[!DNL server]*/is/image/"]）を含めないでください。ただし、前処理ルールトークンを含めることができます。

次の IS コマンドは、ネストされたリクエストで（リクエスト URL または `catalog::Modifier` または `catalog::PostModifier` で）指定された場合、無視されます。

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

また、埋め込まれた IS リクエストに適用される画像カタログの `attribute::MaxPix` と `attribute::DefaultPix` も無視されます。

ネストされたリクエストの結果イメージにマスク（アルファ）データが含まれる場合、そのイメージは常にマテリアルに渡されます。 アルファが不要にならないようにするには、単色の背景画像レイヤーを使用します。

埋め込まれた IS リクエストの画像結果は、`cache=on` を含めることでオプションでキャッシュできます。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、適切な期間内に別のリクエストで中間画像が再利用された場合にのみ有効にしてください。 標準のサーバーサイドキャッシュ管理が適用されます。 データは、可逆形式でキャッシュされます。
