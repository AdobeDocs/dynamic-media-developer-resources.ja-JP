---
description: カルーセルビューアの設定属性ドキュメント。
solution: Experience Manager
title: コマンドリファレンス — 設定属性
feature: Dynamic Media Classic，ビューア，SDK/API，カルーセルバナー
role: Developer,Business Practitioner
exl-id: 71c2c973-d711-4d37-b778-381a7ec71527
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

カルーセルビューアの設定属性ドキュメント。

設定コマンドは、URLまたは`setParam()`、`setParams()`、またはその両方のAPIメソッドを使用して設定できます。 設定属性は、サーバー側の設定レコードでも指定できます。

一部の設定コマンドの前に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名のプレフィックスが付く場合があります。 コンポーネントのインスタンス名は動的で、`setContainerId()` APIメソッドに渡されるビューアコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例えば、`zoomstep`コマンドは次のように記述されています。

`[ZoomView.|<containerId>_carouselView].fmt`

つまり、このコマンドは次のように使用できます。

* `fmt` （短い構文）
* `CarouselView.fmt` （コンポーネントクラス名で修飾）
* `cont_carouselView.fmt` (コンポーネントIDで修飾、 `cont` はコンテナ要素のID)

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください。
