---
title: 外部ビデオのサポート
description: ビューアは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Mediaの外部でホストされているビデオの再生をサポートします。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# 外部ビデオのサポート{#external-video-support}

ビューアは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Mediaの外部でホストされているビデオの再生をサポートします。

外部ビデオでサポートされる形式は、H.264 形式の MP4 または HLS ストリームの M3U8 マニフェストです。

ビューアは、Dynamic Media ClassicまたはExperience Manager- Dynamic Mediaビデオでも、外部ビデオでも動作します。 ビューアがDynamic Media Classic/Dynamic Mediaビデオで始まる場合、そのようなアセットタイプで使用すると、外部ビデオを次を使用してこのビューアに読み込むことはできません。 [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) メソッド。 そして逆の詩：ビューアが最初に外部ビデオで読み込まれた場合は、外部ビデオでのみ動作を続ける必要があります。

外部ビデオを操作する場合、ビューアは再生修飾子の値を無視し、外部ビデオ拡張機能から再生タイプを検出します。 外部ビデオの URL が次の語句で終わる場合 `.m3u8` ビューアでは HLS 再生が使用されていますが、それ以外の場合はプログレッシブ再生が使用されます。
