---
title: ネストされた画像レンダリングリクエスト
description: 高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから得られた画像と同様に、マテリアル画像として使用することができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
TQID: 'https://experienceleague.adobe.com/Fqiu-HsaRtrWMjBQudUBzr1iu3WLg7173Kf-71ikejI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# ネストされた画像レンダリングリクエスト{#nested-image-rendering-requests}

高度なアプリケーションでは、レンダリング操作の結果を、画像サービングから得られた画像と同様に、マテリアル画像として使用することができます。

レンダーリクエストは、`src=` コマンドで次のように指定することで、マテリアルイメージとして使用できます。

` …&src=ir{ *[!DNL renderRequest]*}&…`

`ir` トークンでは、大文字と小文字が区別されます。

ネストされたリクエストには、画像レンダリングのルートパス（通常は`http:// *[!DNL server]*/ir/render/'`）を含めることはできませんが、前処理ルールトークンを含めることができます。

次のコマンドは、ネストされたリクエスト（リクエスト URLまたは`catalog::Modifier`または`catalog::PostModifier`のいずれかで）で指定された場合は無視されます。

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

また、ネストされたレンダーリクエストに適用されるマテリアルカタログの`attribute::MaxPix`と`attribute::DefaultPix`も無視されます。

ネストされたIR リクエストの画像の結果は、`cache=on`を含めることで、オプションでキャッシュできます。 デフォルトでは、中間データのキャッシュは無効になっています。 キャッシュは、中間画像が合理的な期間内に別のリクエストで再利用された場合にのみ有効にする必要があります。 標準的なサーバーサイドのキャッシュ管理が適用されます。 データは可逆形式でキャッシュされます。

