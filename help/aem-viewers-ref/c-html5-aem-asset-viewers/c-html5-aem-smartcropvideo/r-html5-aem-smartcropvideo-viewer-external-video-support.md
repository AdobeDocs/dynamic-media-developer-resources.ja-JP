---
title: 外部ビデオのサポート
description: ビューアは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Mediaの外部でホストされているビデオの再生をサポートします。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# 外部ビデオのサポート{#external-video-support}

ビューアは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Mediaの外部でホストされているビデオの再生をサポートします。

外部ビデオでサポートされる形式は、H.264 形式の MP4 または HLS ストリームの M3U8 マニフェストです。

ビューアは、Dynamic Media ClassicまたはExperience Manager- Dynamic Mediaビデオでも、外部ビデオでも動作します。 ビューアがDynamic Media Classic/Dynamic Mediaビデオで始まる場合、そのようなアセットタイプで使用すると、外部ビデオを次を使用してこのビューアに読み込むことはできません。 [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) メソッドを使用します。 そして逆の詩：ビューアが最初に外部ビデオで読み込まれた場合は、外部ビデオでのみ動作を続ける必要があります。

外部ビデオを操作する場合、ビューアは再生修飾子の値を無視し、外部ビデオ拡張機能から再生タイプを検出します。 外部ビデオの URL が次の語句で終わる場合 `.M3U8` ビューアでは HLS 再生が使用されていますが、それ以外の場合はプログレッシブ再生が使用されます。
