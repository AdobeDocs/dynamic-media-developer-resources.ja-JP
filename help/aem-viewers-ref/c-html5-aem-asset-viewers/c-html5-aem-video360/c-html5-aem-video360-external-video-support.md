---
title: 外部ビデオのサポート
description: ビューアでは、Dynamic Media Classic、Adobe Experience Manager、Dynamic Mediaの外部でホストされているビデオの再生がサポートされています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 外部ビデオのサポート{#external-video-support}

ビューアでは、Dynamic Media Classic、Adobe Experience Manager、Dynamic Mediaの外部でホストされているビデオの再生がサポートされています。

外部ビデオでサポートされる形式は、H.264 形式の MP4 または HLS ストリームの M3U8 マニフェストです。

ビューアは、Dynamic Media Classicビデオ、Experience ManagerDynamic Mediaビデオ、または外部ビデオと連携できます。 ビューアがDynamic Media Classic/AEM Dynamic Mediaビデオで始まる場合は、今後、そのようなアセットタイプで使用する必要があります。 [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) メソッドおよび逆に、このビューアに外部ビデオを読み込むことはできません。 つまり、最初に外部ビデオと共に読み込まれた場合、引き続き外部ビデオでのみ機能します。

外部ビデオを操作する場合、ビューアは再生修飾子の値を無視し、外部ビデオ拡張子から再生タイプを検出します。 外部ビデオの URL が `.m3u8` で終わる場合、ビューアは HLS 再生を使用しています。それ以外の場合は、プログレッシブ再生が使用されます。
