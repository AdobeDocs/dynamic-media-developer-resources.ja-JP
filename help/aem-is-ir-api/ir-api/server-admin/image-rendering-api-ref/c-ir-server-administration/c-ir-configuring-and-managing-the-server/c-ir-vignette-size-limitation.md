---
title: ビネットサイズの制限
description: 画像レンダリングでは、ピラミッド以外のビネットに対して 2 メガピクセルのサイズ制限が適用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# ビネットサイズの制限{#vignette-size-limitation}

画像レンダリングでは、ピラミッド以外のビネットに対して 2 メガピクセルのサイズ制限が適用されます。

アプリケーションで、この制限を超える画像領域（幅 x 高さ）を持つピラミッド以外のビネットのサポートが必要な場合は、[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] の `IrMaxNonPyrVignetteSize` の値を変更します。

>[!NOTE]
>
>`attribute::MaxPix` および `IS::MaxMessageSize` の属性を調整して、非常に大きな応答画像サイズができるようにします。 詳しくは、画像サービングドキュメントを参照してください。
