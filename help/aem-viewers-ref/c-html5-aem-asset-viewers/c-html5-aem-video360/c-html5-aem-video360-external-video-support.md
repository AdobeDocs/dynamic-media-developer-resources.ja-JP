---
title: 外部ビデオのサポート
description: このビューアでは、Dynamic Media ClassicまたはAdobe Experience Manager（Dynamic Media）の外部でホストされるビデオの再生をサポートしています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# 外部ビデオのサポート{#external-video-support}

このビューアでは、Dynamic Media ClassicまたはAdobe Experience Manager（Dynamic Media）の外部でホストされるビデオの再生をサポートしています。

外部ビデオでサポートされている形式は、H.264 形式の MP4 か、HLS ストリームの M3U8 マニフェストです。

ビューアは、Dynamic Media ClassicまたはExperience Manager Dynamic Media ビデオ、または外部ビデオと連携できます。 Dynamic Media Classic/AEM Dynamic Media のビデオでビューアを開始する場合は、今後、このようなアセットタイプで使用する必要があります。 [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) メソッドを使用してこのビューアに外部ビデオを読み込むことはできません。その逆も同様です。 つまり、最初に外部ビデオが読み込まれたビューアは、引き続き外部ビデオでのみ動作します。

外部ビデオを操作する場合、ビューアは再生の修飾子の値を無視し、再生タイプを外部ビデオ拡張機能から検出します。 外部ビデオ URL が `.m3u8` で終わる場合、ビューアはHLS再生を使用します。それ以外の場合は、プログレッシブ再生が使用されます。
