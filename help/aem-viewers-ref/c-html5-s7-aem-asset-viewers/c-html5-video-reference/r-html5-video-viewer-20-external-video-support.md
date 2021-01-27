---
description: ビューアは、Dynamic MediaクラシックまたはAEMDynamic Media以外でホストされているビデオの再生をサポートしています。
solution: Experience Manager
title: 外部ビデオのサポート
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# 外部ビデオのサポート{#external-video-support}

ビューアは、Dynamic MediaクラシックまたはAEMDynamic Media以外でホストされているビデオの再生をサポートしています。

外部ビデオでサポートされる形式は、H.264形式のMP4またはHLSストリーム用のM3U8マニフェストです。

ビューアは、Dynamic Mediaクラシックビデオ、AEMDynamic Mediaビデオ、または外部ビデオを使用できます。 Dynamic Mediaクラシック/Dynamic Mediaビデオを含むビューア開始が、このようなアセットタイプで使用される場合、[ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)メソッドを使用して外部ビデオをこのビューアに読み込むことはできません。 そして、次の副詞：ビューアが最初に外部ビデオと共に読み込まれた場合、外部ビデオのみで作業を続ける必要があります。

外部ビデオを扱う場合、ビューアでは再生修飾子の値が無視され、外部ビデオ拡張子から再生タイプが検出されます。 外部ビデオURLが.m3u8で終わる場合、ビューアではHLS再生が使用され、それ以外の場合はプログレッシブ再生が使用されます。
