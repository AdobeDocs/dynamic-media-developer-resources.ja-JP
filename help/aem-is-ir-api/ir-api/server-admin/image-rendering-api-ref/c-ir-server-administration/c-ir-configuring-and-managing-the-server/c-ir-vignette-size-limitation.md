---
description: 画像レンダリングでは、角錐以外のビネットに対して2メガピクセルのサイズ制限が適用されます。
seo-description: 画像レンダリングでは、角錐以外のビネットに対して2メガピクセルのサイズ制限が適用されます。
seo-title: ビネットサイズの制限
solution: Experience Manager
title: ビネットサイズの制限
topic: Scene7 Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ビネットサイズの制限{#vignette-size-limitation}

画像レンダリングでは、角錐以外のビネットに対して2メガピクセルのサイズ制限が適用されます。

アプリケーションで、こ `IrMaxNonPyrVignetteSize` の制限を超える画像領域（幅x高さ）を持つピラミッド以外のビネットをサポートする必要がある場合は、[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]のの値を変更します。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>`attribute::MaxPix` また、応 `IS::MaxMessageSize` 答画像のサイズが異常に大きくなるように調整する必要がある場合もあります。 詳しくは、画像サービングのドキュメントを参照してください。

