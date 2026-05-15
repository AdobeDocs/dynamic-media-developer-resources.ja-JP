---
title: 外部ビデオのサポート
description: ビューアは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Media以外でホストされているビデオの再生をサポートしています。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
TQID: 'https://experienceleague.adobe.com/nLVjtwe8hj5YpMX6M1GKt1Fx-tZK2Qxe1kdWcK8BQPw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 0%

---

# 外部ビデオのサポート{#external-video-support}

ビューアは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Media以外でホストされているビデオの再生をサポートしています。

外部ビデオでサポートされる形式は、H.264形式のMP4またはHLS ストリームのM3U8 マニフェストです。

ビューアは、Dynamic Media ClassicまたはExperience Manager - Dynamic Media ビデオまたは外部ビデオで動作します。 ビューアがDynamic Media Classic/Dynamic Media ビデオで始まる場合は、今後このようなアセットタイプで使用します。を使用して外部ビデオをビューアに読み込むことはできません [`setVideo`]
（../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c） メソッドを使用します。 逆の逆：ビューアが最初に外部ビデオで読み込まれた場合は、外部ビデオのみを使用し続ける必要があります。

外部動画を操作する場合、ビューアは再生修飾子の値を無視し、外部動画拡張機能から再生タイプを検出します。 外部ビデオのURLが`.M3U8`で終わる場合、ビューアはHLS再生を使用しています。それ以外の場合は、プログレッシブ再生が使用されます。
