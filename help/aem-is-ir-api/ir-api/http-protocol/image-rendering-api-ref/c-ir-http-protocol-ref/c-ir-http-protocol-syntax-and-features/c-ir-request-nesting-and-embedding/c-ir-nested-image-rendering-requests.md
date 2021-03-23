---
description: 高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから取得した画像と同様に、マテリアル画像として使用できます。
seo-description: 高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから取得した画像と同様に、マテリアル画像として使用できます。
seo-title: ネストされた画像レンダリング要求
solution: Experience Manager
title: ネストされた画像レンダリング要求
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---


# ネストされた画像レンダリング要求{#nested-image-rendering-requests}

高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから取得した画像と同様に、マテリアル画像として使用できます。

レンダリング要求は、次のように`src=`コマンドで指定することで、マテリアルイメージとして使用できます。

` …&src=ir{ *[!DNL renderRequest]*}&…`

`ir`トークンでは大文字と小文字が区別されます。

ネストされた要求には、画像レンダリングのルートパス（通常は`http:// *[!DNL server]*/ir/render/'`）を含めることはできませんが、前処理ルールトークンを含めることができます。

ネストされた要求（要求URL、`catalog::Modifier`、または`catalog::PostModifier`）で指定した場合、次のコマンドは無視されます。

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

また、ネストされたレンダリング要求に適用されるマテリアルカタログの`attribute::MaxPix`と`attribute::DefaultPix`も無視されます。

入れ子にされたIR要求のイメージ結果は、`cache=on`を含めることで、オプションでキャッシュできます。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間イメージが別の要求で妥当な期間内に再利用されると予想される場合にのみ有効にする必要があります。 標準のサーバー側キャッシュ管理が適用されます。 データは可逆の形式でキャッシュされます。
