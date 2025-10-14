---
title: コマンドリファレンス – 設定属性
description: カルーセルビューアの設定属性に関するドキュメント
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 71c2c973-d711-4d37-b778-381a7ec71527
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

カルーセルビューアの設定属性に関するドキュメント

設定コマンドは、URL で設定することも、`setParam()`、`setParams()`、またはその両方の API メソッドを使用して設定することもできます。 サーバーサイド設定レコードでは、任意の config 属性も指定できます。

一部の設定コマンドには、対応するビューア SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付いているものがあります。 コンポーネントのインスタンス名は動的であり、API メソッドに渡されるビューアコンテナ DOM 要素の ID`setContainerId()` 依存します。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、次 `zoomstep` コマンドはドキュメントに記載されています。

`[ZoomView.|<containerId>_carouselView].fmt`

その場合、次のコマンドを使用できます。

* `fmt` （短い構文）
* `CarouselView.fmt` （コンポーネントクラス名で修飾）
* `cont_carouselView.fmt` （コンポーネント ID で修飾。`cont` はコンテナ要素の ID と仮定）

[&#x200B; すべてのビューアに共通のコマンドリファレンス – 設定属性 &#x200B;](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) も参照してください。
