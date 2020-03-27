---
description: フライアウトビューアの設定属性ドキュメント
seo-description: フライアウトビューアの設定属性ドキュメント
seo-title: コマンドリファレンス — 設定属性
solution: Experience Manager
title: コマンドリファレンス — 設定属性
topic: Dynamic media
uuid: 0813c334-37b7-43af-b39d-bec66658ad58
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

フライアウトビューアの設定属性ドキュメント

URLには、任意の設定コマンドを設定できます。 または、APIメソッド、APIメソッド、 `setParam()`またはそ `setParams()`の両方を使用できます。 サーバー側の設定レコードで任意の設定属性を指定することもできます。

一部の設定コマンドの先頭に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名のプレフィックスが付けられます。 コンポーネントのインスタンス名は動的で、 `setContainerId()` APIメソッドに渡されるビューアのコンテナのDOM要素のIDに依存します。 このようなコマンドのオプションのプレフィックスがドキュメントに含まれています。 例えば、このコマンドは次のよ `zoomfactor` うに記載されています。

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

このコマンドは次のように使用します。

* `zoomfactor` （短い構文）
* `FlyoutZoomView.zoomfactor` （コンポーネントのクラス名で修飾）
* `cont_flyout.zoomfactor` (コンポーネントIDで修飾、これ `cont` がコンテナ要素のIDと仮定)

すべてのビューアに共 [通のコマンドリファレンス — 設定属性も参照してください。](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
