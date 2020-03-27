---
description: ビューアは、Scene7 Publishing SystemまたはAEMダイナミックメディアの外部でホストされているビデオの再生をサポートしています。
seo-description: ビューアは、Scene7 Publishing SystemまたはAEMダイナミックメディアの外部でホストされているビデオの再生をサポートしています。
seo-title: 外部ビデオのサポート
solution: Experience Manager
title: 外部ビデオのサポート
topic: Dynamic media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 外部ビデオのサポート{#external-video-support}

ビューアは、Scene7 Publishing SystemまたはAEMダイナミックメディアの外部でホストされているビデオの再生をサポートしています。

外部ビデオでサポートされている形式は、H.264形式のMP4またはHLSストリームのM3U8マニフェストです。

ビューアは、Scene7ビデオまたはダイナミックメディアビデオ、または外部ビデオと連携できます。 ビューアがScene7/Dynamic Mediaビデオで始まる場合は、そのようなアセットタイプで使用し、方法を使用して外部ビデオをこのビューアに読み込むことはできま [`setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) せん。 そして副詞：ビューアが最初に外部ビデオと共に読み込まれた場合は、外部ビデオのみで作業を続ける必要があります。

外部ビデオを操作する場合、ビューアは再生修飾子の値を無視し、外部ビデオ拡張子から再生タイプを検出します。 外部ビデオのURLが.m3u8で終わる場合、ビューアはHLS再生を使用し、それ以外の場合はプログレッシブ再生が使用されます。
