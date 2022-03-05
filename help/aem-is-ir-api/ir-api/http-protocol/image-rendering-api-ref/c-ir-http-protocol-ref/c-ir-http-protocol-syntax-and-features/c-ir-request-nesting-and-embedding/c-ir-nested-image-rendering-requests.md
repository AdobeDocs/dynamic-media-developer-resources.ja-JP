---
title: ネストされた画像レンダリング要求
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

# ネストされた画像レンダリング要求{#nested-image-rendering-requests}

高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから取得した画像と同様に、マテリアル画像として使用できます。

レンダリングリクエストは、 `src=` コマンドを次のように指定します。

` …&src=ir{ *[!DNL renderRequest]*}&…`

この `ir` トークンでは大文字と小文字が区別されます。

ネストされたリクエストに画像レンダリングのルートパスを含めることはできません ( 通常は `http:// *[!DNL server]*/ir/render/'`) ですが、前処理ルールトークンを含めることができます。

ネストされたリクエストで ( リクエスト URL または `catalog::Modifier` または `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

また、無視されます `attribute::MaxPix` および `attribute::DefaultPix` ネストされたレンダリング要求に適用されるマテリアルカタログの

ネストされた IR 要求の画像結果は、オプションで `cache=on`. デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間画像が別のリクエストで妥当な期間内に再利用される場合にのみ有効にする必要があります。 標準のサーバー側キャッシュ管理が適用されます。 データはロスレス形式でキャッシュされます。
