---
description: 画像レンダリングでは、非ピラミッドビネットに対して2メガピクセルのサイズ制限が適用されます。
seo-description: 画像レンダリングでは、非ピラミッドビネットに対して2メガピクセルのサイズ制限が適用されます。
seo-title: ビネットサイズの制限
solution: Experience Manager
title: ビネットサイズの制限
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# ビネットサイズの制限{#vignette-size-limitation}

画像レンダリングでは、非ピラミッドビネットに対して2メガピクセルのサイズ制限が適用されます。

アプリケーションで、この制限を超える画像領域（幅x高さ）を持つピラミッド以外のビネットをサポートする必要がある場合、[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]の`IrMaxNonPyrVignetteSize`の値を変更します。

>[!NOTE]
>
>`attribute::MaxPix` また、応答画像のサイズが異常に大きくなるように調整する `IS::MaxMessageSize` 必要がある場合もあります。詳しくは、画像サービングのドキュメントを参照してください。

