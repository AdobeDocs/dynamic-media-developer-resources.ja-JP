---
title: ネストされた画像レンダリングリクエスト
description: 高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから取得した画像と同様に、マテリアル画像として使用できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# ネストされた画像レンダリングリクエスト{#nested-image-rendering-requests}

高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから取得した画像と同様に、マテリアル画像として使用できます。

レンダリング要求をマテリアル イメージとして使用するには、`src=` コマンドで次のように指定します。

` …&src=ir{ *[!DNL renderRequest]*}&…`

`ir` トークンでは大文字と小文字が区別されます。

ネストされたリクエストに画像レンダリングのルートパス（通常は `http:// *[!DNL server]*/ir/render/'`）を含めることはできません。ただし、前処理のルールトークンを含めることができます。

次のコマンドは、ネストされたリクエストで（リクエスト url または `catalog::Modifier` または `catalog::PostModifier` で）指定した場合は無視されます。

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

また、ネストされたレンダリング要求に適用されるマテリアル カタログの `attribute::MaxPix` と `attribute::DefaultPix` も無視されます。

ネストされた IR 要求のイメージ結果は、`cache=on` を含めることでオプションでキャッシュできます。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、適切な期間内に別のリクエストで中間画像が再利用された場合にのみ有効にしてください。 標準のサーバーサイドキャッシュ管理が適用されます。 データは、可逆形式でキャッシュされます。
