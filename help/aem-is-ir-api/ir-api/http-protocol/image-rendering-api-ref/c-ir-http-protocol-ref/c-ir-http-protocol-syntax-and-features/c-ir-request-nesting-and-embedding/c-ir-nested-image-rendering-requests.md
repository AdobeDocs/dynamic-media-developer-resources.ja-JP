---
description: 高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから得られた画像と同じように、素材画像として使用できます。
solution: Experience Manager
title: ネストされた画像レンダリング要求
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# ネストされた画像レンダリング要求{#nested-image-rendering-requests}

高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから得られた画像と同じように、素材画像として使用できます。

レンダリング要求は、次のように`src=`コマンドで指定することで、マテリアルイメージとして使用できます。

` …&src=ir{ *[!DNL renderRequest]*}&…`

`ir`トークンでは大文字と小文字が区別されます。

ネストされたリクエストには、画像レンダリングのルートパス（通常は`http:// *[!DNL server]*/ir/render/'`）を含めることはできませんが、前処理ルールトークンを含めることもできます。

ネストされたリクエストで（リクエストURLまたは`catalog::Modifier`または`catalog::PostModifier`で）指定された場合、次のコマンドは無視されます。

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

また、ネストされたレンダリング要求に適用されるマテリアルカタログの`attribute::MaxPix`と`attribute::DefaultPix`も無視されます。

ネストされたIR要求の画像結果は、オプションで`cache=on`を含めることでキャッシュできます。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間画像が適切な期間内に別のリクエストで再利用されると予想される場合にのみ有効にする必要があります。 標準のサーバー側キャッシュ管理が適用されます。 データは可逆形式でキャッシュされます。
