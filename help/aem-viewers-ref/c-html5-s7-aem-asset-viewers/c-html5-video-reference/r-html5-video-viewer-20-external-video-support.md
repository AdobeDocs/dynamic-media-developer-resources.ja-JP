---
title: 外部ビデオのサポート
description: このビューアでは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Mediaの外部でホストされるビデオの再生をサポートしています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# 外部ビデオのサポート{#external-video-support}

このビューアでは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Mediaの外部でホストされるビデオの再生をサポートしています。

外部ビデオでサポートされている形式は、H.264 形式の MP4 か、HLS ストリームの M3U8 マニフェストです。

ビューアは、Dynamic Media Classic、Experience Manager - Dynamic Media ビデオまたは外部ビデオと連携して動作します。 ビューアがDynamic Media Classic/Dynamic Media ビデオから開始する場合は、そのようなアセットタイプで使用してください。[`setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) の方法では、このビューアに外部ビデオを読み込むことができません。 そして逆の節：ビューアが最初に外部ビデオで読み込まれた場合、外部ビデオでのみ作業し続ける必要があります。

外部ビデオを操作する場合、ビューアは再生の修飾子の値を無視し、再生タイプを外部ビデオ拡張機能から検出します。 外部ビデオ URL の末尾が `.m3u8` で、ビューアが HLS 再生を使用している場合は、プログレッシブ再生が使用されます。
