---
title: Dynamic Media Viewer5 のHTML要件
description: Dynamic Media Viewer5 のHTML要件。
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 1%

---

# Dynamic MediaHTML5 ビューアの必要システム構成{#system-requirements}

Dynamic Media Viewer5 のHTML要件。

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## サーバのハードウェアとソフトウェア {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* AdobeDynamic Media Image Serving 6.7.1 以降。
* HTML5 ビューアには、SDK JavaScript サーバー側ライブラリ3.11.5以降が必要です。
* *友達にメールを送信* social 機能には s7ondemand 5.0.9 以降が必要です。
* eCatalog ビューア — [情報パネルポップアップ](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) のサポートには、情報サーバ 2.1.8 以降が必要です。
* 検索機能コンポーネントを使用するには、 s7search 2.3.0 以降が必要です。

## ビューアの必要システム構成 {#section-cc72b1e209524d038b4d5b92b35e998e}

**コンポーネントビューアに対するクライアントブラウザーの最小要件：**

* 次のオペレーティングシステムバージョン以降でサポートされています。
   * Microsoft® Windows® 7
   * macOS X 10.12
* 次のブラウザー/プラットフォームバージョン以降でサポートされています。
   * Android™ OS 4.x
   * ネイティブブラウザー上の BlackBerry® 10。 ビデオの再生のみがサポートされています。
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS6
   * iPad 2（Safari および Chrome ブラウザーのみ）
   * iPhone 3GS
   * Safari 11
* モバイルデバイス上の Internet Explorer はサポートされていません。
* *PanoramicViewer* は、次のブラウザー/プラットフォームバージョン以降でサポートされています。
   * Android™ 4.4（電話デバイスのみ）
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Video360Viewer* および *DimensionalViewer* は、次のブラウザー/プラットフォームバージョン以降でサポートされています。
   * Android™ 5（電話デバイスのみ）
   * Chrome 82
   * Edge
   * Firefox 77
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer* は、次のブラウザー/プラットフォームバージョン以降でサポートされています。
   * Android™ 4.x
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

## TLS 1.0 および 1.1 のサポート終了 {#tls}

<!-- CQDOC-19433 -->

AdobeDynamic Mediaビューアは、2022 年 9 月 30 日に以下のサポートを終了しました。

* TLS(Transport Layer Security)1.0 および 1.1
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

## Dynamic Media Viewers でサポートされていない Web ブラウザーとオペレーティングシステムの組み合わせ {#browser-os-support}

<!-- CQDOC-19433 -->

AdobeDynamic Mediaビューアでは、次の Web ブラウザーとオペレーティングシステムの組み合わせはサポートされていません。

* Internet Explorer 11 + Windows 7
* Internet Explorer 11 + Windows 8.1
* Internet Explorer 11 + Windows Phone 8.1
* Internet Explorer 11 + Windows Phone 8.1 の更新
* Safari 6 + iOS 6.0.1
* Safari 7 + iOS 7.1
* Safari 7 + OS X 10.9 Mavericks
* Safari 8 + iOS 8.4
* Safari 8 + OS X 10.10 ヨセミテ

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

