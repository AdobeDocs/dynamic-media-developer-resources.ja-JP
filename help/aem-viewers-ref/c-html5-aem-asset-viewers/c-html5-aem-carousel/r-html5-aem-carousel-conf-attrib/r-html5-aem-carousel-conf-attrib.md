---
title: コマンドリファレンス — 設定属性
description: カルーセルビューアの設定属性ドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 71c2c973-d711-4d37-b778-381a7ec71527
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

カルーセルビューアの設定属性ドキュメント。

任意の設定コマンドを URL で設定するか、 `setParam()`または `setParams()`またはその両方の API メソッドを使用できます。 設定属性は、サーバー側の設定レコードでも指定できます。

一部の設定コマンドの前に、対応するビューア SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付く場合があります。 コンポーネントのインスタンス名は動的で、に渡されるビューアのコンテナの DOM 要素の ID に依存します。 `setContainerId()` API メソッド。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例： `zoomstep` コマンドの説明は次のとおりです。

`[ZoomView.|<containerId>_carouselView].fmt`

この場合、次のコマンドを使用できます。

* `fmt` （短い構文）
* `CarouselView.fmt` （コンポーネントのクラス名で修飾）
* `cont_carouselView.fmt` （コンポーネント ID で修飾、仮定） `cont` はコンテナ要素の ID です )

関連トピック [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
