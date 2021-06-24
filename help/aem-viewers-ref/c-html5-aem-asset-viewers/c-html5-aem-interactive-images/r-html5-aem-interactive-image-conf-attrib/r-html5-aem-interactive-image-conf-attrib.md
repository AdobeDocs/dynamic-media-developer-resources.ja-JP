---
description: インタラクティブ画像ビューアの設定属性ドキュメント。
solution: Experience Manager
title: コマンドリファレンス — 設定属性
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブ画像
role: Developer,Business Practitioner
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

インタラクティブ画像ビューアの設定属性ドキュメント。

設定コマンドは、URLまたは`setParam()`、`setParams()`、またはその両方のAPIメソッドを使用して設定できます。 設定属性は、サーバー側の設定レコードでも指定できます。

一部の設定コマンドの前に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名のプレフィックスが付く場合があります。 コンポーネントのインスタンス名は動的で、`setContainerId()` APIメソッドに渡されるビューアコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例えば、`zoomstep`コマンドは次のように記述されています。

`[ZoomView.|<containerId>_zoomView].fmt`

つまり、このコマンドは次のように使用できます。

* `fmt` （短い構文）
* `ZoomView.fmt` （コンポーネントクラス名で修飾）
* `cont_zoomView.fmt` (コンポーネントIDで修飾、 `cont` はコンテナ要素のID)

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください。
