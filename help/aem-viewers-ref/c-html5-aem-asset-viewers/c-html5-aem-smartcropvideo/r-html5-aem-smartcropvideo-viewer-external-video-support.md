---
description: ビューアでは、Dynamic Media ClassicまたはAEM Dynamic Mediaの外部でホストされるビデオの再生がサポートされています。
solution: Experience Manager
title: 外部ビデオのサポート
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# 外部ビデオのサポート{#external-video-support}

ビューアでは、Dynamic Media ClassicまたはAEM Dynamic Mediaの外部でホストされるビデオの再生がサポートされています。

外部ビデオでサポートされる形式は、H.264 形式の MP4 または HLS ストリームの M3U8 マニフェストです。

ビューアは、Dynamic Media ClassicまたはAEM Dynamic Mediaビデオで動作することも、外部ビデオで動作することもできます。 ビューアがDynamic Media Classic/Dynamic Mediaビデオで始まる場合、そのようなアセットタイプで使用すると、外部ビデオを次を使用してこのビューアに読み込むことはできません。 [ `setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) メソッドを使用します。 そして逆の詩：ビューアが最初に外部ビデオで読み込まれた場合は、外部ビデオでのみ動作を続ける必要があります。

外部ビデオを操作する場合、ビューアは再生修飾子の値を無視し、外部ビデオ拡張機能から再生タイプを検出します。 外部ビデオの URLが.m3u8 で終わる場合、ビューアは HLS 再生を使用しています。それ以外の場合は、プログレッシブ再生が使用されます。
