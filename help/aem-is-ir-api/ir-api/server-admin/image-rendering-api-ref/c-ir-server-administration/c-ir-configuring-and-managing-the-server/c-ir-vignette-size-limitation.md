---
description: 画像レンダリングでは、非ピラミッドビネットに対して2メガピクセルのサイズ制限が適用されます。
solution: Experience Manager
title: ビネットサイズの制限
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# ビネットサイズの制限{#vignette-size-limitation}

画像レンダリングでは、非ピラミッドビネットに対して2メガピクセルのサイズ制限が適用されます。

アプリケーションで、この制限を超える画像領域（幅x高さ）を持つ非ピラミッドビネットをサポートする必要がある場合は、[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]の`IrMaxNonPyrVignetteSize`の値を変更します。

>[!NOTE]
>
>`attribute::MaxPix` また、応答 `IS::MaxMessageSize` 画像のサイズが異常に大きくなるように調整する必要が生じる場合もあります。詳しくは、画像サービングのドキュメントを参照してください。
