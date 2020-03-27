---
description: ビューアは、SPSまたはAEMダイナミックメディアの外部でホストされているビデオの再生をサポートしています。
seo-description: ビューアは、SPSまたはAEMダイナミックメディアの外部でホストされているビデオの再生をサポートしています。
seo-title: 外部ビデオのサポート
solution: Experience Manager
title: 外部ビデオのサポート
topic: Dynamic media
uuid: 2e9f1c54-627f-4462-ae85-8a5ca1d09762
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 外部ビデオのサポート{#external-video-support}

ビューアは、SPSまたはAEMダイナミックメディアの外部でホストされているビデオの再生をサポートしています。

外部ビデオでサポートされている形式は、H.264形式のMP4またはHLSストリームのM3U8マニフェストです。

ビューアは、ダイナミックメディアクラシックまたはAEMダイナミックメディアビデオ、または外部ビデオと連携して動作します。 ビューアがDynamic Media Classic/AEM Dynamic Mediaビデオで始まる場合は、今後、そのようなアセットタイプで使用する必要があります。 setVideoメソッドを使用して外部ビデオをこのビューアに読み込むことはできません。また [、その逆も](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) 同じです。 つまり、ビューアが最初に外部ビデオと共に読み込まれた場合、引き続き外部ビデオのみで機能します。

外部ビデオを操作する場合、ビューアは再生修飾子の値を無視し、外部ビデオ拡張子から再生タイプを検出します。 外部ビデオのURLがで終わる場合、ビ `.m3u8`ューアはHLS再生を使用しています。それ以外の場合は、プログレッシブ再生が使用されます。
