---
description: ビューアは、Dynamic Media ClassicまたはAEM Dynamic Mediaの外部でホストされているビデオの再生をサポートしています。
solution: Experience Manager
title: 外部ビデオのサポート
feature: Dynamic Media Classic，ビューア，SDK/API,360 VRビデオ
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# 外部ビデオのサポート{#external-video-support}

ビューアは、Dynamic Media ClassicまたはAEM Dynamic Mediaの外部でホストされているビデオの再生をサポートしています。

外部ビデオでサポートされる形式は、H.264形式のMP4またはHLSストリーム用のM3U8マニフェストです。

ビューアは、Dynamic Media ClassicまたはAEM Dynamic Mediaビデオで動作するか、外部ビデオで動作させることができます。 ビューアがDynamic Media Classic/AEM Dynamic Mediaビデオで開始する場合は、今後、そのようなアセットタイプで使用する必要があります。 [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)メソッドを使用してこのビューアに外部ビデオを読み込むことはできません。逆も同様です。 つまり、ビューアが最初に外部ビデオと共に読み込まれた場合、引き続き外部ビデオでのみ機能します。

外部ビデオを操作する場合、ビューアは再生修飾子の値を無視し、外部ビデオ拡張子から再生タイプを検出します。 外部ビデオのURLが`.m3u8`で終わる場合、ビューアはHLS再生を使用しています。それ以外の場合は、プログレッシブ再生が使用されます。
