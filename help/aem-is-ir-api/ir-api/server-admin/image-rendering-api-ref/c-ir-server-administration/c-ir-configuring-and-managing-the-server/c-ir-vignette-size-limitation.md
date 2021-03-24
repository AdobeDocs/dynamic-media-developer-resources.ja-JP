---
description: 画像レンダリングでは、非ピラミッドビネットに対して2メガピクセルのサイズ制限が適用されます。
solution: Experience Manager
title: ビネットサイズの制限
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# ビネットサイズの制限{#vignette-size-limitation}

画像レンダリングでは、非ピラミッドビネットに対して2メガピクセルのサイズ制限が適用されます。

アプリケーションで、この制限を超える画像領域（幅x高さ）を持つピラミッド以外のビネットをサポートする必要がある場合、[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]の`IrMaxNonPyrVignetteSize`の値を変更します。

>[!NOTE]
>
>`attribute::MaxPix` また、応答画像のサイズが異常に大きくなるように調整する `IS::MaxMessageSize` 必要がある場合もあります。詳しくは、画像サービングのドキュメントを参照してください。

