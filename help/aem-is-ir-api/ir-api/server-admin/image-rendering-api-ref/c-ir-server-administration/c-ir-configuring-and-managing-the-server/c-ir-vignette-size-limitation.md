---
description: 画像レンダリングでは、非ピラミッドビネットに対して2メガピクセルのサイズ制限が適用されます。
seo-description: 画像レンダリングでは、非ピラミッドビネットに対して2メガピクセルのサイズ制限が適用されます。
seo-title: ビネットサイズの制限
solution: Experience Manager
title: ビネットサイズの制限
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# ビネットサイズの制限{#vignette-size-limitation}

画像レンダリングでは、非ピラミッドビネットに対して2メガピクセルのサイズ制限が適用されます。

アプリケーションで、この制限を超える画像領域（幅x高さ）を持つピラミッド以外のビネットをサポートする必要がある場合、[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]の`IrMaxNonPyrVignetteSize`の値を変更します。

>[!NOTE]
>
>`attribute::MaxPix` また、応答画像のサイズが異常に大きくなるように調整する `IS::MaxMessageSize` 必要がある場合もあります。詳しくは、画像サービングのドキュメントを参照してください。

