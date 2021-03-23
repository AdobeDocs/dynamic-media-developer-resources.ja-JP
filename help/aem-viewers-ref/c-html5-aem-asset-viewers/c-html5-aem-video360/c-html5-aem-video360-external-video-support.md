---
description: ビューアは、Dynamic MediaクラシックまたはAEMDynamic Media以外でホストされているビデオの再生をサポートしています。
solution: Experience Manager
title: 外部ビデオのサポート
feature: Dynamic Mediaクラシック，ビューア，SDK/API,360 VRビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# 外部ビデオのサポート{#external-video-support}

ビューアは、Dynamic MediaクラシックまたはAEMDynamic Media以外でホストされているビデオの再生をサポートしています。

外部ビデオでサポートされる形式は、H.264形式のMP4またはHLSストリーム用のM3U8マニフェストです。

ビューアは、Dynamic Mediaクラシックビデオ、AEMDynamic Mediaビデオ、または外部ビデオを使用できます。 Dynamic Mediaクラシック/AEMDynamic Mediaビデオを使用するビューア開始の場合は、今後、そのようなアセットタイプで使用する必要があります。 [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)メソッドを使用して外部ビデオをこのビューアに読み込むことはできません。また、その逆も同じです。 つまり、ビューアが最初に外部ビデオと共に読み込まれた場合、引き続き外部ビデオのみで動作します。

外部ビデオを扱う場合、ビューアでは再生修飾子の値が無視され、外部ビデオ拡張子から再生タイプが検出されます。 外部ビデオURLが`.m3u8`で終わる場合、ビューアはHLS再生を使用します。それ以外の場合は、プログレッシブ再生が使用されます。
