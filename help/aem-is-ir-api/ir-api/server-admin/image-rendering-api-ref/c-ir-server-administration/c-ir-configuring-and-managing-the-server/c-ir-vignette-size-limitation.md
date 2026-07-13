---
title: 周辺光量補正サイズの制限
description: 画像レンダリングでは、ピラミッド以外の周辺光量補正に2 メガピクセルのサイズ制限が適用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
TQID: 'https://experienceleague.adobe.com/qPrnkvYXinvZAfx-s6ePjpe64qsoBfwtVbUJ-fYBbmc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 0%

---

# 周辺光量補正サイズの制限{#vignette-size-limitation}

画像レンダリングでは、ピラミッド以外の周辺光量補正に2 メガピクセルのサイズ制限が適用されます。

アプリケーションでこの制限よりも大きい画像領域（幅x高さ）を持つピラミッド以外のビネットのサポートが必要な場合は、[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]の`IrMaxNonPyrVignetteSize`の値を変更します。

>[!NOTE]
>
>属性`attribute::MaxPix`と`IS::MaxMessageSize`を調整して、通常とは異なる大きさの応答画像サイズを許可します。 詳しくは、画像サービングのドキュメントを参照してください。

