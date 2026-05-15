---
title: Dynamic Media HTML5 ビューアの必要システム構成
description: Dynamic Media HTML5 ビューアの必要システム構成。
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
TQID: 'https://experienceleague.adobe.com/tPpOrJ26zb4wztdD5XE6ErLB-6D1IZPO4MSaumdUevY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 360
ht-degree: 0%

---

# Dynamic Media HTML5 ビューアの必要システム構成{#system-requirements}

Dynamic Media HTML5 ビューアの必要システム構成。

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## サーバーハードウェアとソフトウェア {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media Image Serving 6.7.1以降。
* HTML 5 ビューアには、SDK JavaScript サーバーサイドライブラリ 3.11.5以降が必要です。
* *友達にメール*&#x200B;のソーシャル機能を利用するには、s7ondemand 5.0.9以降が必要です。
* eCatalog Viewer - [情報パネル ポップアップ ](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md)のサポートには、情報サーバー2.1.8以降が必要です。
* 検索機能コンポーネントには、s7search 2.3.0以降が必要です。

## ビューアの必要システム構成 {#section-cc72b1e209524d038b4d5b92b35e998e}

**コンポーネント ビューアのクライアント ブラウザーの最小要件：**

* 次のオペレーティングシステムのバージョン以降でサポートされています。
   * Microsoft® Windows® 7
   * macOS X 10.12
* 次のブラウザー/プラットフォームのバージョン以降でサポートされています。
   * Android™ OS 4.x
   * ネイティブブラウザー上のBlackBerry® 10。 ビデオ再生のみがサポートされています。
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * IOS6
   * iPad 2 （SafariおよびChrome ブラウザーのみ）
   * iPhone 3GS
   * Safari 11
* モバイルデバイス上のInternet Explorerはサポートされていません。
* *PanoramicViewer*&#x200B;は、次のブラウザー/プラットフォームのバージョン以降でサポートされています。
   * Android™ 4.4 （携帯端末のみ）
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Video360Viewer*&#x200B;および&#x200B;*DimensionalViewer*&#x200B;は、次のブラウザー/プラットフォームのバージョン以降でサポートされています。
   * Android™ 5 （携帯端末のみ）
   * Chrome 82
   * Edge
   * Firefox 77
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer*&#x200B;は、次のブラウザー/プラットフォーム バージョン以降でサポートされています。
   * Android™ 4.x
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

## TLS 1.0および1.1のサポート終了 {#tls}

<!-- CQDOC-19433 -->

2022年9月30日（PT）より、Adobe Dynamic Media Viewersでは、次のサポートを終了しました。

* TLS （Transport Layer Security） 1.0および1.1
* TLS 1.2の以下の脆弱な暗号：
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

## Dynamic Media ビューアでサポートされていないWeb ブラウザーとオペレーティングシステムの組み合わせ {#browser-os-support}

<!-- CQDOC-19433 -->

Adobe Dynamic Media ビューアは、次のweb ブラウザーとオペレーティングシステムの組み合わせをサポートしていません。

* Internet Explorer 11 + Windows 7
* Internet Explorer 11 + Windows 8.1
* Internet Explorer 11 + Windows Phone 8.1
* Internet Explorer 11 + Windows Phone 8.1 アップデート
* Safari 6 + iOS 6.0.1
* Safari 7 + iOS 7.1
* Safari 7 + OS X 10.9 Mavericks
* Safari 8 + iOS 8.4
* Safari 8 + OS X 10.10 Yosemite

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
FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform.
-->

