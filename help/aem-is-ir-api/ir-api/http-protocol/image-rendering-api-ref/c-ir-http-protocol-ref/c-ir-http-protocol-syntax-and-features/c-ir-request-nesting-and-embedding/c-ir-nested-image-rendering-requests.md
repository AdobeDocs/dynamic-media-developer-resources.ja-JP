---
description: 高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから取得した画像と同様に、マテリアル画像として使用できます。
seo-description: 高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから取得した画像と同様に、マテリアル画像として使用できます。
seo-title: ネストされた画像レンダリング要求
solution: Experience Manager
title: ネストされた画像レンダリング要求
topic: Scene7 Image Serving - Image Rendering API
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ネストされた画像レンダリング要求{#nested-image-rendering-requests}

高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから取得した画像と同様に、マテリアル画像として使用できます。

レンダリング要求は、次のコマンドで指定することで、マテリアルイメージとし `src=` て使用できます。

` …&src=ir{ *[!DNL renderRequest]*}&…`

トークン `ir` では大文字と小文字が区別されます。

ネストされた要求には、画像レンダリングのルートパス(通常は `http:// *[!DNL server]*/ir/render/'`)を含める必要はありませんが、前処理ルールトークンを含めることができます。

ネストされたリクエスト（リクエストURLまたはまたは内）で指定した場合、次のコマンドは無視 `catalog::Modifier` され `catalog::PostModifier`ます。

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

また、ネストされたレ `attribute::MaxPix` ンダリング `attribute::DefaultPix` 要求に適用されるマテリアルカタログのも無視されます。

入れ子になったIR要求のイメージ結果は、を含めることで、オプションでキャッシュできま `cache=on`す。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間イメージが別の要求で適切な期間内に再利用されると予想される場合にのみ有効にする必要があります。 標準のサーバー側キャッシュ管理が適用されます。 データは可逆圧縮形式でキャッシュされます。
