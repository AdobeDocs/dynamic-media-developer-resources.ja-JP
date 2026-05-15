---
title: 外部ビデオのサポート
description: ビューアは、Dynamic Media ClassicまたはAdobe Experience Manager Dynamic Media以外でホストされるビデオの再生をサポートしています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
TQID: 'https://experienceleague.adobe.com/RCjgY-azk-9IIQyK6-Xz4ju6ev3Otbfs1UFvs3j385U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 0%

---

# 外部ビデオのサポート{#external-video-support}

ビューアは、Dynamic Media ClassicまたはAdobe Experience Manager Dynamic Media以外でホストされるビデオの再生をサポートしています。

外部ビデオでサポートされる形式は、H.264形式のMP4またはHLS ストリームのM3U8 マニフェストです。

ビューアは、Dynamic Media ClassicまたはExperience Manager Dynamic Media ビデオまたは外部ビデオで動作します。 ビューアがDynamic Media Classic/AEM Dynamic Media ビデオで始まる場合は、今後このようなアセットタイプで使用する必要があります。 [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) メソッドを使用してこのビューアに外部ビデオを読み込むことはできず、逆に読み込むことはできません。 つまり、ビューアが最初に外部ビデオを読み込んだ場合、外部ビデオでのみ引き続き機能します。

外部動画を操作する場合、ビューアは再生修飾子の値を無視し、外部動画拡張機能から再生タイプを検出します。 外部ビデオのURLが`.m3u8`で終わる場合、ビューアはHLS再生を使用しています。それ以外の場合は、プログレッシブ再生が使用されます。
