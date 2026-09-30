---
title: 外部ビデオのサポート
description: ビューアは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Media以外でホストされているビデオの再生をサポートしています。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
TQID: 'https://experienceleague.adobe.com/nLVjtwe8hj5YpMX6M1GKt1Fx-tZK2Qxe1kdWcK8BQPw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%
---
# 外部ビデオのサポート{#external-video-support}

ビューアは、Dynamic Media ClassicまたはAdobe Experience Manager - Dynamic Media以外でホストされているビデオの再生をサポートしています。

外部ビデオでサポートされる形式は、H.264形式のMP4またはHLS ストリームのM3U8 マニフェストです。

ビューアは、Dynamic Media ClassicまたはExperience Manager - Dynamic Media ビデオまたは外部ビデオで動作します。 ビューアがDynamic Media Classic/Dynamic Media ビデオで始まる場合は、今後このようなアセットタイプで使用します。を使用して外部ビデオをビューアに読み込むことはできません [`setVideo`]
（../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c） メソッドを使用します。 逆の逆：ビューアが最初に外部ビデオで読み込まれた場合は、外部ビデオのみを使用し続ける必要があります。

外部動画を操作する場合、ビューアは再生修飾子の値を無視し、外部動画拡張機能から再生タイプを検出します。 外部ビデオのURLが`.M3U8`で終わる場合、ビューアはHLS再生を使用しています。それ以外の場合は、プログレッシブ再生が使用されます。
