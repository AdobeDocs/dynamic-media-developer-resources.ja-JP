---
title: 埋め込みImage Server リクエスト
description: Image Server （IS）リクエストは、マテリアル画像として使用できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
TQID: 'https://experienceleague.adobe.com/dt-baBh9jAyJdjqopFR3AoqRvz5zqLzi8B3SnE04xEs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# 埋め込みImage Server リクエスト{#embedded-image-server-requests}

Image Server （IS）リクエストは、マテリアル画像として使用できます。

次のように、`src=` コマンドでリクエストを指定します。

` …&src=is( *[!DNL imageServingRequest]*)&…`

`is` トークンでは、大文字と小文字が区別されます。

ネストされたリクエストには、画像サービングルートパス（通常 [!DNL http:// *[!DNL server]*/is/image/"]）を含めることはできませんが、前処理ルールトークンを含めることができます。

次のIS コマンドは、ネストされたリクエスト（リクエスト URLまたは`catalog::Modifier`または`catalog::PostModifier`のいずれかで）で指定された場合は無視されます。

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

埋め込まれたIS リクエストに適用される画像カタログの`attribute::MaxPix`と`attribute::DefaultPix`も無視されます。

ネストされたリクエストの結果画像にマスク（アルファ）データが含まれる場合、常にマテリアルに渡されます。 不要なアルファを避けるために、単色の背景画像レイヤーを使用します。

埋め込まれたIS リクエストの画像の結果は、`cache=on`を含めることで、オプションでキャッシュできます。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間画像が合理的な期間内に別のリクエストで再利用された場合にのみ有効にする必要があります。 標準的なサーバーサイドのキャッシュ管理が適用されます。 データは可逆形式でキャッシュされます。

