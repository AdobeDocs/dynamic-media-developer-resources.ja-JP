---
title: 外部ビデオのサポート
description: このビューアでは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Mediaの外部でホストされるビデオの再生をサポートしています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# 外部ビデオのサポート{#external-video-support}

このビューアでは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Mediaの外部でホストされるビデオの再生をサポートしています。

外部ビデオでサポートされている形式は、H.264 形式の MP4 か、HLS ストリームの M3U8 マニフェストです。

ビューアは、Dynamic Media Classic、Experience Manager - Dynamic Media ビデオまたは外部ビデオと連携して動作します。 ビューアがDynamic Media Classic/Dynamic Mediaのビデオから始まる場合は、そのようなアセットタイプで使用してください。[`setVideo`] を使用して外部ビデオをこのビューアに読み込むことはできません
（../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c） メソッド。 そして逆の節：ビューアが最初に外部ビデオで読み込まれた場合、外部ビデオでのみ作業し続ける必要があります。

外部ビデオを操作する場合、ビューアは再生の修飾子の値を無視し、再生タイプを外部ビデオ拡張機能から検出します。 ビューアが HLS 再生を使用してい `.M3U8` 外部ビデオ URL がで終わる場合、それ以外の場合はプログレッシブ再生が使用されます。
