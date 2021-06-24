---
description: ビューアは、Dynamic Media ClassicまたはAEM Dynamic Mediaの外部でホストされているビデオの再生をサポートしています。
solution: Experience Manager
title: 外部ビデオのサポート
feature: Dynamic Media Classic，ビューア，SDK/API，ビデオ
role: Developer,Business Practitioner
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# 外部ビデオのサポート{#external-video-support}

ビューアは、Dynamic Media ClassicまたはAEM Dynamic Mediaの外部でホストされているビデオの再生をサポートしています。

外部ビデオでサポートされる形式は、H.264形式のMP4またはHLSストリーム用のM3U8マニフェストです。

ビューアは、Dynamic Media ClassicまたはAEM Dynamic Mediaビデオで動作するか、外部ビデオで動作させることができます。 ビューアがDynamic Media Classic/Dynamic Mediaビデオで開始する場合は、今後そのようなアセットタイプで使用するので、 [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)メソッドを使用して、このビューアに外部ビデオを読み込むことはできません。 そして副詞：ビューアが最初に外部ビデオと共に読み込まれた場合は、外部ビデオでのみ動作し続ける必要があります。

外部ビデオを操作する場合、ビューアは再生修飾子の値を無視し、外部ビデオ拡張子から再生タイプを検出します。 外部ビデオのURLが.m3u8で終わる場合、ビューアはHLS再生を使用し、それ以外の場合はプログレッシブ再生が使用されます。
