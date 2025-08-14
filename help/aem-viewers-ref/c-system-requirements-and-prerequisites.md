---
title: Dynamic Media HTML5 ビューアの必要システム構成
description: Dynamic Media HTML5 ビューアの必要システム構成です。
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 2%

---

# Dynamic Media HTML5 ビューアの必要システム構成{#system-requirements}

Dynamic Media HTML5 ビューアの必要システム構成です。

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## サーバのハードウェアとソフトウェア {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media 画像サービング 6.7.1 以降。
* HTML5 ビューアを使用するには、SDK JavaScript サーバーサイドライブラリ 3.11.5 以降が必要です。
* *友達にメールを送信* ソーシャル機能には、s7ondemand 5.0.9 以降が必要です。
* eCatalog ビューア - [ 情報パネルポップアップ ](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) のサポートには、情報サーバー 2.1.8 以降が必要です。
* 検索機能コンポーネントには s7search 2.3.0 以降が必要です。

## ビューアの必要システム構成 {#section-cc72b1e209524d038b4d5b92b35e998e}

**コンポーネントビューア用のクライアントブラウザーの最小要件：**

* 次のバージョン以降のオペレーティングシステムでサポートされています。
   * Microsoft® Windows® 7
   * macOS X 10.12
* 次のブラウザー/プラットフォームバージョン以降でサポート：
   * Android™ OS 4.x
   * ネイティブブラウザーの BlackBerry® 10。 ビデオの再生のみがサポートされています。
   * Chrome82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS
   * iPad 2 （Safari およびChrome ブラウザーのみ）
   * iPhone 3GS
   * Safari 11
* モバイルデバイスでの Internet Explorer はサポートされていません。
* *PanoramicViewer* は、次のブラウザー/プラットフォームバージョン以降でサポートされています。
   * Android™ 4.4 （電話デバイスのみ）
   * Chrome82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS10
   * Safari 11
* *Video360Viewer* および *DimensionalViewer* は、次のブラウザー/プラットフォームバージョン以降でサポートされています。
   * Android™ 5 （スマートフォンのみ）
   * Chrome82
   * Edge
   * Firefox 77
   * iOS12
   * Safari 12
* *ZoomVerticalViewer* は、次のバージョン以降のブラウザー/プラットフォームでサポートされています。
   * Android™ 4.x
   * Chrome82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS10
   * Safari 11

## TLS 1.0 および 1.1 のサポート終了 {#tls}

<!-- CQDOC-19433 -->

2022 年 9 月 30 日（PT）をもって、Adobe Dynamic Media ビューアは以下のサポートを終了しました。

* TLS （Transport Layer Security） 1.0 および 1.1
* TLS 1.2 での以下の脆弱な暗号：
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
   * TLS_RSA_WITH_AES_256_GCM_SHA384
   * TLS_RSA_WITH_AES_256_CBC_SHA256
   * TLS_RSA_WITH_AES_256_CBC_SHA
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_AES_128_GCM_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_256_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_128_CBC_SHA
   * TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA
   * TLS_RSA_WITH_SDES_EDE_CBC_SHA

## Dynamic Media ビューアでサポートしていない web ブラウザーとオペレーティングシステムの組み合わせ {#browser-os-support}

<!-- CQDOC-19433 -->

Adobe Dynamic Media ビューアでは、次の web ブラウザーとオペレーティングシステムの組み合わせをサポートしていません。

* Internet Explorer 11 と Windows 7
* Internet Explorer 11 と Windows 8.1
* Internet Explorer 11 と Windows Phone 8.1
* Internet Explorer 11 と Windows Phone 8.1 Update
* Safari 6 とiOS 6.0.1
* Safari 7 とiOS 7.1
* Safari 7 と OS X 10.9 Mavericks
* Safari 8 とiOS 8.4
* Safari 8 と OS X 10.10 Yosemite

<!-- CQDOC-19433 -->

<!-- 
NOTE
Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android&trade; 2.3.7
* Android&trade; 4.0.4
* Android&trade; 4.1.1
* Android&trade; 4.2.2
* Android&trade; 4.3
* Internet Explorer 7 on Window Vista&reg;
* Internet Explorer 8 on Windows&reg; XP
* Internet Explorer 8-10 on Windows&reg; 7
* Internet Explorer 10 on Windows&reg; Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java&trade; 6u45
* Java&trade; 7u25
* OpenSSL 0.9.8y
* Baidu January 2015

NOTE
FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->

