---
description: ビューアでは、Scene7パブリッシングシステムまたはAEMDynamic Mediaの外部でホストされているビデオの再生がサポートされています。
seo-description: ビューアでは、Scene7パブリッシングシステムまたはAEMDynamic Mediaの外部でホストされているビデオの再生がサポートされています。
seo-title: 外部ビデオのサポート
solution: Experience Manager
title: 外部ビデオのサポート
topic: Dynamic media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# 外部ビデオのサポート{#external-video-support}

ビューアでは、Scene7パブリッシングシステムまたはAEMDynamic Mediaの外部でホストされているビデオの再生がサポートされています。

外部ビデオでサポートされる形式は、H.264形式のMP4またはHLSストリーム用のM3U8マニフェストです。

ビューアは、Scene7ビデオまたはDynamic Mediaビデオ、または外部ビデオを使用できます。 Scene7/Dynamic Mediaビデオを含むビューア開始が、このようなアセットタイプで使用される場合、[ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)メソッドを使用して外部ビデオをこのビューアに読み込むことはできません。 そして、次の副詞：ビューアが最初に外部ビデオと共に読み込まれた場合、外部ビデオのみで作業を続ける必要があります。

外部ビデオを扱う場合、ビューアでは再生修飾子の値が無視され、外部ビデオ拡張子から再生タイプが検出されます。 外部ビデオURLが.m3u8で終わる場合、ビューアではHLS再生が使用され、それ以外の場合はプログレッシブ再生が使用されます。
